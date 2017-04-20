---
layout: post
title: CoX - 路在何方？
---


## CoX的原定方向

CoX作为一个外设标准，那么首先来探讨他的存在性或者关系或者价值：

### CoX & CooCox?

- CoX首先是组件平台的基石，或者一个外设标志是组件平台的基石
    + 如果没有一个标准，即使平台做起来，那么顶多也就是一个资源汇总的地方，他的质量等等，应该会比较普通，一个现实的例子：苹果自己的封闭系统，反而更容易搭建一个生态系统。
- CoX若能成为一个工业标准，那么可以提升CooCox在产业链的地位
- 从CoX研发的角度，也会省一些力气，不需要到处Port


### CoX & Cortex-M开发者

前提：CoX是一个标准，但是也是一个很好的库，应该主要是以下两个方面：

- 减少学习成本
    + 新芯片日新月异，无需跟着到处跑，一劳永逸
    + 在产品选型中，对单片机的熟悉程度已经可以不在是一个因素（目前，应该是很重要一点）
- 基于这个接口，大量可复用的Library, 当然也包含工程师自己先前项目积累的一些代码

> 移植：好像不是很重要，电子产品的生命周期一般都比较长，比如5年，十年（5年以后，这个产品还是否需要，5年以后，
> 这个公司是否还可以存在，CoX是否还存在），大家可能向后看的少，如果移植，大多应该是向前看。
> 
> - 什么时候需要移植：
>     + 半导体游说，你用我的芯片吧，我给一个很优惠的价钱 【前提你要是一个大客户】
>     + 芯片断货，或者很难购买，或者价钱变的不能接受 【比如AVR前面出现的一些状况】

### CoX & 半导体

- 小型半导体
    + 各大半导体的资源，可以共享
    + 大半导体的客户可以很平滑的过渡为他的客户
    + 更有利于打价格战

### CoX & ARM

- ARM应该也希望有一个标准，这有利于其整个生态的建设
- ARM更希望是自己出一个标准

### CoX & Driver芯片，模式商

- 一次开发，到处运行，他们应该会很喜欢

### CoX & 评估板商？

评估板主要是学习，他们更多的考虑开发者，开发者需要什么，他们准备什么

如果开发者觉得CoX好，他们会义无反顾的切换到CoX, 官方的除外。

做评估板的，就是墙头草。

## CoX原定的发展路线？

根据CoX的价值，那么怎么发展壮大，发展哪部分客户群呢？

- 半导体？ 
    + 小的半导体很欢迎，但是小的半导体的客户群相对较小，对CooCox的推广的价值应该有限，从推广上说，做3个小半导体，不如做1个大半导体。
    + 大半导体，更多的中立状态，不支持，不反对（拥抱第3方，又不想第3方太强大），另外一边去搭建自己的标准。
- 开发者
    + 这应该是重点目标，因为CoX可以实实在在的解决他们的问题
- 评估板
    + 当开发者喜欢CoX的时候，评估板也会拥抱CoX
    + 评估板也需差异化，CoX可以是他们差异化的开始
    + 如果CooCox有比较强的市场/商务能力，也可联合一个大的开发板商，共同推几种开发板，就类似 ST & mbed ==> Necleo, mbed & Seeed ==> xxx
- Driver芯片/Component
    + 他们会很欢迎，但是也是观望态度（自己根据标志开发或者付费）？
        * CoX是否被很多人认可？（用户群是否大）
        * 他们的客户需要什么？（比如需要STM32的Driver?）

结合以上几点，我们会发现，CooCox做为一个第3方，必须要走亲民道路，把这些程序员拿下，那么会很轻松的攻克 半导体，Driver芯片，开发板。

那么怎么去亲民？

- 第一点，我认为必须实实在在的解决开发者的问题，要达到减少学习成本：
    + 首先这是一个正在的可以商用的，工业级的
        * 接口全，如果没有接口定义的外设，也应该可以用（类似EBI这些，可以先当厂商库来做，如果这还不方便做，那么先给出来寄存器接口）
        * 应该先覆盖比较常见的几种MCU, 比如ST, Freescale, NXP(可以挑选库比较薄弱，但是MCU比较常见的开始，比如FSL)
- 第二点，需要把它当做开源项目来运作，而且要做活
    + 为什么大家信赖官方，而不信赖一些第3方，大家担心不长久，1年以后是否还存在？
    + 这是社区是否活跃？就是遇到问题，能不能很好的解决，他的路线是否清晰？他是否在不断的添加新功能
    + 占位符，怎么参与这个开源项目，从提交bug开始
- 第3点，配套要跟上
    + 文档，example
    + 上得厅堂，下得厨房，即可以编写MCU的基本应用，又可以跟OS,协议栈搭配的很好
- 第四点，引爆点（推广策略）
    + 比如借助CoX，才可以解决他们的问题？比如 UI？

## CooCox是怎么来运作CoX的？

- 初期爆发，定义了很多接口，接下来很长一段时间，没有了
    + 至今没有达到一个完整，好用的库的目标，仍然不完整
- Port了不少MCU,但都是冷门的（对于程序员民众来说，不是指出货量）
- CoX成了一个软件，有新版本就发布一下
- 希望靠Driver倒推，通过大量的Driver, 让大家喜欢上CoX, 用上CoX
    + Driver是有几百个了，但是质量，没有文档，很多直接Copy, 我们心里很明白，是否可以正在的用到产业上，不清楚
    + 几百个Driver，多数是比较平常的Driver, 可能不足与让他去改变一些东西
- 太默默无闻了，没有社区运营，更没有开源项目的运营
    + 没有Buglist
    + 没有Pull Request

## 新的挑战？

- ARM定义了CMSIS-DRIVER标准，他的目标是工业级的
    + ARM的标准之上向下推广，而且直接与厂商库结合，很平滑的过渡
    + 文档很齐全，对开发者（厂商，OS, 中间件），对使用者友好
    + 完整生态的一部分，CMSIS-Core, CMSIS-RTOS, CMSIS-Driver, 也很自然
- 半导体试图在自己的产品线推自己的标准，然后兼容CMSIS-Driver
    + NXP LPCOpen, 最早开始
    + ST Cube Library
    + Freescle 的Process Export其实也差不多

CoX vs CMSIS-Driver vs LPCOpen.. ?

## 方向，定位，调整

(时间不多，这里简写下)

关于CoX的发展，大家也考虑了很多，其中最大的一点是：

- 是否可以像cmsis-driver/mbed那样，直接基于厂商库定义标准？
    + 这样做，与cmsis-driver同质化了，那么与ARM/半导体正面竞争，会很惨
    + CMSIS-Driver, 还没有大规模应用，我们还有机会

方向基本不便，运营需要微调一下？

- 简化CoX, 干掉 MCU特有部分，仅保留CoX层
- 尽快在主流MCU实现最常见的接口，真正作为一个可用的库
- 我们需要把CoX当做一个社区开源项目来运营，引导大家参与进来
    + 更新Roadmap
    + 发issue
    + pull request
    + 制定规范
    + ...


## Reference

有两个帖子，用户对CMSIS-Driver的态度

- [Is the LPCWare CMSIS driver development now dead, as it seems all development work is on LPCOpen?](http://www.lpcware.com/zh-hans/content/forum/lpcware-cmsis-driver-development-now-dead-it-seems-all-development-work-lpcopen)
- [CMSIS Driver API and Software Packs status](http://community.arm.com/thread/4569)
