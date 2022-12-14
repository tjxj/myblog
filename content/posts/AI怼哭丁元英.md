---
title: "我是ChatGPT，我怼哭了丁元英"
date: "2022-12-14"
description: All the list of my posts
---

大家好，最近科技界的顶流非 OpenAI 的 ChatGPT 莫属。

大家都在探索它的使用极限，无论接受以否，未来它都将影响我们的生活。ChatGPT 写故事，编程、解答世间万物、翻译、取标题、写摘要、写对联，你能想到的所有文字内容他都能hold住（虽然也闹了不少笑话）。

昨天我尝试了一个非常有意思的玩法，就是让 ChatGPT 来个角色扮演，然后居然还发现了一个彩蛋，有趣是一方面，由此也可窥见 ChatGPT 之强大。

实现过程如下：

先让他假装成 Linux 终端

```
我要你假装是一个Linux终端。我会输入命令，你回复终端应该显示什么。我希望你只用一个唯一的代码块里的终端输出回复，别的都不要。不要输出解释。除非我指示你这样做，否则不要输入命令。当我需要用中文告诉你什么时，我会用花括号{像这样}把文本放在里面。我的第一个命令是pwd。
```

然后居然真的可以执行，列出了当前路径

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211205338.png)


然后用`ls -R`看看各目录下都有什么文件

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211210135.png)


其实每个文件我都看了，只有`./Documents/project1/data.txt` 有实质内容。

大家好奇这个txt里是什么吗？cat 命令看一眼


![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211205633.png)


“The quick brown fox jumps over the lazy dog”（中译为“敏捷的棕毛狐狸从懒狗身上跃过”）是一个著名的英语全字母句，刚好包含了从A到Z全部26个字母。

这句话常被用于测试字体的显示效果和键盘有没有故障，现在各类浏览器的字体设定中常把该句子作为预览句。


``./Documents/project1/`下面还有个script.py ,也来看一眼：

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211205741.png)


可惜不能执行，因为没有pandas
![20221211213337](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211213337.png)


顺便看一眼python版本，挺老的

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211213413.png)

至于figure目录下的这三种图片是什么，可能是个很大的谜了。

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211205902.png)




对了，ChatGPT 假装成的这个Linux还有更多东西可以探索

比如：创建文件

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211223047.png)


比如：我把内置的python升级到了3.0

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211224306.png)
![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211224323.png)

还安装了pandas

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211224348.png)

大家有什么发现，欢迎告诉我。


`one more thing` ，那个令人闻风丧胆的命令可以执行吗？

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211221822.png)


嗯，想多了

![](https://my-wechat.oss-cn-beijing.aliyuncs.com/20221211221858.png)

Bye