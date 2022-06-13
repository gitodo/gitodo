+++
title = "Shopify店铺使用Cloudflare解析出现身份质询怎么办？"
date = "2022-06-11T11:14:34+08:00"
description = "Cloudflare 是一个网络工具，提供免费的 CDN 和域名解析服务。但有些Shopify店铺使用Cloudflare解析出现身份质询，严重影响网站体验。遇到这种情况怎么处理呢？是否需要取消Cloudflare解析？"

tags = ["Shopify",]
+++

Cloudflare 是一个网络工具，提供免费的 CDN 和域名解析服务。但有些Shopify店铺使用Cloudflare解析出现身份质询，严重影响网站体验。遇到这种情况怎么处理呢？是否需要取消Cloudflare解析？
<!--more-->

对于大多数网站来说，3分钟就可以解决，不管是Shopify网站还是Wordpress网站，调整后基本不会有任何不良影响。

### 使用Cloudflare解析后出现身份质询

使用Cloudflare解析后，访问Shopify网站出现错误提示，或者需要进行身份质询，例如：

* You are unable to access myshopify.com
* Checking your browser before accessing xxx
* One more step, please complete the security check to access xxx

![使用Cloudflare解析后出现身份质询](/images/2022/0611-使用Cloudflare解析后出现身份质询.png)

有些人发现Shopify网站出现了这类提示，然后把Cloudflare解析换掉后又恢复正常了。如果你的Shopify网站也出现了这类提示，并不是说Shopify网站出了Bug，也不意味着Shopify网站不能使用Cloudflare解析。

之所以出现这样的提示，确实是因为Cloudflare造成的。出于某种原因，例如你访问网站时开启了不安全的VPN等，Cloudflare对你的身份产生了怀疑，于是触发了对你的Shopify网站的保护机制。

上面的提示并不总是出现，可能很多粗心的卖家根本没有发现这个问题。而且即便是自己测试的时候没有遇到，也难以避免其他真实的买家遇到，这就非常影响店铺体验。试想，买家点击你发布的产品广告后，首先看到的是Cloudflare的身份质询页面，有多少人会选择停留或者配合完成质询呢？并且，人们通常会站在自己的角度考虑问题，所以当你的店铺访客看到Cloudflare的身份质询页面时，首先想到的肯定不是自己的身份出了问题，而是认为是你的店铺有问题，还会降低对店铺的信任度。

### 我的Shopify网站需要取消Cloudflare解析吗？

不用。

你的Shopify网站可以继续使用Cloudflare解析，只需修改Cloudflare解析中的【安全级别】即可，具体步骤如下：

1. 登录你的Cloudflare账户
2. 找到Shopify网站对应的域名
3. 点击域名后，选择【安全性】-【设置】
4. 修改【安全级别】调整您网站的安全级别，确定哪些访问者将收到质询页面
5. 将【安全级别】设置为“本质上为关”

![设置Cloudflare安全级别](/images/2022/0611-设置Cloudflare安全级别.png)

将Cloudflare中对应域名的【安全级别】设置为“本质上为关”后，再次访问你的Shopify网站，就不会出现身份质询了。

### 关闭后我的Shopify网站会不安全吗？

很安全。

你的店铺安全性在于Shopify网站的安全性，只要Shopify安全，你的店铺就安全，跟Cloudflare的设置无关。当然，前提是你没有使用一些破解的Shopify主题或者APP等。

类似于你使用Google邮箱，你用安全的方式使用就不可能被盗，否则就是Google邮箱系统出了问题。但如果你电脑有病毒，很可能你的所有账户都不安全。这时候Cloudflare的身份质询就类似于杀毒软件的功能，可以帮助你识别并杀死病毒，保护你电脑中记录的Google邮箱密码。

### 非Shopify店铺可以关闭Cloudflare身份质询吗？

可以放心关闭。

除非你被“仇家”盯上，一个小的电商网站基本上不用过分担心安全问题。一来攻击一个小网站根本无利可图，二来业内搭建网站的工具（例如Wordpress等）本身安全性已经做的很好，三来网站的服务器提供商也有一定的防御机制。

但总是有一些做坏事的人，对普遍存在的漏洞扫描，发现一批存在漏洞的网站。所以，如果你做的不及格，网站很可能就会牺牲品。反之，只要做到及格，即便不是那么优秀，也可以成功躲过。

有利于保护网站的基本操作包括：
1. 不使用任何破解主题或破解插件
2. 及时更新网站系统，例如Wordpress版本等
3. 只开放必要的服务器端口，例如22、80、443等
4. 不使用简单密码，例如123456等

类似的建议有很多，之所以称这些为及格操作，是因为这些设置都很简单，而且只需设置一次，省时省心。

除此之外，建议设置每周自动备份网站和对应的数据库。万一出了问题，可以快速恢复网站。