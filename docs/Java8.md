<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# Java 8 新特性简介

> 原文：[https://zwmst.com/1196.html](https://zwmst.com/1196.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:43:02+08:00"> 2021-08-15 </time> ](https://zwmst.com/1196.html)  1.  代码更少（增加了新语法：Lambda 表达式）

2.  强大的 Stream API（集合数据的操作）

3.  最大化的减少空指针 异常：Optional 类 的使用

4.  接口的新特性

5.  注解的新特性

6.  集合的底层 源码实现

7.  新日期时间的 api*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# 抽象类和接口的异同？

> 原文：[https://zwmst.com/1198.html](https://zwmst.com/1198.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:43:14+08:00"> 2021-08-15 </time> ](https://zwmst.com/1198.html)  抽象类：含有 abstract 修饰符的 class 就算 抽象类；它既可以有抽象方法，也可以有 普通 方法，构造方法，静态方法，但是不能有抽象构造方法 和 抽象静态方法。且如果其子类没有实现 其所有的 抽象方法，那么该 子类 也必须是 抽象类； 接口：他可以看成是 抽象类的 一个特例，使用 interface 修饰符；

内部结构：

*   jdk7：接口只有常量和抽象方法，无构造器

*   jdk8：接口增加了 默认方法 和 静态方法，无构造器

*   jdk9：接口允许 以 private 修饰的方法，无构造器

共同点：

*   不能实例化；

*   多态方式的一种使用；

不同点：

*   抽象类是单继承的，而接口可以多继承（实现）；*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# Java8支持函数编程是什么意思？

> 原文：[https://zwmst.com/1200.html](https://zwmst.com/1200.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:43:25+08:00"> 2021-08-15 </time> ](https://zwmst.com/1200.html)  在Java 8之前，所有东西都是面向对象的。除了原语之外，java中的 所有内容都作为对象存 在。对方法/函数的所有调用都是使用对象或类引用进行的。

方法/功能本身并不是独立存在的。

使用Java 8，引入了函数式编程。所以我们可以使用匿名函数。Java是一种一流的面向对象语 言。除了原始数据类型之外，Java中的所有内容都是一个对象。即使是一个数组也是一个对 象。每个类都创建对象的实例。没有办法只定义一个独立于Java的函数/方法。无法将方法作 为参数传递或返回该实例的方法体。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# Java8中的可选项是什么？

> 原文：[https://zwmst.com/1202.html](https://zwmst.com/1202.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:43:35+08:00"> 2021-08-15 </time> ](https://zwmst.com/1202.html)  Java 8引入了一个新的容器类java.util.Optional 。如果该值可用，它将包装一个值。如果该 值不可用，则应返回空的可选项。因此它代表空值，缺失值。这个类有各种实用方法，如 isPresent（），它可以帮助用户避免使用空值检查。由于不直接返回值，而是返回包装器对 象，所以用户可以避免空指针异常。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# hashMap原理，java8做的改变

> 原文：[https://zwmst.com/1204.html](https://zwmst.com/1204.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:43:46+08:00"> 2021-08-15 </time> ](https://zwmst.com/1204.html)  从结构实现来讲，HashMap是数组+链表+红黑树（JDK1.8增加了红黑树部分）实现的。

HashMap最多只允许一条记录的键为null，允许多条记录的值为null。HashMap非线程安 全。ConcurrentHashMap线程安全。解决碰撞：当出现冲突时，运用拉链法，将关键词为同 义词的结点链接在一个单链表中，散列表长m，则定义一个由m个头指针组成的指针数组T， 地址为i的结点插入以T(i)为头指针的单链表中。Java8中，冲突的元素超过限制（8），用红 黑树替换链表。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# 解释Java8中间操作与终端操作？

> 原文：[https://zwmst.com/1206.html](https://zwmst.com/1206.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:43:56+08:00"> 2021-08-15 </time> ](https://zwmst.com/1206.html)  流操作可以分为两部分：

中间操作 -返回另一个Stream的中间操作，允许操作以查询的形式连接。

终端操作 -产生非流，结果如原始值，集合或根本没有值。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# 什么是Lambda表达式？

> 原文：[https://zwmst.com/1208.html](https://zwmst.com/1208.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:44:07+08:00"> 2021-08-15 </time> ](https://zwmst.com/1208.html)  Lambda Expression可以定义为允许用户将方法作为参数传递的匿名函数。这有助于删除大 量的样板代码。Lambda函数没有访问修饰符（私有，公共或受保护），没有返回类型声明和 没有名称。

Lambda表达式允许用户将“函数”传递给代码。所以，与以前需要一整套的接口/抽象类想 必，我们可以更容易地编写代码。例如，假设我们的代码具有一些复杂的循环/条件逻辑或工作 流程。使用lambda表达式，在那些有难度的地方，可以得到很好的解决。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# Lambda函数的优点

> 原文：[https://zwmst.com/1210.html](https://zwmst.com/1210.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:44:18+08:00"> 2021-08-15 </time> ](https://zwmst.com/1210.html)  直到Java 8列表和集合通常由客户端代码从集合中获取迭代器来处理，然后使用它迭代其元素 并依次处理每个元素。如果要并行处理不同的元素，那么客户代码而不是集合的责任就是组织 它。 通过Java 8，可以更轻松地在多个线程上分发集合的处理。 集合现在可以在内部组织自己 的迭代，将并行化的责任从客户端代码转移到库代码中。

更少的代码行。如上所述，用户必须仅以声明方式声明要执行的操作。 n > System.out.println（“Hello World”+ n）; 所以用户必须键入减少的代码量。

使用Java 8 Lambda表达式可以实现更高的效率。通过使用具有多核的CPU，用户可以通过使 用lambda并行处理集合来利用多核CPU。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# 什么是Java8中的MetaSpace？它与PermGen Space有何不同？

> 原文：[https://zwmst.com/1212.html](https://zwmst.com/1212.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:44:31+08:00"> 2021-08-15 </time> ](https://zwmst.com/1212.html)  使用JDK8时，permGen空间已被删除。那么现在将元数据信息存储在哪里？此元数据现在存 储在本机内存中，称为“MetaSpace”。该内存不是连续的Java堆内存。它允许通过垃圾收 集，自动调整，元数据并发解除分配来改进PermGen空间。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# 是什么使JavaSE8优于其他？

> 原文：[https://zwmst.com/1214.html](https://zwmst.com/1214.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:44:43+08:00"> 2021-08-15 </time> ](https://zwmst.com/1214.html)  Java SE 8具有以下功能，使其优于其他功能： 它编写并行代码。

它提供了更多可用的代码。它具有改进的性能应用程序。

它具有更易读和简 洁的代码。它支持编写包含促销的数据库。*
<!--yml
category: 未分类
date: 0001-01-01 00:00:00
-->

# Lambda表达式的参数列表与Lambda箭头运算符有何不同？

> 原文：[https://zwmst.com/1216.html](https://zwmst.com/1216.html)

   [ *Java8* ](https://zwmst.com/java8)*[ <time datetime="2021-08-15T10:44:53+08:00"> 2021-08-15 </time> ](https://zwmst.com/1216.html)  Lambda表达式可以一次携带零个，一个或甚至多个参数。另一方面，Lambda箭头运算符使 用图标“->”将这些参数从列表和主体中分离出来。*