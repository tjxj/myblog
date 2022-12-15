---
title: "去谷歌开发者大会了，收“获”满满"
date: "2022-12-14"
description: All the list of my posts
---
> **多图预警，请耐心等待加载**

周四去上海参加了谷歌开发者大会，收获满满。
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20220916160531.png)

下面我就当个导游，带大家畅游一番吧。  
先来到世博中心，显眼的 `Google Logo`
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4343.jpeg)
入场后先报道，领取胸牌  
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4436.jpeg)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4349.jpeg)
进入主会场  
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4347.jpeg)

等待演讲开始  
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4358.jpeg) 
前面是关于`Android`的演讲就不拍了，和大家一样，我对谷歌在 `TensorFlow` 和 机器学习方面的最新动态比较感兴趣。
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4369.jpeg)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4370.jpeg)

## 主题1 《未来之路：谷歌为开发者提供全面的开源机器学习产品生态》

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4373.jpeg)

其实这一部分的核心内容在昨天的主旨演讲中`Laurence`已经简单介绍过，大佬从数据、框架、模型、MLOps 四个方面说明 `TensorFlow Project` 为开源机器学习构建了全面开源生态，感兴趣可以去大会官网听一下，其实现场的演讲也都有回放了：

> https://developersummit.googlecnapps.cn/

现场嘉宾讲的更详细，每一方面都有展开，其实核心就是下面这张图
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4380.jpeg)

机器学习的四个支柱：数据、模型框架、部署、监控和维护，这四个支柱 `Google` 都有开源工具。

### `数据获取及预处理：TensorFlow 数据集`
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4381.jpeg)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4389.jpeg)

### `模型框架：TensorFlow 和 JAX`

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4396.jpeg)

`Deepmind` 的一些科研成果，比如`alphafold`,还有`Google research`的 `imagen`、 `Parti` 都是通过`JAX`创建的。

  `JAX` 前段时间还有个趣闻，关注我公众号的同学应该知道，有篇文章说“JAX取代TensorFlow”，“谷歌大脑和DeepMind已经普遍放弃TensorFlow，转投 JAX”。（➡️[TensorFlow，危！抛弃者正是谷歌自己](https://mp.weixin.qq.com/s?__biz=MzA4MjYwMTc5Nw==&mid=2648967200&idx=1&sn=c367a7a51414e0058faa3fc044a652d2&chksm=87939a0ab0e4131ce0dd77459980e27e421d1b52dc644d30a29118e7c66e5654a44402852d17&token=1004761094&lang=zh_CN#rd)），很快就有了辟谣（➡️[TensorFlow团队：我们没被抛弃](https://mp.weixin.qq.com/s?__biz=MzA4MjYwMTc5Nw==&mid=2648967438&idx=1&sn=52203fd39921fe307bae329376d64e5f&chksm=87939b24b0e41232ca2cb14cb5cc3e4b01c5fa1c04ab3fe02f39420e39a7cafdc546e009a65b&token=1004761094&lang=zh_CN#rd)），将继续投资`TensorFlow`和`JAX`两个`ML`框架，以推动数百万用户的研究和应用。

演讲嘉宾讲的很透彻，`JAX` 和 `TensorFlow` 是定位不同的两个框架，前者专为硬件加速器优化的框架，从而帮助开发者更深入地钻研机器学习的数学运算，后者定位高级框架，帮助不需要深入到数学层面的开发者可以轻松创建自己的模型。

### `模型部署：TensorFlow.js 、TensorFlow Lite`
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4403.jpeg)

在云端、网页端、浏览器、移动端和嵌入式平台上运行模型，`Google` 也有很多成熟的产品，我之前也曾写过一篇文章介绍`tfjs`（[用浏览器玩机器学习，赞！](https://mp.weixin.qq.com/s?__biz=MzA4MjYwMTc5Nw==&mid=2648964943&idx=1&sn=a38aebef63532a8b0fd172095583cd32&chksm=87946d65b0e3e473d42b1ccbc9cd7d258a69c760672e761e4a16dde8590890725e8937b95991&token=820012341&lang=zh_CN&scene=21#wechat_redirect)），自认写的清晰明了。

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4406.jpeg)

`Google Lite `也挺亮眼的，它可以内置到 `Google Play` 服务中，不需要再在应用中植入 `TF Lite` ，应用体量可以大幅缩减，也可以使用后台更新功能，用户始终能够使用最新版本，不需要在TF Lite每次更新时再重新。如果用户不使用 `Google Play` 服务，也可以不使用以上方式，像以前一样自主分发。

### `监控和维护：TFX `

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4401.jpeg)

