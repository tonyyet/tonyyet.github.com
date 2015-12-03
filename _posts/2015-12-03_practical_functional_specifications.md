---
layout: post
title: "产品经理修炼（一）"
category:
tags: [product]
---
{% include JB/setup %}




最近开始做产品，学会了一个新名词，叫 PRD （其英文全称是 [Product requirements document](https://en.wikipedia.org/wiki/Product_requirements_document)），中文是「产品需求文档」。这东西看似神秘，但其实你搞懂了它的实质之后，也就懂得为何它可以是好玩的一个东西了。


为了搞清楚PRD是什么鬼玩意，我到 Duckduckgo 上面去搜，找到了 Quora 上面的[一个提问](https://www.quora.com/What-are-some-great-examples-of-product-requirement-documents-and-functional-specs?share=1)，其中有人提到了 [Joel Spolsky](http://www.joelonsoftware.com/AboutMe.html) 的文章，于是花了一个下午看完，并且摘要翻译了一下，对于产品新手来讲这太有用了。Joel 是 [Trello](https://trello.com) 联合创始人，也是 [Stack Exchange](http://stackexchange.com/) 的CEO，他的书也有被翻译成中文的，比如[《软件随想录》](http://book.douban.com/subject/4163938/)。

很多人尤其是工程师，会以为自己有个想法，然后马上写代码去实现，就能做出一个产品了。但 Joel 显然不同意这样的看法。他写了四篇博客文章来说明[为何写 spec 是如此重要](http://www.joelonsoftware.com/articles/fog0000000036.html)，我们也来学习一下吧。


## 什么是 spec？

所谓 spec，就是关于一个软件或网站或 app 的需求说明，基本上就是把你脑子里关于那个东西的想法付诸文字，而且包含各种可能出现的技术细节。其根本目的是帮程序员节省思考的时间。

Joel 在他的网站上给出了一个他自己写的 [spec 文档](http://www.joelonsoftware.com/RandomStuff/copilot_spec.pdf)，那是给 [CoPilot](http://copilot.com) 这个网站写的，大家不妨参考一下。



## 为啥写spec？

第一个原因是，花一个小时去写一个 spec，然后及早跟用户去沟通，了解他们是否真的需要某些功能，可以省去大量的沟通时间。因为假如你不写 spec 然后匆忙地做出产品才发现不符合用户需求，再急忙去改，可能会花掉你整整一周的时间。

第二个原因是，有了 spec，你跟项目相关的各种人沟通的时候，可以节省很多时间，大家一看 spec 就明白了，不需花费太多的唇舌。

第三个原因是，这对于制定时间表很有帮助。产品开发是需要钱的，应当在有限的时间内完成，及早交付，及早获得用户反馈，以及改良，而不是永无止境地进行开发。

写出好的 spec 也可以帮助你提前把可能会遇到的各种烦人的问题想到。比如，假如你要开发一个网站，有用户登录的功能，假如用户忘记密码的话，你会给用户发电邮让他完成密码重置。这电邮怎么写呢？难道让程序员去想？不，这个该由产品经理去想，邮件的那句话是不是可以写得更亲和一些，在写 spec 的时候就应该考虑到。




## 一份 spec 文档说明该包含什么？

- 免责声明，比如，明确地写清楚「此文档尚未完善」
- 作者，每份 spec 都应该有作者署名，并且只能有一位作者
- 用户使用场景，产品应当是为真实世界的用户而设计的，不是空想出来的
- 暂不考虑的目标，团队里大家都有自己关于产品的想法，但时间总是有限的，所以，那些太远大而且对当前用户需求关系不大的需求可以滞后，放到这一版块
- 全景图，假如我只有一分钟看这文档，我就看这里
- 细节分析，这是一份 spec 文档最重要的部分，就以一个网站的登录页面为例，就有很多要考虑的细节，这些都应该在这一部分给予说明
- 尚未明细的问题，第一版本的 spec 可以有一些尚待讨论的问题，但最好在开发开始之前就跟程序员沟通并且加以解决
- 注释，每份 spec 文档都有不同的读者，因此，最好是有一些注释的地方，让市场人员、工程人员都能够在文档里找到他们困惑的问题的解答
- spec 一定要是活的，不是写好就晾在那里的，要根据实际情况不断进行更新，并且最好有个共享的地址大家可以轻松地查找得到。




## 什么样的 spec 才是好的 spec？

### 第一，它应当是有趣的。

比较一下这两个 spec 文档：

A: 

> The user types Ctrl+N to create a new Employee table and starts entering the names of the employees.


B: 

> Miss Piggy, poking at the keyboard with a eyeliner stick because her chubby little fingers are too fat to press individual keys, types Ctrl+N to create a new Boyfriend table and types in the single record "Kermit."


很明显B比A有趣多了。

尝试写成B那种风格。


### 第二，用人话来写，不用写成只有电脑才看得懂的文档

还是先看两个例子：

A: 
> Assume a function AddressOf(x) which is defined as the mapping from a user x, to the RFC-822 compliant email address of that user, an ANSI string. Let us assume user A and user B, where A wants to send an email to user B. So user A initiates a new message using any (but not all) of the techniques defined elsewhere, and types AddressOf(B) in the To: editbox.



B: 
> Miss Piggy wants to go to lunch, so she starts a new email and types Kermit's address in the "To:" box. 

> Technical note: the address must be a standard Internet address (RFC-822 compliant.)



很明显，A例子只有程序员自己才能看得懂。但正常人的大脑是不愿意看这样的文档的，正常人的大脑更愿意看像B例子那样的文档。

### 第三，越简单越好。

简而言之，避免长句。

能用截图来说明的，尽量用截图。

### 第四，反复检查。

假如有文字或语法错误，马上改过来。

### 第五，忘记任何 spec 模板的想法吧。

spec 应当读起来跟读一篇漂亮的杂志文章一样，好的杂志文章是没有模板的，好的 spec 也不是从模板产生的。


## 阅读更多

- [Painless Functional Specifications](http://www.joelonsoftware.com/articles/fog0000000036.html)

- [如何成为产品经理](http://www.joelonsoftware.com/items/2009/03/09.html)

- [Joel 自己给出的 spec 示范](http://www.joelonsoftware.com/articles/AardvarkSpec.html)

