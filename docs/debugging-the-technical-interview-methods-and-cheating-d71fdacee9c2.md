# 调试技术面试。方法和欺骗

> 原文：<https://medium.com/javarevisited/debugging-the-technical-interview-methods-and-cheating-d71fdacee9c2?source=collection_archive---------1----------------------->

![](img/2f55afaf3fe4236d9b5ce8f347c5adcc.png)

标题立刻引起了我的注意"[我震惊地发现一名候选人在网上面试中作弊](https://levelup.gitconnected.com/i-was-shocked-to-catch-a-candidate-cheating-in-an-online-interview-2441fef0ab4)"……你到底是怎么在面试中作弊的？[西哈诺·德·伯格拉克](https://en.wikipedia.org/wiki/Cyrano_de_Bergerac_(play)在镜头外小声回答了吗？

嗯，差不多了。这位候选人正在谷歌搜索答案，并把它们复制到一个共享屏幕上，假装这是他的代码。隐瞒这个就是撒谎。从来都不行。但这真的让我想起了几年前读过的一条推文，可惜我找不到了……它是这样的:

> *我妻子正在学习编程，并向我透露她在“作弊”。她用谷歌搜索她不知道的东西。我应该告诉她吗？*

这太棒了。

我们都知道作者的意思。我们一直都在谷歌上搜索编码。显然，有一种方法可以正确地做到这一点(特别是关于知识产权)，但是如果你测试的是谷歌可搜索的东西，那么你测试的是错误的技能。技术面试问题应该关注更相关的东西，而不是谷歌搜索。

在阅读了这些关于这个主题的文章后，我觉得我需要写一些自己的东西来反映我对一个好的技术面试的看法。

# 技术面试的目标是什么

当我进行技术面试时，我是在雇佣一个队友。这个队友应该是我想合作的人。因此，我关注:

*   显然，我不想雇用一个不可靠的人。说谎会立即被取消资格
*   没有现场编码测试
*   不，带回家练习
*   没有排名网站或黑客挑战
*   所有面试都是一对一的
*   让三个人单独进行一对一的面谈。达成共识
*   没有“让你思考”的难题

当我把这个告诉别人时，我的反应是“你到底在问什么”或者“为什么不是 X？”。我先从积极的方面开始，我问的问题…

# 调试作为一种技术面试技巧

我不在乎具体公司的编程经验。我在意的是编程经验，可以是在开源，大学或者其他地方。如果你做了任何真实世界的编程，那么你有错误，你处理它们。

那是编程。如果你不知道一门[编程语言](/javarevisited/top-5-programming-languages-for-mobile-app-development-in-2021-19a1778195b8)，你可以捡起来。如果你不知道一个库或 API，你可以学习它。但是调试和处理问题是一种通过实践培养的技能。

# 我遇到过的最难的技术面试问题

太阳微系统公司利用三名独立的工程师进行了采访。第三位， [Eran Davidov](/@erand) 问了我一个问题，这是我在技术面试中遇到的最难的问题之一。几年后，我问他这件事，他完全忘记了…

问题是:“告诉我你犯的一个错误，你是如何跟踪并修复它的？”。我开始告诉他我追踪到的一个 bug，他阻止了我。是你做的窃听器吗？

不，“我想听听你做的东西”。

我不怯场。我从不哑口无言。但我却一无所获。我坐在那里，唯一想到的错误是我花了两天时间寻找一个问题，因为一个`<`标志指向错误的方向……我不能告诉他！

最终，我不得不承认，我知道我要对虫子负责…但是我的大脑完全把它们从我的脑海中抹去了。尽管我明显过于自负，他还是推荐了我。至少他事先知道这件事。

# 伟大的技术性工作面试问题

基于此，以下是一些[最佳技术面试问题](/javarevisited/25-software-design-interview-questions-to-crack-any-programming-and-technical-interviews-4b8237942db0)，提问顺序不分先后:

**告诉我你最近热衷的一个项目**

我想要喜欢自己工作的人。我想让他们告诉我什么可行，什么不可行。他们可以做得更好的地方以及他们学到了什么。通过围绕这一点展开讨论，我需要形成一个项目的心理图像。

我喜欢看到人们在一个项目上“极客化”。如果他们没有，这是一个严重的警告信号。

告诉我你追踪的最后一个大 bug。你的流程是什么？

一个调试故事比其他任何东西都更能告诉我关于候选人的信息。人们可能在这里一无所获，或者可能需要一段时间才能找到一些东西，但这些都是引人入胜的故事，所以它们非常适合面试。

人们需要描述他们用来跟踪 bug 的工具和技术。那是你只有凭经验才能做到的事。

你如何实现类似 X 的东西？

当我在 [Lightrun](https://lightrun.com/) 面试时，他们问我如何为生产扩展一个特定的系统。我可以使用白板，但老实说，这在口头上也可以。做出架构决策，解释它们，然后根据额外的考虑进行调整…这是我们工作的核心。

你可以问几十个这样的问题……这样做的好处是，你甚至可以提前把它们交给候选人，他们可以有备而来。你仍然不会损失太多的价值。

# 代码呢？

读代码比写代码难多了。这就是为什么我认为编码问题完全是多余的。在这里，开源可以帮上忙。

我在最近的采访中做的一件事是这样的。我发了一个链接到一个开源库和一个问题。

**向我描述一下你将如何调试这个问题？**

然后我会口头指导他们完成这个过程，看看他们是否领会了我的意图。例如，我解释了用户点击某个东西而系统没有响应的情况。那么你会去哪里找呢？

显然，人们必须找到处理事件分派的部分，以便在那里放置一个断点。遵循这个思考过程很有启发性。远比冒泡排序更有价值。

# 为什么常见的技术面试问题是有问题的

所以是时候消极一点了。以前，我立刻抛弃了许多有缺陷的技术面试技巧。你最喜欢的可能就在那里，所以是时候解释为什么我不喜欢他们了。

我会跳过“不准说谎”的规则。我认为这很明显。但是其他的在这里。

# 没有现场编码测试

在日常生活中，我们花在调试和阅读代码上的时间比花在编码上的时间还要多。所以面试写代码是多余的。压力大，不怎么表现。

在白板或者外国电脑上做是最差的。

# 不，带回家练习

这太丢人了。从雇主那里拿到作业表明未来的雇员完全无视他们的时间。完成这项工作的人是:

*   绝望——我并不认为这是一种轻视。在一个不景气的市场中找到一份工作或第一份工作是很难的，如果这是雇主要求的话…但是即使你得到了这份工作，这也会留下不好的印象
*   可能会直接从网上抄袭

因此，你从中绝对得不到任何有价值的信息，并失去了潜在的优秀候选人，他们的雇主重视他们的时间。

# 没有排名网站或黑客挑战

这些网站过分看重像我这样社交范围更广的人。招聘的时候，你想对候选人进行“摇钱树”。你想要一个在非正式面试中看起来不怎么样，但却是一个很棒的候选人。我遇到过一些胆小的程序员，他们的社交足迹很小。但他们是了不起的程序员。

我在 stackoverflow 上有 50k，它主要说我回答了 3000 多个问题。这意味着我在那上面花了时间，并不是说我特别有天赋。

我认为这体现了我的职业道德和耐心。这些使我成为一个伟大的开发者拥护者。但是对于一个编程职位来说，这并不能真正说明我作为一名开发人员的技能。我的黑客排名也很高，因为我写了很多代码。但是我的经验是非常专业的，可能不适用于特定的工作。我也是真的贵…

最终，我认为这些网站是你可以考虑的一个小数据点。但对于编码或团队领导来说，它们不应该是主要因素。

# 所有面试都是一对一的

这不是我经历过的事情。但我听到人们(尤其是女性)抱怨说，当几个面试官用问题“轰炸”他们时，他们感觉“被联合起来了”。这很难。我们希望受访者感到自在。毕竟，如果我们喜欢他们，我们需要他们也喜欢我们。面试经历是招聘的第一步。

因此，我们希望一对一的过程有助于建立关系。这在以后招聘时会很有价值。

理想情况下，你需要不同的面试官来防止偏见进入面试过程。在小型创业公司在更广泛的人口统计中占有一席之地之前，这是很困难的。一旦你有了它，你需要把它整合到流程中。

# 让三个人单独进行一对一的面谈。达成共识

这种面试容易出错。我可以因为一个人的魅力、投射等形成对他的正面评价。当你和一个面试官使用这种方法时，你会得到有问题的结果。

力量在于人数和共识。魅力可能会愚弄一个人。一个人可能会错过一个有问题的迹象。但是三个人很难糊弄。

二是有问题的，如果他们不同意一个事实，没有人来平衡这一点。他们可能还是会漏掉一些东西。四个有点多了。他们可能会制造一种让受访者感到不舒服的情况。

没有“让你思考”的难题人们喜欢“为什么井盖是圆的”这类问题。我也真心喜欢他们。作为游戏。

他们会告诉我一个人是否能成为优秀的程序员吗？

绝对没有。

为什么不猎头国际象棋大师？

解决这些难题所需的技能是完全不同的。

那么为什么谷歌等公司还在做呢？

让招聘过程变得艰难。通过让在谷歌获得一份工作看起来“独一无二”且难以获得，你在你的公司周围创造了一种成就的氛围。这使得人们对成就的重视超过了它的实际价值。

所以我为什么不推荐这个呢？

因为我们不是谷歌。如果没有像这样的招聘过程，你只是有另一个过滤器，将优秀的候选人拒之门外。所有这些都是为了一个毫无意义的多余问题。一个不知名的主要组织可以发挥其虚构的“独家俱乐部”的优势。小公司在招聘时需要更多的个人接触(因此是一对一)。

# TL；速度三角形定位法(dead reckoning)

在技术面试中，不要:

*   做现场编码测试
*   带回家练习
*   使用排名网站或黑客挑战
*   集体面试
*   只有一两个人面试
*   使用难题

做:

*   问开放性问题
*   询问调试情况
*   询问激情和最近的项目
*   一对一面试
*   有三个面试官
*   支持多样性