TFX 不仅可以用于模型部署，它也可为完整 `MLOps` 部署提供软件框架和工具，并在数据和模型随时间推移不断演变的过程中检测问题。

这四个支柱中 `Google` 提供的一些列工具集成到一起，统称为`Tensor Projects`，满足研究人员、开发者、MLOPS 和商务团队的任意机器学习应用需求。

## 主题2 《MediaPipe: 搭建你自己的端侧开源机器学习解决方案》

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4418.jpeg)

之前没有关注过这一块，设备端（智能手机、物联网设备或浏览器）机器学习其实已经有很多成熟的应用：

- Google Meet的背景模糊处理/替换
- Nest 的人员移动侦测、包裹递送通知、手势识别
- YouTube 的AR 试妆

设备端机器学习主要包括设备端模型和机器学习流水线，模型是核心，机器学习流水线涵盖从原始输入到输出结果的全流程，两者都非常复杂。

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4413.jpeg)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4414.jpeg)

`MediaPipe` 可以极大简化这个过程，它可以把流水线封装成 `MediaPipe Tasks`，用 `Model Maker` 定制模型，通过低代码 `API` 提供可定制的高性能设备端机器学习解决方案。
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4421.jpeg)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4423.jpeg)

使用貌似也挺简单的，和把大象装进冰箱一样，一共分三步：  
收集训练数据、使用 `Tasks` 或 `Model Maker` 枃建模型、使用 `Task library`部署模型。

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4434.jpeg)

`MediaPipe` 确实挺有意思的，嘉宾分享了好几个资源，我计划之后深入学习学习  

> https://mediapipe.dev    
> https://github.com/google/mediapipe    
> https://google.github.io/mediapipe/solutions/pose.html  

----


下午场是展示区的技术/产品趣味互动体验，有点困，先喝杯 `Google` 牌雀巢咖啡提提神

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4458.jpeg)

在展区打卡领到许多小礼品：`Android` 吉祥物、充电线、眼镜、水杯、悠悠球、鼠标垫、冰箱贴、各种贴纸

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20220916160531.png)


当然，这些都是身外之物，体验 `Google` 黑科技才是正事，这部分我会剪个视频在 B 站发布，这里就以图文介绍吧。

## 黑科技1: 智能互动，让音乐“动”起来
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/IMG_4449.jpeg)

挺好玩的，在摄像头前挥舞手臂，就可以化身指挥家，指挥交响乐团。这个 `Semi-Conductor` 使用了 `PoseNet` 这个可在浏览器中运行的开源机器学习模型，能够将网络摄像头拍到的身体动作映射到对应的指挥操作。运用其独特的算法，该应用得以有机融合数百个短小的乐器录音片段，让乐团演奏的乐曲能够随着你的指挥而变化。

## 黑科技2: 激发音乐灵感，创造无限可能

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20220916221852.png)

`Tone Transfer` 让你可以将日常生活中的各种声音转化为乐器声，比如可以直接对着话筒哼一段旋律，直接在浏览器中录制和上传声音，机器学习模型将它转化成萨克斯风、长笛和其他乐器的声音!

## 黑科技3: MediaPipe Tasks 面部追踪、姿态检测

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20220916231854.png)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20220916231955.png)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20220916232152.png)

这几个都是前面介绍过的 `MediaPipe` 实现的，听介绍，代码量极低。


## 开启 TensorFlow 进阶之旅，丰富学习资源，待你探索
你是否正在研究如何更高效地使用 `TensorFlow` 开发和训练开源机器学习模型，成为开源机器学习专家? 在这里，根据自身需求，灵活挑选合适的学习资源，开启进阶之旅吧!


# TensorFlow & 机器学习 丰富的学习资源

最后再放几个资源吧，也是在展区看到的。

为了使开发者更高效地使用 `TensorFlow` 开发和训练开源机器学习模型，`Google` 还有很多开源课程。

比如：

`Google` 携手网易有道在中国大学 `MOOC` 平台上发布的《 TensorFlow 入门课程 - 部署篇》 专题课程

https://www.icourse163.org/course/youdao-1467217161?from=searchPage&outVendor=zw_mooc_pcssjg_

Google 开发者在线课程，针对希望在部署层面得到进阶提升的开发者。

https://developers.google.cn/learn/pathways?utm_source=social&utm_medium=devkol&utm_campaign=gds22

TensorFlow 开发者认证计划，通过考试的开发者，有机会荣获官方颁发的 TensorFlow 开发者证书和徽章。

https://www.tensorflow.org/certificate?hl=zh-cn

# 总结

总结一句话就是：不虚此行，下次一定还来。

大家一起 `Code For Better`，“共码未来” 吧，我要去学 `MediaPipe` 了。