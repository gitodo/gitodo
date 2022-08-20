+++
title = "3步修改Hosts禁用Edge浏览器标签页广告推送"
date = "2022-08-16T10:41:11+08:00"
description = "Edge 浏览器的新标签页广告内容可以设置关闭，但在中国大陆地区又无法通过设置的方式彻底关闭。绕过 Edge 浏览器中的设置，我们可以 3 步修改 Hosts 禁用 Edge 浏览器标签页广告推送。"

tags = ["网络工具",]
+++

Edge 浏览器的新标签页广告内容可以设置关闭，但在中国大陆地区又无法通过设置的方式彻底关闭。绕过 Edge 浏览器中的设置，我们可以 3 步修改 Hosts 禁用 Edge 浏览器标签页广告推送。
<!--more-->

![3步修改Hosts禁用Edge浏览器标签页广告推送](/images/2022/0816-microsoft-edge-hosts-ads.jpg)

## 修改Hosts禁用Edge浏览器标签页广告推

1. 进入`hosts`文件目录：在文件管理器中打开`C:\Windows\System32\drivers\etc`
2. 编辑`hosts`文件：使用记事本打开`hosts`文件，并在末尾添加以下内容
3. 保存`hosts`文件：保存编辑后的`hosts`文件，有些情况下没有保存权限，可以先保存到桌面，然后移动替换原来的`hosts`文件

注意：以下`hosts`内容将屏蔽 Microsoft 的跟踪，可以起到更好的隐私保护效果，并且对绝大部分用户来说没有任何影响。

```
# 屏蔽 Edge 浏览器跟踪
0.0.0.0 msn.cn
0.0.0.0 ntp.msn.cn
0.0.0.0 assets.msn.cn
0.0.0.0 c.msn.com
0.0.0.0 ntp.msn.com
0.0.0.0 api.msn.com
0.0.0.0 browser.events.data.msn.com
0.0.0.0 img-s-msn-com.akamaized.net
0.0.0.0 ad.doubleclick.net
0.0.0.0 a.ads1.msn.com
0.0.0.0 a.ads2.msads.net
0.0.0.0 a.ads2.msn.com
0.0.0.0 ads.arcct.msn.com
0.0.0.0 ads.msn.com
0.0.0.0 ads1.msads.net
0.0.0.0 ads1.msn.com
0.0.0.0 aidps.atdmt.com
0.0.0.0 aka-cdn-ns.adtech.de
0.0.0.0 b.ads1.msn.com
0.0.0.0 b.ads2.msads.net
0.0.0.0 c.atdmt.com
0.0.0.0 cdn.atdmt.com
0.0.0.0 db3aqu.atdmt.com
0.0.0.0 ec.atdmt.com
0.0.0.0 events-sandbox.data.msn.com
0.0.0.0 events.data.microsoft.com
0.0.0.0 feedback.microsoft-hohm.com
0.0.0.0 feedback.search.microsoft.com
0.0.0.0 feedback.smartscreen.microsoft.com
0.0.0.0 feedback.windows.com
0.0.0.0 functional.events.data.microsoft.com
0.0.0.0 mobile.events.data.microsoft.com
0.0.0.0 microsoftnews.msn.com
0.0.0.0 nw-umwatson.events.data.microsoft.com
0.0.0.0 preview.msn.com
0.0.0.0 view.atdmt.com
```

## 清除缓存的广告文件

修改完`hosts`文件后，遗留的旧广告仍然会出现的 Edge 浏览器的标签页中，下一步我们来删除浏览器中的缓存文件。

1. 删除缓存文件：在 Edge 浏览器中打开 `edge://settings/clearBrowserData`，勾选缓存图像和文件，然后点击删除
2. 清除DNS缓存：快捷键`Win+R`打开运行，输入`CMD`，打开命令提示符，输入`ipconfig /flushdns`后按回车
3. 重启浏览器：重启之后 Edge 浏览器的新标签页就看不到广告推送了

以上操作不会影响 Edge 浏览器正常工作，对网页访问速度和浏览器的更新无干扰。