> * 原文地址：[So You Want to be a Functional Programmer (Part 1)](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-1-1f15e387e536#.4pbbhao8l)
* 原文作者：[Charles Scalfani](https://medium.com/@cscalfani)
* 译文出自：[掘金翻译计划](https://github.com/xitu/gold-miner)
* 译者：[cdpath](https://github.com/cdpath)
* 校对者：[luoyaqifei](https://github.com/luoyaqifei)， [DeadLion (Jasper Zhong)](https://github.com/DeadLion)

# 准备充分了嘛就想学函数式编程？（第一部分）


迈出理解函数式编程概念的第一步是最重要的，有时也是最难的一步。但是不一定特别难。只要选对了思考方法就不难。

#### 学开车

![](https://cdn-images-1.medium.com/max/1600/1*3aCyRpNew24v3PLXxu4VxQ.png)

第一次学车时，我们也曾挣扎过。看别人学开车时觉得真的很简单。但事实上学车比我们想象的难多了。

我们借父母的车子练习，在家周围街道上开熟练之前甚至都不敢冒险开到公路上去。

但是通过不断的练习，在经历过一些父母想忘掉的担心令人的经历之后，我们学会了开车，最终拿到了驾照。

拿到驾照之后我们一有机会就会把车开出去。每次出行都会让我们的技术越来越娴熟，信心也随之增长。终于有一天，我们必须开别人的车，或者自己的车最终报废了，只能买辆新的。

第一次开另一辆**不同的车**是什么感觉？和**第一次**开车的感觉相同吗？差得远呢。第一次开车时一切都是那么陌生。我们之前在车里待过，但只是个乘客。这一次我们可是在驾驶席上，掌控着一切。

但当我们开第二辆车时，我们只是简单问问自己几个问题就够了，比如钥匙怎么用，灯光在哪里，怎么用转向灯还有如何调整后视镜。

之后就顺利多了。但是为什么这次比起第一次要容易那么多？

这是因为这个新车和旧车基本上没什么区别。它们都有构成汽车的基本部件，而且都在差不多一样的地方。

新车有些部件的实现方式有些差异，也可能有了一些新功能，但是第一次，甚至第二次开的时候都不会用到这些功能。直到最后我们了解了所有的新功能。至少是那些我们觉得有用的功能。

其实学习编程语言的过程和学车有点类似。第一次是最难的。但是只要掌握了第一种语言，后面的都会轻松许多。

开始学第二门语言的时候，我们也只是问几个诸如「如何创建模块？如何搜索数组？子字符串的参数是什么？」之类的简单问题。

你有信心驾驭第二门语言，因为你觉得这就是旧语言加了一些新东西，学起来也就更轻松。

#### 初次驾驶宇宙飞船

![](https://cdn-images-1.medium.com/max/1600/1*ZLJIz9OrgCHCTST9KOcHIQ.png)

不管你这辈子开过一辆车还是十来量，想象一下你就要开宇宙飞船了。

要开宇宙飞船的话你就不能指望在路上开车的技术有什么用了，一切都要从零学起。（**我们可是程序员啊，我们从 0 开始计数。**）

开始练习之前我们要想到在太空中一切都不同了，要把这玩意开起来和在公路上开车可完全不同。

物理学倒是不会变。变的只是我们在这同一个宇宙中航行的方式。

学习函数式编程就是这样。一定要做好大部分东西都会改变的准备。而且已有的编程知识并**不会**有太大帮助。

编程就是思维方式，而函数式编程则是新的思维方式。习惯了这种新的思维方式之后你甚至可能没办法回到从前。

#### 忘了知道的一切

![](https://cdn-images-1.medium.com/max/1600/1*PoIg8NuGaH3XQkQ8Ctz6hw.png)

（说到函数式编程时，）人们喜欢说这句话，其实也有几分道理。**学习函数式编程就像从零学起。** 虽然不准确，但是不无道理。虽然函数式编程有许多类似的概念，但是最好还是让自己把**所有东西都重新学一遍**。

有了正确的思考方法就会有正确的预期，而预期对了就不会在遇到困难时轻言放弃。

许多在之前编程时习惯了的东西在函数式编程中都用不了了。

这就比如在开车时你已经习惯了倒车出库，但是开飞船的时候发现没有倒挡。这时候你会想了，「什么？没有倒挡？！没法儿倒车了我到底该怎么开？！」

好吧，其实开飞船的时候不需要倒挡，因为它是在三维空间中移动的。一旦了解了这一点，你就再也不会想什么倒挡了。事实上，总有一天你会回想起以前开车时的限制可真多啊。

> 学习函数式编程没那么快。所以别着急。

那么我们就离开寒冷的指令式编程世界，沉浸在函数式编程的温泉中吧。

这篇文章分为好几节，之后还介绍了一些函数式编程的概念，你可以在深入研究第一门函数式编程语言之前看看，会有帮助的。如果你已经开始着手学习了，它们也会帮助你加深理解。

务必不要心急。从这里开始慢慢地读，慢慢地理解示例代码。你甚至会想在读完每一节之后停顿一会儿，让自己充分领会，然后接着读下去。

最重要的是**理解**。

#### 纯粹

![](https://cdn-images-1.medium.com/max/1600/1*lHMDe_A2Cs_4InZ-E9Da9A.png)

函数式编程语言中的纯粹指的就是纯函数。

纯函数就是极简单的函数，只对输入参数起作用。

下面是 Javascript 中纯函数的例子：

    var z = 10;
    function add(x, y) {
        return x + y;
    }

注意，**add** 函数没有碰 **z** 变量。它即不读 **z** 也不写 **z**。它只是读了 **x** 和 **y** 参数，然后返回了两者的和。

这就是纯函数。如果 **add** 动了 **z** 变量，它就不再纯粹了。

下面是另一个例子：

    function justTen() {
        return 10;
    }

如果 **justTen** 是纯函数，它就**只能**返回一个常量。为什么呢？

因为我们还没有给它任何输入参数。如果是纯函数，它就不能存取自身的输入参数之外的任何东西，所以它只能返回一个常量。

既然无参数的纯函数什么都做不了，没什么用，还不如直接把 **justTen** 定义为一个常量。

> 大多数 **有用的** 纯函数至少要有一个参数。

思考一下这个函数：

    function addNoReturn(x, y) {
        var z = x + y
    }

注意，这个函数什么都没有返回。它把 **x** **y** 之和赋给了变量 z，但并没有返回 z。

这也是个纯函数，它只是处理了自身的参数。虽然有加法，但是没返回结果，所以也没用。

> **有用的**纯函数总要返回一些东西。

我们再回过头看看第一个 **add** 函数：

    function add(x, y) {
        return x + y;
    }
    console.log(add(1, 2)); // prints 3
    console.log(add(1, 2)); // still prints 3
    console.log(add(1, 2)); // WILL ALWAYS print 3

**add(1, 2)** 总是返回 **3**。结果不出所料，这毕竟是个纯函数。如果 **add** 函数用了其他外部值，就**没法**预测它的行为了。

> 纯函数对相同的输入总能产生相同的输出。

因为纯函数不能修改任何外部变量，下面这些函数都是**不纯粹的**。

    writeFile(fileName);
    updateDatabaseTable(sqlCmd);
    sendAjaxRequest(ajaxRequest);
    openSocket(ipAddress);

这些函数都有副作用。调用它们会修改文件和数据库的表，向服务器发送数据或者调用系统获取 socket。它们不仅处理输入参数并返回值，还做了其他事情。所以永远**无法**预测这些函数会返回什么。

> 纯函数**没有**副作用。

诸如 JavaScript, Java 和 C# 之类的指令式编程语言充斥着副作用。所以调试起来比较困难，毕竟变量有可能在**任何地方**遭到修改。如果遇到了因为变量被错误修改而导致的 bug，要从何看起呢？这一点都不好。

读到这里，你可能在想，「到底怎样才能用纯函数做任何事情呢？！」

函数式编程并不是只写纯函数。

函数式编程语言并不能彻底去除副作用，只能限制它们。因为函数总是要和现实世界打交道的，每个程序总有不纯粹的函数。而目标就是减少不纯粹代码的数量，并将它们和纯粹的代码隔离开来。

#### 不可变性

![](https://cdn-images-1.medium.com/max/1600/1*wKAhKZPXmcSwnq2AcLN-9Q.jpeg)

还记得是在啥时候第一次看到下面这些代码吗？

    var x = 1;
    x = x + 1;

还记得是谁叫你忘了在数学课上学到的东西吗？数学中的 **x** 永远不会等于 **x + 1**。

但是在指令式编程中，这段代码表示将 **x** 的当前值加 1 再**赋值回** **x**。

但是在函数式编程中 **x = x + 1** 是错误的。所以你得**记得**在数学课上**忘掉**了的东西…… 大致如此。

> 函数式编程中**没有**变量。

存储的值还是叫做变量，不过这是历史原因，它们其实是常量。比如一旦 **x** 有了一个值，这个变量就一直是这个值。

不要担心，**x** 通常是个局部变量，生命周期很短。但是只要它还在，值就不会变。

下面是个 Elm 中常变量的例子（Elm 是用于 Web 开发的纯函数编程语言）：

    addOneToSum y z =
        let
            x = 1
        in
            x + y + z

如果不熟悉 ML 风格的语法，我在这里解释一下。 **addOneToSum** 是个有两个参数（**y** 和 **z**）的函数。 

在 **let** 块中，**x** 绑定到的值是 **1**，所以它之后永远等于 **1**。函数退出，更准确地说是 **let** 块求值完之时，x 的生命周期才结束。

在 **in** 块中，计算过程中可以使用 **let** 块定义的值，即 **x**。**x + y + z** 的计算结果，更准确地说是 **1 + y + z** 的计算结果会被返回，因为 **x = 1**。

好吧，我听到你又问了一遍「到底怎样才能用纯函数做任何事情呢？！」

让我们想想何时需要修改变量。通常有两种情况：修改多个值（比如修改对象或 Record 中的值）和修改单一值（比如循环的计数器）。

函数式编程通过创建修改了值的 Record 副本来实现对 Record 中的值的修改。不过利用数据结构可以不必复制 Record 中的全部属性，十分高效。

函数式编程修改单一值也是通过创建副本实现的。

哦，对了。这样也**没有**用到循环。

「为什么没有变量和循环？！我讨厌你！！！」

等一下。这并不是说我们不能使用循环（我没有玩游戏文字），只是函数式编程语言没有像 **for**，**while**，**do** 以及 **repeat** 这样明确的循环结构而已。

> 函数式编程的循环用递归实现。

下面的代码展示了 Javascript 创建循环的两种方式：

    // simple loop construct
    var acc = 0;
    for (var i = 1; i <= 10; ++i)
        acc += i;
    console.log(acc); // prints 55

    // without loop construct or variables (recursion)
    function sumRange(start, end, acc) {
        if (start > end)
            return acc;
        return sumRange(start + 1, end, acc + start)
    }
    console.log(sumRange(1, 10, 0)); // prints 55

看看函数式编程中的递归是如何实现 **for** 循环的：就是用新起始值(**start + 1**)和新累积值(**acc + start**)不断地调用自身。它没有修改旧值，而是使用由旧值计算出来的新值。

不幸的是，即使学过一段时间 JavaScript 你也很难用到这种写法，原因有二。第一，JavaScript 语法很繁琐，第二是你可能不习惯递归式思考。

而 Elm 的写法更易读，也更易懂：

    sumRange start end acc =
        if start > end then
            acc
        else
            sumRange (start + 1) end (acc + start)

执行过程如下：

    sumRange 1 10 0 =      -- sumRange (1 + 1)  10 (0 + 1)
    sumRange 2 10 1 =      -- sumRange (2 + 1)  10 (1 + 2)
    sumRange 3 10 3 =      -- sumRange (3 + 1)  10 (3 + 3)
    sumRange 4 10 6 =      -- sumRange (4 + 1)  10 (6 + 4)
    sumRange 5 10 10 =     -- sumRange (5 + 1)  10 (10 + 5)
    sumRange 6 10 15 =     -- sumRange (6 + 1)  10 (15 + 6)
    sumRange 7 10 21 =     -- sumRange (7 + 1)  10 (21 + 7)
    sumRange 8 10 28 =     -- sumRange (8 + 1)  10 (28 + 8)
    sumRange 9 10 36 =     -- sumRange (9 + 1)  10 (36 + 9)
    sumRange 10 10 45 =    -- sumRange (10 + 1) 10 (45 + 10)
    sumRange 11 10 55 =    -- 11 > 10 => 55
    55

你可能认为 **for** 循环更好理解。这是有争议的，而且更多是因为我们更**熟悉** for 循环。这种非递归实现的循环需要可变变量，更糟糕。

我在这里没有讲完不可变性的全部好处，更多内容请参阅[为什么程序员需要限制]((https://medium.com/@cscalfani/why-programmers-need-limits-3d96e1a0a6db))一文中的**全局可变状态**一节。

不过一个显而易见的好处就是，如果对程序中的变量有访问权限，也只是只读权限，这也就是说，再也没人能改变这个值，哪怕是你自己。所以省去了很多意想不到的麻烦。

而且，如果是多线程程序，其他线程就无法干扰到当前线程。如果当前线程有一个常量而且其它线程试图改变它，其他线程只能用旧值复制一个新值出来。

在 90 世纪中期时，我写了[生化危机](https://www.youtube.com/watch?v=uIOYSjBRORM)游戏引擎，最大的 bug 源头就是各种多线程问题。我真希望自己那时候就知道不可变性。不过我那时候更应该担心 2 倍速和 4 倍速 CD-ROM 驱动在游戏渲染上的差异。

> 不可变性使代码更简单，安全。

#### 我的脑子！！！！

![](https://cdn-images-1.medium.com/max/1600/1*IK5485-iZaHeZRfP8aWmYg.png)

本部分到此结束。

在下一部分中我会继续介绍高阶函数，复合函数和柯里化等内容。

下一篇：[第二部分](https://github.com/xitu/gold-miner/blob/master/TODO/so-you-want-to-be-a-functional-programmer-part-2.md)
