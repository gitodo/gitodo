+++
title = "3个步骤解决Chrome浏览器software reporter tool占用CPU过高"
date = "2022-08-19T10:41:11+08:00"
description = "software_reporter_tool.exe 是 Chrome 浏览器的清理工具，但会自动运行。经常出现引发的问题是 CPU 占用率过高，导致 Chrome 停止工作等。3 步解决 Chrome 浏览器 software_reporter_tool.exe 占用 CPU 过高的问题，不用重置，更不用换浏览器。"

tags = ["网络工具",]
+++

software_reporter_tool.exe 是 Chrome 浏览器的清理工具，但会自动运行。经常出现引发的问题是 CPU 占用率过高，导致 Chrome 停止工作等。3 步解决 Chrome 浏览器 software_reporter_tool.exe 占用 CPU 过高的问题，不用重置，更不用换浏览器。
<!--more-->

![3步解决Chrome浏览器software_reporter_tool.exe占用CPU过高](/images/2022/0819-software-reporter-tool-chrome-cpu.jpg)

平时几乎不关电脑，今天 Windows 更新被迫重启。然后发现 CPU 逼近 100%，电脑风扇呼呼转。打开任务管理器发现一个`software_reporter_tool.exe`进程，强制结束后电脑才恢复。

但`software_reporter_tool.exe`进程会自动运行，有没有彻底的解决方案呢？

## 禁用 Software_Reporter_Tool.exe

我们可以直接删除这个工具，无副作用。方法也很简单，3个步骤即可。

1. 进入`software_reporter_tool.exe`所在文件夹：在文件资源管理器中打开路径`%USERPROFILE%\AppData\Local\Google\Chrome\User Data\`，然后删除`SwReporter`
2. 我们需要新建一个同名的 0 字节文件：右键新建文本文档，把文件名修改为`SwReporter`，注意不要保留`.txt`后缀
3. 最后，我们需要禁止 Chrome 修改此文件：右键文件属性-安全-编辑-Users的权限选择全部选择拒绝

如何显示文件后缀，请自行搜索。
