
---
title: "开发了一个一键去背景工具"
date: 2022-12-14
description: All the list of my posts
---

jr们早上好

iPhone 的 iOS 16有个很酷的功能，长按照片就能把其中的拍摄主体提取出来，抠图过程比一般的抠图App方便，精细度也更高。

![](/Users/huhaiyang/projs/mdFiles/images/苹果抠图.gif)

最近发现一个Python库——rembg，后台引擎是用于显著对象检测的深度网络架构 U²-Net

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221012145220.png)

所以我就用它开发了一个在线抠图应用，依然是依托Gradio + huggingface 的space

大家先来感受一下

https://huggingface.co/spaces/beihai/Remove-Background-By-U2Net

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221012144211.png)


用法非常简单，上传需要去背景的图片，点击Submit，稍等片刻，右侧Output将去背景后的主体另存为即可。

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221012145744.png)


抠图应该算蛮成熟的应用了，不过学以致用嘛。

自己动手做一个大家不觉得这很酷吗?作为一名理工男我觉得这太酷了，很符合我对未来生活的想象，科技并带着趣味。/手动狗头

实现过程实在不想再讲了，因为我之前在[腾讯的这个算法，我搬到了网上，随便玩！](https://mp.weixin.qq.com/s?__biz=MzA4MjYwMTc5Nw==&mid=2648965011&idx=1&sn=5a16c12fb7396cfd455ee327bbce3aea&chksm=87946db9b0e3e4afb3324c40ff439ab03a069c3b4f6a18c704f02b0172aa68478f72931dc829&token=474570519&lang=zh_CN#rd) 还有 [LightGBM 可视化调参](https://mp.weixin.qq.com/s?__biz=MzA4MjYwMTc5Nw==&mid=2648965227&idx=1&sn=6ab3c6d1f26c1ae28f56c0d4207d4e2a&chksm=87939241b0e41b5759dbc6153b00d71b4c8689e25e770c35cfe3c3a5a38e0b154a159aeedb04&scene=21#wechat_redirect)这两篇文章中已经讲过了：



step1：注册Huggingface账号

step2：创建Space，SDK选Gradio

step3：克隆新建的space代码，然后将改好的代码push上去




这里只展示下核心代码吧，也是简单的离谱


## 核心代码

```Python
import os
os.system("/usr/local/bin/python -m pip install --upgrade pip")
import gradio as gr
from rembg import remove
import cv2

def inference(img):
    input_img = cv2.imread(img)
    output = remove(input_img[:, :, [2,1,0]])
    return output

gr.Interface(
    inference, 
    gr.inputs.Image(type="filepath", label="Input"), 
    gr.outputs.Image(type="pil", label="Output")
    ).launch() 
```

