---
title: 如何将自己的域名绑定到 GitHub Pages上 (2019-12-11)
categories: GitHub
date: 2019-12-11 09:50:11
---
## 如何将自己的域名绑定到 GitHub Pages上 ## (2019-12-11)
    在做好自己的GitHub pages主页之后，接下来我们需要将自己的域名绑定（解析映射）到*username*.github.io，然而百度了很多教程，基本都过时或者方法不对，最新2019-12-11亲测可用方法如下：
    

 1. 创建好GitHub Pages后，你将可以使用 *username*.github.io访问你的主页。如果不知道如何创建自己的GitHub Pages，参考官方文档：https://pages.github.com/。主题可以选用Jekyll。
 2. 注册域名，阿里云，腾讯云都可，方法基本一致，注册后需要实名认证。
 3. 进入GitHub仓库Settings的Custom domain中将自己的域名save，Enforce Https可不勾选
 4. 域名解析，到域名控制台（阿里云，腾讯云，或者其他域名供应商）找到域名列表点击解析设置，很多人在这一步出错，或者设置完了但是访问不了（username.github.io 和 example.com都无法访问），有的旧教程里面各种ping主机，填IP，统统不需要。主机记录www和@是为了 www.example.com 和example.com 都能访问到你的页面。

         - 记录类型 主机记录    记录值
         - CNAME     www        username.github.io    
         - CNAME     @          username.github.io   
 5. 这个时候你会发现还是不能访问，因为在等服务商分配DNS（可能不止10分钟），这样配置准没错，去睡个觉醒来就能访问了




##参考资料： ##
https://blog.csdn.net/FlowerDance17/article/details/80685112