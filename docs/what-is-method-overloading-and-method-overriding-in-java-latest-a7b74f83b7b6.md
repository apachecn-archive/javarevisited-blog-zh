# 什么是 Java 中的方法重载和方法重写？

> 原文：<https://medium.com/javarevisited/what-is-method-overloading-and-method-overriding-in-java-latest-a7b74f83b7b6?source=collection_archive---------9----------------------->

## 面向对象编程

## 关于多态性你只需要知道。

![](img/29e38ebb9ed3867db261ccc102fba581.png)

**un splash 上 Clément H 拍摄的照片**

多态是面向对象编程中的关键概念之一。通过这篇文章，我们将学习方法重载和重写。这是初学者被问得最多的面试问题之一。此外，我们将理解定义重载和重写的规则，以及每个 Java 开发人员都应该知道的重要的基调。

# 什么是方法重载？

1.方法重载意味着**一个类中有两个或更多的方法有相同的名字但是不同的参数(实参)。**

2.方法**可能有也可能没有不同的返回类型。**

3.**方法重载减少了重复代码**，并允许我们为不同的目的使用相同的方法名。

4.方法重载也称为**编译时多态性** *，因为在编译代码时，编译器会根据* ***方法名、返回类型和参数来决定要调用哪个方法。***

5.重载也可能发生在继承的情况下。这是因为子类 ***已经有了从父类*** 继承的方法的一个版本，并且还可以编写该方法的另一个重载版本。

# 方法重载的规则是什么？

1.方法必须有**相同的名字**但是**不同的方法签名**(不同数量的参数，不同类型的参数，不同的参数序列)。

2.重载方法**可能有也可能没有不同的返回类型。**

3.重载方法**可能有也可能没有不同的访问修饰符。**

4.重载方法**可能抛出不同的已检查或未检查异常。**

# 演示重载的示例程序:

在下面的程序中，我已经解释了**方法重载的概念。在阅读程序时，我建议阅读与代码相关的注释，以便更好地理解。**

方法重载的一个例子:

方法重载的一个例子

# 什么是方法重写？

1.方法覆盖是用已经写在父类中的**相同方法名和相同方法签名**在子类中定义一个方法。

2.**被覆盖方法的返回类型可以是父类方法的返回类型的子类型。**

例如，如果父类方法返回**车辆**，那么子类的被覆盖方法的返回类型可以是**车辆**类的任何子类，例如，**汽车**可以是子类中被覆盖方法的返回类型。(假设 Vehicle 为父类，Car 为 Vehicle 类的子类)。

3.它不能有更低的访问修饰符。

例如，如果父类方法有一个受保护的访问修饰符，那么子类重写的方法不能有私有的访问修饰符，但是允许公共的。

4.对被覆盖的方法使用 **@override annotation** ，这样如果我们不遵循覆盖规则，编译器就会显示错误。

5.方法覆盖被称为**动态多态*，因为要调用的方法是由 JVM 在运行时决定的。***

6.**静态方法不能被覆盖，**只有实例方法被覆盖。

# 关于方法重写，有几点需要记住:

1.只有继承的方法可以被重写。

2.不能重写构造函数和私有方法(仅对类可见)。

3.不能重写最终方法。

4.子类可以使用`**super.methodName()**`来调用被覆盖方法的超类版本。

# 演示覆盖的示例程序:

在下面的程序中，我已经解释了**方法覆盖。在阅读程序时，我再次建议阅读与代码相关的注释，以便更好地理解。**

重写的示例:

将车辆视为父类:

作为父类的车辆

继承父类的子类:

汽车作为子类

*本文到此为止。希望你喜欢这篇文章。*

# 您可以关注[维克拉姆·古普塔](https://medium.com/u/2c3b611409dc?source=post_page-----a7b74f83b7b6--------------------------------)了解类似内容。