---
title: 功能全未必是好的解决方案 | 计算日子
date: 2019-08-20
---

这是一个普通得不能再普通的需求，去各大 APP 商店，搜索「倒数日」，都能找出一堆类似的 APP。

计算日期的功能不是一个刚性需求，可有可无，没有的话，其实没有什么大碍，有的话，也挺好玩，稍微设计一下，也是一个不错的小工具。

基于这样的目的，我就做了「计算日子」这个小工具，另外，还简单做了个分享卡片，如下图所示。

![](./_image/IMG_3101.JPG)
分享卡片

### 需求分析
纪念日的需求一直都存在，最初，我一直使用的「Days Matter」这款 APP，用了好多年，每次换机都必装，虽然使用频率不高，但作为一个工具，也实现了它的价值。

**字节加工厂**小程序里「计算日子」这个小工具，并不是为了将「Days Matter」这个 APP 复制到微信小程序中，而是从中提取出，我最需要的功能。

这类 APP 虽说叫「倒数日」，其实就是计算日期，距离过去某个日期有多少天？距离未来某个日期有多少天？

它的作用就是纪念过去，提醒未来。例如：生日、结婚纪念日、高考还剩多少天等，这么一说，关键的功能点就比较清晰了。

简单来说就是：列表，表单（添加/修改），分享卡片，提醒功能。如下图所示：

![](./_image/IMG_3100.JPG)
计算日子页面

### 进一步思考
完成上述的功能点，就实现了最基本的需求（计算日期）。添加一个标题，指定一个日期，就可以计算出距离现在的天数。

我老爸在试用的时候，我在一旁看着他，他把我老妈的出生日期、我的出生日期，以及他们的结婚纪念日，添加进去后，然后看着页面，很困惑的看着我，说道「为什么不显示生日还剩多少天？」

一下把我问懵了，页面上显示的，当然只有你添加的日期距离现在的天数呀，要是想显示还剩下多少天，那就得添加「下一个生日」的那个日期呀。

解释完，我就意识到问题所在了，这是产品的问题。「计算日期」的功能，在我看来就是冷冰冰的数字加减，你填入什么日期，后台计算出距离现在的天数，显示给你，你想要显示生日还剩多少天，就不是填出生日期，而是填写「下一个生日」的那个日期。

比如，我是 1989 年 5 月 3 日 出生，那么想显示我的生日还剩多少天，应该保存 2020 年 5 月 3 日，这样才对。当然过了一年，还得再保存一次。

这个操作就有点不友好了，那该怎么实现呢？

###  Days Matter 解决方案
下图是「Days Matter」这款 APP 的添加页面。

![](./_image/IMG_3169.jpg)
添加表单

它的实现方式是在表单中加入「重复」这个字段，而且重复的选项很多，非常全面。

![](./_image/IMG_3171.jpg)
重复可选项

如上图，分成两栏，左边「每x」一直到了「每999」，右边分为天、周、月以及年。所以，重复周期的跨度，从每天一直到了每 999 年，当然中间会有很多重复的，例如：每 7 天 = 每周。 

在我看来，这是典型的程序员思维，不管什么使用场景，我提供最全的功能，用户总能找到想要的。

**而产品思维是，在做每一个功能之前，都要去想，这个功能的实际使用场景是怎样的。**

从某种角度来说，功能全，未必是好的解决方案。因为提供最全的功能，意味着，你并不知道用户最想要的。

我设计了一个新的解决方案（当然也未必是好的）。由于线上版本还在审核中，姑且放到下一篇再讲吧。

未完。