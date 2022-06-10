+++
title = "30分钟安装Google Tag Manager，从此调整埋点不求人"
date = "2022-06-08T11:14:34+08:00"
description = "GTM代码管理器（Google Tag Manager）是一个 Google 官方工具，安装Google Tag Manager到网站后，可以用来添加和管理第三方代码段。GTM代码管理器就像“中间人”，用于连接网站和其他第三方代码。"

tags = ["GTM代码管理器",]
+++
GTM代码管理器（Google Tag Manager）是一个 Google 官方工具，安装Google Tag Manager到网站后，可以用来添加和管理第三方代码段。GTM代码管理器就像“中间人”，用于连接网站和其他第三方代码。所以只安装GTM没有任何作用，需要在GTM中配置第三方代码后才能发挥作用。

<!--more-->

## 如何创建 Google Tag Manager
Google 账户可以登录“Google 全家桶”，包括 Google Tag Manager。所以，有了 Gmail 账户，直接登录 Google Tag Manager即可，无需额外创建账户。并且在同一个 Google Tag Manager 账户下，可以同时管理多个网站或者 APP 对象，不同的对象分别对应的容器下，不会相互影响。如果需要同时管理多个网站，也无需为不同的网站创建多个  Google Tag Manager 账户。

登录 Gmail 账户后，进入[Google Tag Manager 官网](https://tagmanager.google.com/) 会自动开通账户权限。

## 在GTM中创建 Account 和 Container

同一个 Google Tag Manager 下可以创建多个 Account，同一个 Account 下可以创建多个 Container，一个 Container 对应了一个的 Google Tag Manager 代码，一个 Google Tag Manager 代码只能安装到一个网站或 APP 中。

![在GTM中创建 Account 和 Container](/images/2022/0609-gtm中创建account-container.png)

创建 Account 时，系统会默认创建一个 Container。

1. 在 Google Tag Manager 中，点击右上角创建帐号
2. 输入帐号名称，名字和国家随意
3. 输入 Container 名称，然后选择如下内容类型：网站、AMP、Android 或 iOS。
4. 点击创建。

向现有 Account 添加新 Container

1. 在 Google Tag Manager 中，点击 Account 右侧的三个竖点，弹出菜单。
2. 点击 Create Container
3. 输入 Container 名称，然后选择如下内容类型：网站、AMP、Android 或 iOS。
4. 点击创建。

## 如何安装 Google Tag Manager

完成 Container 的创建后，我们需要找到 Container 对应的 GTM 代码，然后把代码安装到待埋点的网站上即可。

1. 在 Google Tag Manager 中，点击工作区。
2. 在靠近窗口顶部的位置，找到容器 ID，格式为“GTM-XXXXXX”。
3. 点击容器 ID，打开“安装跟踪代码管理器”框。
4. 按照“安装跟踪代码管理器”框中的说明，将代码段复制并粘贴到网站，或下载并安装相应的移动 SDK。

![安装 Google Tag Manager](/images/2022/0609-安装-google-tag-manager.png)

安装 Google Tag Manager 很简单，复制粘贴即可，但是需要拥有修改网站代码的权限。所以安装 Google Tag Manager 可能需要网站前端同事配合完成，先把 GTM 中生成的代码复制粘贴到 TXT 文本中，注意不要粘贴到 Word 文档中。

Google Tag Manager 有两段，第一段放在 `<head>` 标签中，第二段放在 `<body>` 标签中。

## 如何验证 Google Tag Manager 的安装结果

Google Tag Assistant 是谷歌官方提供的 Chrome 浏览器扩展程序，有助于解决各种安装 Google tags 中遇到的问题，包括 Google Analytics、Google Tag Manager 等。

![如何验证 Google Tag Manager 的安装结果](/images/2022/0609-验证gtm安装结果.jpg)

如果你正在使用 Chrome 或 Edge 浏览器，可以点击此处[安装 Google Tag Assistant](https://chrome.google.com/webstore/detail/tag-assistant-legacy-by-g/kejbdjndbnbjgmefkgdddjlbokphdefk)。

安装完成后，Google Tag Assistant 图标就会显示在 Chrome 浏览器的扩展程序栏中。点击扩展程序栏的Google Tag Assistant 图标，选择启用(Enable)。

刷新页面，Google Tag Assistant 将会对网页上的代码进行分析。请注意，扩展程序的图标颜色可能会改变并显示数字，具体取决于其发现的代码。

系统会显示记录的网页上发现的每个代码以及相应代码的详情。代码和问题消息使用不同的颜色进行标记，以表明发现的问题类型：

* 绿色标记图标或消息表示没有发现任何代码存在问题。
* 蓝色标记图标或消息表示某个代码存在微小的实现问题，但不影响使用。
* 黄色标记图标或消息警告代码实现可能会导致结果与预期不符。
* 红色标记图标或消息表示某个代码存在严重的实现问题。相应代码可能无法正常使用，并且可能会导致报告中的数据有误或缺失。