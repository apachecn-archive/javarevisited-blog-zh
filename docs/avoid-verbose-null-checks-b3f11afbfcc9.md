# 避免显式空检查

> 原文：<https://medium.com/javarevisited/avoid-verbose-null-checks-b3f11afbfcc9?source=collection_archive---------0----------------------->

![](img/35bbe7dfa0b5365c4b9b0ba6330e8bbf.png)

阅读糟糕的代码最令人沮丧的事情之一是，你不得不在头脑中抛弃大量代码，只是为了找到相关的内容。在他的职业生涯中，谁没有至少一次发现一个充满重复的巨大方法，一个做不止一件事的样板？我可以谈论一整天的代码气味，但是今天我只想集中讨论一种非常主要的代码气味，它实际上比许多人认为的更容易避免。

**显式空值检查** 显式空值检查是对传入参数的空值验证，因为害怕出现[*NullPointerException*](https://www.java67.com/2021/05/how-to-solve-nullpointerexception-in-java.html)。这不是一个好的做法，因为它给你的代码增加了噪音，增加了代码阅读的难度，并且违反了 SRP( *S* [*单一责任原则*](https://javarevisited.blogspot.com/2017/04/single-responsibility-principle-example.html) )。让我们来看一个空值检查的例子。

有些人认为，“*但有时我别无选择，只能这样做。”。* 真的吗？让我展示一些可以根据具体情况使用的替代方案。

**什么都不做**
一种选择是什么都不做，这个函数的调用方，应该小心谨慎，确保不传递 null。但是如果他这样做了，并且这导致了一个[*NullPointerException*](https://javarevisited.blogspot.com/2013/05/ava-tips-and-best-practices-to-avoid-nullpointerexception-program-application.html#axzz6Kgpx2OGT)，这是一个知道函数被使用的方式是错误的好方法。而且我们调用的函数中的代码永远不应该返回 null。空检查不好，但返回空也同样不好。

被调用的函数可以做很多事情来避免返回 nul。如果异常出现，这至少会提示一个对话，关于什么是强制的，为什么不存在？也许需要对系统设计进行更多的思考。

**使用断言**
Java 关键字‘assert’可以与布尔表达式结合使用，通过抛出断言错误来停止程序执行。虽然这似乎是 if 语句的一个有趣的替代，但是在 java 中默认禁用[断言。对于那些想小心使用它们的人来说，它们是很好的调试工具。有时一些程序员会在修复 bug 时启用它们，但是在生产环境中它们总是被禁用。](https://javarevisited.blogspot.com/2012/01/what-is-assertion-in-java-java.html)

空对象模式
这种行为设计模式背后的思想是使用多态性来创建对象的空版本(M.Fowler 也称它们为缺失对象)。这些空对象将有一个名为`isNull()`的函数，它对于源类总是返回 false，但是对于空对象将返回 true。客户端将能够选择传递一个空对象而不是空值，这将避免在方法()中进行显式的空值检查。

最新版本的 java 有一个名为 [Optional](https://javarevisited.blogspot.com/2017/04/10-examples-of-optional-in-java-8.html#axzz6ccm5KWKs) 的类，可以用来避免返回空值。它基本上是空对象模式的一个实现。通过在客户端使用[可选的](https://www.java67.com/2018/06/java-8-optional-example-ispresent-orElse-get.html)，我们可以避免传递空值。

**验证器、IllegalArgumentException 和业务异常**
如果函数的调用者不在我们的控制范围内，并且我们不能确信将传递给我们函数的值，那么有其他替代空检查的方法，尽管也是防御性的，但可能对业务更友好，并且可能提供更多信息。

**验证器**
我在开头提到方法不应该有多重责任。如果出于某种原因，我们必须进行空检查或其他类型的验证，我们可以将它委托给一个验证器对象。

有时，这个验证器也不是一个平滑的解决方案，可能是类中不必要的依赖。可以使用装饰模式来替换它。基本上是一个包装被装饰对象调用的函数的包装器。关于装饰器设计模式的更多信息，在我之前写的这篇文章中:[https://medium . com/Java re visited/can-you-please-wrap-the-gift-it-is-for my-granth-1a 15da 02 f 60d](/javarevisited/can-you-please-wrap-the-gift-it-is-for-my-grandma-1a15da02f60d)

**非法参数异常** [*NullPointerException*](https://javarevisited.blogspot.com/2012/06/common-cause-of-javalangnullpointerexce.html)它对于客户端来说不是一个非常有用的异常。因此，如果我们决定不进行任何类型的空值检查，但我们仍然害怕空值，也许我们可以抛出一个 *IllegalArgumentException* 来代替。

捕捉运行时异常(又名吞咽异常)，因为如你所知，程序只是继续工作。强烈建议，如果你要做这样的事情，至少你要添加一个 *Logger.log()* 语句来帮助开发人员在出现问题时[调试](https://javarevisited.blogspot.com/2011/07/java-debugging-tutorial-example-tips.html#axzz6bYzaddcE)。

**业务异常**
正如我刚才在前面提到的，替代运行时异常不是一个值得捕捉的好东西。相反，我们可以使用业务/声明的异常，这将要求调用方函数做好准备(通过添加 try 和 catch 块..)查找潜在故障。

如您所见，除了显式空值检查，还有其他选择。空检查的主题很重要，因为作为干净的程序员和软件工匠，我们不仅要关心代码是否工作，还要关心它的可读性和可维护性。业界对 null 有很大的恐惧，这是有道理的，因为 null 会导致灾难性的灾难，但这并不意味着我们首先应该机械地执行冗长的 null 检查。

> 三思而后行

我希望你喜欢这篇文章，如果你喜欢，请鼓掌👏和/或在社交媒体上与您的朋友分享。