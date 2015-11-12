---
layout: post
title: "光棍节我在学 pull request"
category:
tags: [collaboration, github]
---
{% include JB/setup %}


假如你是 [GitHub](https://github.com) 这个网站的用户，登录进去之后，你会发现，它页面顶部的菜单栏只显示三个东西，分别是 [Pull requests](https://github.com/pulls), [Issues](https://github.com/issues)，以及 [Gist](https://gist.github.com/)。后面两个其实都比较容易理解，分别是臭虫列表以及小代码分享，但 Pull request 这个功能却并不是那么直观，一看就懂。假如有一天你跨过了这个坎，看懂了 pull request，那么你就掌握了开源世界的入场券了。

我最早知道 [pull request](https://help.github.com/articles/using-pull-requests/) 是2011年的时候，那时候纯粹是出于好奇心，开始玩 github，也就造访一些比较知名的开源软件仓库而已。那时候 github 开始变得流行起来，经常在各种开源软件项目的网站上看得到 fork me on github 的标签，当时没有理解其意思，现在才明白，原来那是呼唤你去帮忙改善别人的代码啊！

那么我今天到底做了什么事情，才有了这个顿悟？

### pull request 是什么？

简而言之，pull request 就是你把别人的代码克隆到本地，然后加以完善之后，将完善后的代码推送给原作者，其实这个事情在 git 这个版本管理工具还没有被发明之前，主要是[通过电邮](https://twitter.com/RebeccaSlatkin/status/622112261293928449/photo/1)进行的，但 git 出现之后，一切都改变了。


我用笨方法把 [@Octocat](https://github.com/octocat/) 这个样板用户旗下的 [Spoon-Knife](https://github.com/octocat/Spoon-Knife) 仓库的 README 文件翻译成了中文，翻译完之后，才懂得为何开分支一定是叫 fork，而不是其他动词。

然后就非常干脆地将 Spoon-Knife 这个仓库 fork 到我自己的 GitHub 帐号底下，把我翻译好的[中文版 README](https://github.com/tonyyet/Spoon-Knife/) 取代了原先的英文版，然后 git add && git commit，再 git push 推送到 GitHub，这时候就可以去到我 fork 出来的这个代码仓库的网页上，找到其右侧的 pull request 按钮，点它，再按照画面指示来操作，就完成了我人生第一次 pull request!


完成了 pull request 的那一刻，我才真正明白，为何 GitHub 要大力推销自己是一个 social coding 之市集。

因为，对于程序员来讲，pull request 就是他们彼此之间打招呼最直接的方式。而且，成千上万的软件如今就是以这样一种方式通过类似 GitHub 那样的平台协作共创出来的。



### pull request 还能做什么？该怎么写？


假如你是一位老师，其实你可以考虑用 pull request 来收学生的作业。这是（[案例一](http://ivory.idyll.org/blog/2014-teaching-undergrads-with-github.html)，还有[案例二](http://blog.xdite.net/posts/2014/06/18/git-pull-request-homework)）

正是有了 pull request 这样的机制，程序员才有可能花更多的时间[离线工作](http://artsy.github.io/blog/2015/09/30/Work-Offline-More/)，而 GitHub 所提倡的[远程工作](zachholman.com/posts/how-github-works/)才能成为现实。

嗯，还有人直接用 pull request 来[求婚](https://twitter.com/kcimc/status/659812732569567232/photo/1)呢。当然，婚礼上的致词直接[以 pull request 来作为比喻](https://github.com/muan/wedding-party-speech/blob/master/speech-zh-cn.md)，也不奇怪了。



要知道怎样的 pull request 才是好的 pull request 吗？看看开源达人[@clkao](https://github.com/clkao)的 [pull request 记录](https://github.com/search?p=1&q=is%3Apr+author%3Aclkao&ref=searchresults&type=Issues&utf8=%E2%9C%93)的pull request 怎么写就知道了 :) 当然，像 pull request 这样重要的东西，GitHub 官方肯定也会提供[示范和指南](https://github.com/blog/1943-how-to-write-the-perfect-pull-request)的。假如你习惯使用命令行，你还可以直接[在命令行](https://sethvargo.com/checkout-a-github-pull-request/)进行 pull request 的操作。


当然，pull request 也[不是 GitHub 的原创](https://stackoverflow.com/questions/31648748/create-update-a-git-pull-request-from-command-line)，还有其他的代码托管平台也声称自己的 pull request 机制[做得更好](https://developer.atlassian.com/blog/2015/01/a-better-pull-request/)，但 GitHub 把这样一个行为发扬光大了，显然是值得大书特书。


### pull request 乃开源协作之精髓

通过 pull request，你可以[参与到各种开源项目](http://24pullrequests.com/contributing)当中，这实际上是很好的提升写代码能力，以及获得高手指点的一个途径。当然，你为开源项目贡献的代码或者文档越多，你在社区中的威望也会变得越高。台湾设计师 @muan 就是因为当年给 bootstrap [写的一个 pull request](http://muan.co/2015/05/12/first-pull-request/) 而被招进了 GitHub。开源硬件供应商SparkFun甚至[通过 pull request 来招人](https://github.com/sparkfun/hacker-application)！

GitHub 这家公司把 pull request 以及其他各种的异步沟通工具[玩到了极致](http://ben.balter.com/2014/11/06/rules-of-communicating-at-github/)，他们的官方博客就介绍过他们是[怎么用 pull request 来创造 GitHub](https://github.com/blog/1124-how-we-use-pull-requests-to-build-github) 的——也难怪他们的员工的快乐指数可以那么高！

---

假如你看完了这篇文章觉得意犹未尽，可以试一试 pull request。我新建了一个[与吃相关](https://github.com/tonyyet/recipes/)的代码仓库，要是你有兴趣，也欢迎[提交 pull request](https://github.com/tonyyet/recipes/pulls) :)

对了，明年2月27号是[「国际 Pull Request 日」](http://pullrequestday.com/)，现在就在自己的日历里记下这一天，到时用自己的闲暇时间为开源项目做点小贡献。


---

### 资源


- [GitHub 官方视频版的 Pull Request 介绍](https://www.youtube.com/watch?v=81uKcXZoQ2A)
- [How we use Pull Request to build GitHub](https://github.com/blog/1124-how-we-use-pull-requests-to-build-github)
- [Github School](https://github.com/githubschool)