---
layout: post
title: 码农的知识管理
---


## 什么是知识管理？

知识是一个笼统的说法，应该叫做档案，他的一个重要特点是可以保存下来，而且可以检阅。比如是公司项目的源码，我学习了一门编程语言，我谈成的客户信息，我知道怎么去报关等等，他是一种技能，经验，也是一个Guide, 指导我们朝着正确的方向去做事。

我认为的知识管理 是 把 知识 转变为 __经验__，这是一个累积的过程，由小变大的过程，逐步形成一个库。随后再需要用到的时候，再从这个__小库__里面调出来，而无需重复造轮子，无需在同一个地方摔第二次跟头。

知识管理在一个公司内，尤其重要，因为人是流动的，要做到铁打的营盘，流水的兵，就必须把个人的经验转变公司的经验，保存下来。

人脑很像是内存，时间久了，一些东西就容易忘记，所以，市面上出现了很多工具，比如各种备忘录，笔记本，博客，甚至存到了云端，再也不会丢失。

## 码农的知识管理是什么样的？

码农每天都在跟代码打交道，又不断需要学习各种不断更新的技术，具体：

- 代码在多数情况下，会显得晦涩难懂。
- 各种新的技术，层出不穷
- 一些技术，如果有一段时间没用，会马上变得生疏起来。
-  前辈分享的经验，要转变为自己的
-  别人的代码，转变未自己的
- 经常在同一个地方摔跤

程序员的知识库可能是：

- 一堆开源的代码, 或者Library, 或者一个领域的应用参考，后续希望能够使用上
- 一堆Guide, 各种指导，什么Linux Command Line, 什么编程指导，什么TCP IP
- 经验/教训/曾经犯过的错，走过的弯路，或者听到的，看到的

## 怎么样的知识管理，是好的知识管理？

知识只有经过整理，吸纳，才会变成自己的，如果仅仅是收藏(比如收藏到百度云，有道笔记)，这些可能永远也不会看到。

怎么整理？ 在我看来，需要整零结合：

- 一个特定的领域，比如如何学习Git, 那么最好的方式整理成一本书，有一个目录，把Git相关的东西整理到一个书中。但是这本书的章节是经过自己加工处理/吸纳的，不是简单的复制粘贴。
    + 那么到后来，需要用到这方面，也可以系统的根据目录从头看到尾，也可挑选自己需要了解的。
    + 很容易分享，这个经验，很方便变为公司的，或者其它人的
- 比较零散的，可使用wiki的形式，在需要的时候，可搜索出来。

那么推出我的方式：

__BOOK + WIKI__

## 一个新型的工具 GITBOOK ?

GITBOOK 结合了 BOOK , WIKI的优点， 他的特点在于：

- 首先他是一本书，他具有书的一切优点，比如是人工整理的，系统的知识
- 他具备WIKI的优点 - 协作，甚至比WIKi的协作还要好，他可以同时编辑
- 他具备WIKI的另一个优点 - 高质量， 发动社区的力量，总比1,2个人做出的东西更优
- 他有很多的表现手法，可以导出各种格式，比如PDF, ePub, Html等等

更多看：[GitBook官方](gitbook.io)

## 怎么管理 Library 和各种代码？

程序员现在都会使用SVN/HG/GIT 来管理代码，在开源盛行的时候，程序员很多时候，无需重复创造轮子，他山之石，可以攻玉。程序员的更多的需要去发现更多好用的，高质量的轮子，并把他收藏到自己的资料库中，但是代码通常是难懂的，没有文档的代码，更难使用，风险也很大。

那么怎么管理代码的文档呢？ 具有高质量文档的代码，将很容易用起来。


## 管理代码的文档

一个Active的软件项目，在不断的发展中，从0.1 到 1.0， 在到 3.0 . 代码与文档相比，代码永远是主体，文档永远是附属品，那么代码在不断的改进，文档也需要相应的同步改进。

会出现这样的问题：代码因为有各种测试，代码很稳定，标记为一个版本，但是文档因为没有一个严格的测试，而且也是一个精益求精的东西，所以文档很难定型。

建议的做法是：在新起一个版本的时候，创建一个先前版本的分支比如0.1，分支上文档，代码都可进行微调, 变成 0.1.2

### 小型的library

这种类型的代码比较简单，文档量不大，那么可以直接把文档 嵌入到 一个Git仓库中。

### 大中型的代码库/项目

文档单独出一个Git库，因为维护一个文档，也是需要很多的时间，和代码混在一起，实在太难维护。

当代码定义出一个版本的时候，文档库新定义一个分支出来，单独跟踪这个版本分支或者节点。


## 小结

其实我想说的是 知识管理 需要 从 先前 WIKI 转变为 WIKI + BOOK + 社区(团队/公司)协作的形式