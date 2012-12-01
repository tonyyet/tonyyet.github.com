---
layout: post
title: "using punch to create static websites"
category: 
tags: []
---
{% include JB/setup %}

今天发现了一个静态网站建站神器，叫
[punch](https://github.com/laktek/punch)，它可以帮助你非常轻松的搭建起一个静态网站，而无需自己去写繁琐的html标签。最为特别的是，punch
支持
[mustache](mustache.github.com)，可以让你的代码看上去更加整洁。

看到这个工具貌似还不错，于是我就想试一试。结果发现，真的很简单，用punch建静态网站要比jekyll,
nanoc之类的简单轻松多了。我从熟悉这个工具到使用它来重新搭建
[TEDxGuangzhou](http://tedxguangzhou.com) 的网站，也才花了几个小时时间。

下面就简单的说一说怎么用这个工具吧。

先是下载：

1. 下载node.js:
http://nodejs.org/#download

2. 进入终端，通过npm安装punch:
npm install -g punch

3. 安装完毕之后，可以在终端输入：
punch
应该可以看到一些punch的相关命令项目提示，这就表明安装成功了。


下载安装好之后，你可以通过以下命令来创建一个静态网站：
punch setup mysite
而后cd到mysite的目录，这时候开启nodejs内置的服务器，就能在浏览器上看到新建的网站了：
cd mysite
punch s
这时候打开浏览器，在地址栏打”localhost:9009“就可以进入这个网站了。


* 使用

punch自身有一个非常吸引人的tutorial，只需打开网站即可看到。我就是看着这份tutorial把东西做出来的。
