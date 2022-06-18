+++
title = "V97版以上，如何修改Firefox浏览器的滚动条"
date = "2022-06-18T10:41:11+08:00"
description = "本来想鼠标离开的时候让滚动条自动隐藏，但现在的 Firefox 中似乎无法实现。无奈 Windows 系统中 Firefox 浏览器的滚动条实在丑陋，无法忍受。所幸终于找到修改滚动条样式的方法，可以做个简单的美化。过程也很简单，1分钟搞定，甚至不需要重启浏览器。"

tags = ["网络工具",]
+++

本来想鼠标离开的时候让滚动条自动隐藏，但现在的 Firefox 中似乎无法实现。无奈 Windows 系统中 Firefox 浏览器的滚动条实在丑陋，无法忍受。所幸终于找到修改滚动条样式的方法，可以做个简单的美化。过程也很简单，1分钟搞定，甚至不需要重启浏览器。
<!--more-->

## 通过`about:config`修改Firefox滚动条样式

97 版本以上的 Firefox 有五种滚动条样式，这五种滚动条样式分别对应了不同的平台。

* macOS 系统
* Linux 系统
* Android 系统
* Windows 10 系统
* Windows 11 系统

### 修改Firefox滚动条的步骤

1. 启动Firefox浏览器
2. 在地址栏输入`about:config`，然后按回车键
3. 点击确认接受风险并继续的提示
4. 在Config界面找到`widget.non-native-theme.scrollbar.style`
5. 编辑`scrollbar.style`的值，默认为`0`
6. 点击保存对勾形状

![修改Firefox滚动条样式](/images/2022/0618-修改Firefox滚动条样式.jpg)

有以下6个值可供你选择：

* 数值`0` = 默认滚动条样式
* 数值`1` = macOS 苹果系统样式
* 数值`2` = GTX Linux 系统样式
* 数值`3` = 安卓系统样式
* 数值`4` = Windows 10 样式
* 数值`5` = Windows 11 样式

修改保存后，浏览器即可就可以更换滚动条的样式。例如当你输入`1`之后，Firefox 的滚动条形状会变成更圆润的 macOS 样式，当鼠标接触后滚动条的颜色会变成深色。

![macOS系统firefox滚动条样式](/images/2022/0618-macOS系统firefox滚动条样式.jpg)

如果你想要恢复 Firefox 默认的设置，只需要重新进入`about:config`，然后把`widget.non-native-theme.scrollbar.style`的值改回默认的`0`即可。

修改 Firefox 的滚动条样式不会对浏览器的性能或其他功能造成任何影响，仅仅改变滚动条的外观。

此外，在 Firefox 浏览器的扩展程序商店中，也有一些可以改变滚动条样式的插件，例如 [Custom Scrollbars 免费插件](https://addons.mozilla.org/en-GB/firefox/addon/custom-scrollbars/)。不过这些我没有测试过，如果你有兴趣，也可以尝试下。