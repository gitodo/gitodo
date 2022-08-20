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
0.0.0.0 a-0001.a-msedge.net
0.0.0.0 a-0002.a-msedge.net
0.0.0.0 a-0003.a-msedge.net
0.0.0.0 a-0004.a-msedge.net
0.0.0.0 a-0005.a-msedge.net
0.0.0.0 a-0006.a-msedge.net
0.0.0.0 a-0007.a-msedge.net
0.0.0.0 a-0008.a-msedge.net
0.0.0.0 a-0009.a-msedge.net
0.0.0.0 a-msedge.net
0.0.0.0 a.ads1.msn.com
0.0.0.0 a.ads2.msads.net
0.0.0.0 a.ads2.msn.com
0.0.0.0 a.rad.msn.com
0.0.0.0 ac3.msn.com
0.0.0.0 ad.doubleclick.net
0.0.0.0 adnexus.net
0.0.0.0 adnxs.com
0.0.0.0 ads.arcct.msn.com
0.0.0.0 ads.msn.com
0.0.0.0 ads1.msads.net
0.0.0.0 ads1.msn.com
0.0.0.0 aidps.atdmt.com
0.0.0.0 aka-cdn-ns.adtech.de
0.0.0.0 api.edgeoffer.microsoft.com
0.0.0.0 api.msn.com
0.0.0.0 api.vcservice.webxtsvc-int.microsoft.com
0.0.0.0 api.webxtsvc.microsoft.com
0.0.0.0 apps.skype.com
0.0.0.0 arc.msn.com
0.0.0.0 assets.msn.com
0.0.0.0 az361816.vo.msecnd.net
0.0.0.0 az512334.vo.msecnd.net
0.0.0.0 b.ads1.msn.com
0.0.0.0 b.ads2.msads.net
0.0.0.0 b.rad.msn.com
0.0.0.0 bat.bing.com
0.0.0.0 browser.events.data.msn.com
0.0.0.0 browser.pipe.aria.microsoft.com
0.0.0.0 bs.serving-sys.com
0.0.0.0 c.atdmt.com
0.0.0.0 c.bing.com
0.0.0.0 c.live.com
0.0.0.0 c.msn.com
0.0.0.0 c1.microsoft.com
0.0.0.0 ca.telemetry.microsoft.com
0.0.0.0 cache.datamart.windows.com
0.0.0.0 cdn.atdmt.com
0.0.0.0 cdn.edgeoffer.microsoft.com
0.0.0.0 cds26.ams9.msecn.net
0.0.0.0 choice.microsoft.com
0.0.0.0 choice.microsoft.com.nsatc.net
0.0.0.0 choice.microsoft.com.nstac.net
0.0.0.0 citrix.onmicrosoft.com
0.0.0.0 clarity.ms
0.0.0.0 clientfd.family.microsoft.com
0.0.0.0 cloudbrowser.microsoft.com
0.0.0.0 cn.bing.com
0.0.0.0 compatexchange.cloudapp.net
0.0.0.0 config.edge.skype.com
0.0.0.0 corp.sts.microsoft.com
0.0.0.0 corpext.msitadfs.glbdns2.microsoft.com
0.0.0.0 crl.microsoft.com
0.0.0.0 cs1.wpc.v0cdn.net
0.0.0.0 customervoice.microsoft.com
0.0.0.0 db3aqu.atdmt.com
0.0.0.0 db3wns2011111.wns.windows.com
0.0.0.0 df.telemetry.microsoft.com
0.0.0.0 diagnostics.support.microsoft.com
0.0.0.0 ec.atdmt.com
0.0.0.0 edge-staging.microsoft.com
0.0.0.0 edge-test.microsoft.com
0.0.0.0 edge.cloudbrowser.microsoft.com
0.0.0.0 edge.microsoft.com
0.0.0.0 edgeservices.bing.com
0.0.0.0 edgeshoppingstatic.azureedge.net
0.0.0.0 edgetippingservice.webxtsvc.microsoft.com
0.0.0.0 events-sandbox.data.msn.com
0.0.0.0 events.data.microsoft.com
0.0.0.0 family.api.account.microsoft.com
0.0.0.0 farevents.family.microsoft.com
0.0.0.0 fe2.update.microsoft.com.akadns.net
0.0.0.0 fe3.delivery.dsp.mp.microsoft.com.nsatc.net
0.0.0.0 feedback.microsoft-hohm.com
0.0.0.0 feedback.search.microsoft.com
0.0.0.0 feedback.smartscreen.microsoft.com
0.0.0.0 feedback.windows.com
0.0.0.0 flex.msn.com
0.0.0.0 forms.microsoft.com
0.0.0.0 functional.events.data.microsoft.com
0.0.0.0 g.bing.com
0.0.0.0 g.msn.com
0.0.0.0 global.bing.com
0.0.0.0 go.microsoft.com
0.0.0.0 graph.microsoft.com
0.0.0.0 h1.msn.com
0.0.0.0 i1.services.social.microsoft.com
0.0.0.0 i1.services.social.microsoft.com.nsatc.net
0.0.0.0 inference.location.live.com
0.0.0.0 instrumentExport.cp.microsoft.com
0.0.0.0 lb1.www.ms.akadns.net
0.0.0.0 live.rads.msn.com
0.0.0.0 local.cloudbrowser.microsoft.com
0.0.0.0 m.adnxs.com
0.0.0.0 m.bing.com
0.0.0.0 m.hotmail.com
0.0.0.0 mathsolver.microsoft.com
0.0.0.0 microsoftedgetips.microsoft.com
0.0.0.0 microsoftedgewelcome.microsoft.com
0.0.0.0 microsoftnews.msn.com
0.0.0.0 mobile.events.data.microsoft.com
0.0.0.0 msedge.net
0.0.0.0 msft.sts.microsoft.com
0.0.0.0 msftncsi.com
0.0.0.0 msn.com
0.0.0.0 msntest.serving-sys.com
0.0.0.0 mwservice.xpay-int.microsoft.com
0.0.0.0 ntp.msn.com
0.0.0.0 nw-umwatson.events.data.microsoft.com
0.0.0.0 oca.telemetry.microsoft.com
0.0.0.0 oca.telemetry.microsoft.com.nsatc.net
0.0.0.0 officeapps.live.com
0.0.0.0 paymentinstruments.mp.microsoft.com
0.0.0.0 pptsgs.officeapps.live.com
0.0.0.0 pre.footprintpredict.com
0.0.0.0 preview.msn.com
0.0.0.0 pricelist.skype.com
0.0.0.0 privacy.microsoft.com
0.0.0.0 prod.rewardsplatform.microsoft.com
0.0.0.0 rad.live.com
0.0.0.0 rad.msn.com
0.0.0.0 redir.metaservices.microsoft.com
0.0.0.0 reports.wes.df.telemetry.microsoft.com
0.0.0.0 rewards.microsoft.com
0.0.0.0 s.gateway.messenger.live.com
0.0.0.0 s0.2mdn.net
0.0.0.0 sO.2mdn.net
0.0.0.0 schemas.microsoft.akadns.net
0.0.0.0 schemas.microsoft.com
0.0.0.0 sdx.microsoft.com
0.0.0.0 secure.adnxs.com
0.0.0.0 secure.flashtalking.com
0.0.0.0 self.events.data.microsoft.com
0.0.0.0 services.wes.df.telemetry.microsoft.com
0.0.0.0 settings-sandbox.data.microsoft.com
0.0.0.0 settings-win.data.microsoft.com
0.0.0.0 settings.data.microsof.com
0.0.0.0 settings.family.microsoft.com
0.0.0.0 signup.live.com
0.0.0.0 sls.update.microsoft.com.akadns.net
0.0.0.0 speech.platform.bing.com
0.0.0.0 spynet2.microsoft.com
0.0.0.0 spynetalt.microsoft.com
0.0.0.0 sqm.df.telemetry.microsoft.com
0.0.0.0 sqm.telemetry.microsoft.com
0.0.0.0 sqm.telemetry.microsoft.com.nsatc.net
0.0.0.0 ssw.live.com
0.0.0.0 static.2mdn.net
0.0.0.0 statsfe1.ws.microsoft.com
0.0.0.0 statsfe2.update.microsoft.com.akadns.net
0.0.0.0 statsfe2.ws.microsoft.com
0.0.0.0 support.microsoft.com
0.0.0.0 survey.watson.microsoft.com
0.0.0.0 telecommand.telemetry.microsoft.com
0.0.0.0 telecommand.telemetry.microsoft.com.nsatc.net
0.0.0.0 telemetry.appex.bing.net
0.0.0.0 telemetry.microsoft.com
0.0.0.0 telemetry.urs.microsoft.com
0.0.0.0 tip.customervoice.microsoft.com 
0.0.0.0 tokenization.cp.microsoft.com
0.0.0.0 ui.skype.com
0.0.0.0 v10.vortex-win.data.microsoft.com
0.0.0.0 vcservice.webxtsvc.microsoft.com
0.0.0.0 view.atdmt.com
0.0.0.0 view.officeapps.live.com
0.0.0.0 vortex-bn2.metron.live.com.nsatc.net
0.0.0.0 vortex-cy2.metron.live.com.nsatc.net
0.0.0.0 vortex-sandbox.data.microsoft.com
0.0.0.0 vortex-win.data.metron.live.com.nsatc.net
0.0.0.0 vortex-win.data.microsoft.com
0.0.0.0 vortex.data.glbdns2.microsoft.com
0.0.0.0 vortex.data.microsoft.com
0.0.0.0 watson.live.com
0.0.0.0 watson.microsoft.com
0.0.0.0 watson.ppe.telemetry.microsoft.com
0.0.0.0 watson.telemetry.microsoft.com
0.0.0.0 watson.telemetry.microsoft.com.nsatc.net
0.0.0.0 web.vortex-sandbox.data.msn.com
0.0.0.0 web.vortex.data.microsoft.com
0.0.0.0 web.vortex.data.msn.com
0.0.0.0 webxtsvc.microsoft.com
0.0.0.0 wes.df.telemetry.microsoft.com
0.0.0.0 win10.ipv6.microsoft.com
0.0.0.0 windows.msn.com
0.0.0.0 www.msftncsi.com
0.0.0.0 www.msn.com
0.0.0.0 xpay-int.microsoft.com
```

## 清除缓存的广告文件

修改完`hosts`文件后，遗留的旧广告仍然会出现的 Edge 浏览器的标签页中，下一步我们来删除浏览器中的缓存文件。

1. 删除缓存文件：在 Edge 浏览器中打开 `edge://settings/clearBrowserData`，勾选缓存图像和文件，然后点击删除
2. 清除DNS缓存：快捷键`Win+R`打开运行，输入`CMD`，打开命令提示符，输入`ipconfig /flushdns`后按回车
3. 重启浏览器：重启之后 Edge 浏览器的新标签页就看不到广告推送了

以上操作不会影响 Edge 浏览器正常工作，对网页访问速度和浏览器的更新无干扰。