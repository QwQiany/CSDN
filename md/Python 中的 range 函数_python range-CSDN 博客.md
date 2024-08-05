> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [blog.csdn.net](https://blog.csdn.net/fei347795790/article/details/129299464?ops_request_misc=&request_id=&biz_id=102&utm_term=python%20range&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-129299464.142^v100^pc_search_result_base4&spm=1018.2226.3001.4187)

哈喽兄弟们！今天我们聊聊 Python 中很重要的 range 对象！（本文章基于 Python3 环境，[Python2](https://so.csdn.net/so/search?q=Python2&spm=1001.2101.3001.7020) 环境下的 range 会有所不同，但并不影响我们使用）

一、range 对象是什么
-------------

每一个 Python 初学者都一定在开始学 Python 不久就一定会遇到”[range 函数](https://so.csdn.net/so/search?q=range%E5%87%BD%E6%95%B0&spm=1001.2101.3001.7020) “，大家都把他叫做 “range 函数”，是因为我们在用它的时候像调用函数一样，只需要给它传入参数，它就可以给出你想要的结果。这一点和函数是一样的，于是大家就习惯上把它叫做函数。但其实它并不是一个函数，因为它是惰性的，什么叫惰性的呢？给大家看看

```
print(range(1,3))    # 如果它是函数，得到的结果是0,1,2，然而
```

![](https://i-blog.csdnimg.cn/blog_migrate/c538364e2da0a1106a61d103b12ac7bb.png)

于是，大家恍然大悟，” 它是迭代器 “，一开始我也以为是，但是后面才知道，这家伙没那么简单，哪里不简单呢？我们来看看迭代器长啥样。比如迭代器 zip

![](https://i-blog.csdnimg.cn/blog_migrate/36073628761290b2e8ab85de832e6fd2.png)

并且种种表现也证明了它并不是一个迭代器，“迭代器是惰性的一次性可迭代对象”，也就是说，我们在迭代器是遍历一个元素就少一个，但是它不是，甚至，我们可以对它进行索引（jupyter notebook 环境）

![](https://i-blog.csdnimg.cn/blog_migrate/9743d524d13d5bd7773f9ebdc5f3e4bd.png)

那么，它到底是什么呢？如果实在要给它一个名字，可以称它为 “懒序列”，也就是说，实际上它就是列表元组集合一类的东西，然而，它比较” 懒“，那么什么叫懒呢？这里我需要讲一下。为了好理解，我用简单的例子比喻，我知道你们也不想看定义。

补充：

懒惰机制在计算机中就是说在为了缓解内存的压力，我们设置懒惰机制不要将计算的结果一次给出，而是在计算机使用者（可以是人也可以是其他机器）需要时再通过计算给出其需要的计算结果。现在再看看迭代器，实际上迭代器就是这样一个惰性机制。不会像列表这样的可迭代对象一次给出所有计算结果。range 对象也有这样的特性。

二、基本语法
------

实际上 range 对象是什么并不是那么的那么的重要，而怎样用它才是我们最应该重点关注的。基本语法

这是它的使用说明，如果看不懂没有关系！~看不懂才有我的用武之地~

![](https://i-blog.csdnimg.cn/blog_migrate/b62cb7d83ffe2d0e3b73f0dce016d6d3.png)

```
range(start,stop[,step])      # []代表不是必须
```

参数说明：

start 默认为 0，与 stop 配合使用，用来指定迭代范围的开始。

例如

迭代 range(5) 得到的是

0,1,2,3,4 表示从 0 到 4 start 和 stop 表示的范围规则：“前闭后开”（也就是说取不到 stop）

stop 与 start 配合使用，指定迭代范围的结束（并不包括 stop 本身）

例如

迭代 range(1,5) 得到的是

1,2,3,4 表示从 1 到 4

step 步长，默认为 1，表示迭代时的增量（或减量), 在使用 step 时必须要指定第一个参数 start

例如

迭代 range(1,5,2) ，得到

1,3 得到 1 和 3，并不会得到 5，因为 “前闭后开”，而步长为 2，代表取出规则是 “取一个元素跳过一个元素再接着取”

三、应用举例
------

简单知道 range 对象的语法以后，我们进行应用举例。

最常用组合 ----for 循环

我们在上面已经讲到 range 对象是一个 “懒序列”，那么通常我们需要将里面的元素取出来使用。因此，最常用的便是与 for 循环配合使用。直接上例子。

1、stop 指定范围结束，start 默认为 0，stop 步长默认为 1

```
for i in range(9):    # 此时9是stop，指定范围结束，start默认为0，stop步长默认为1
    print(i)
```

![](https://i-blog.csdnimg.cn/blog_migrate/2520b53d8ba20eecd05e5b6c10d578f7.png)

2、指定 start、stop，默认 stop

```
for i in range(2,9):   
    print(i)
```

![](https://i-blog.csdnimg.cn/blog_migrate/7d1c574a9ef56b3ff32c7df8f68bfcf0.png)

3、指定 stop，此时 start 和 stop 不能省略

```
for i in range(2,9,2):
    print(i)
```

![](https://i-blog.csdnimg.cn/blog_migrate/3c6bd20e281eaf2884dd0f7797c0b54b.png)

4、stop 为负数，此时 start 可以大于 stop，例如

```
for i in range(9,2,-2):   # 从9到2，步长为-2，没迭代一次增加-2，即下降2
    print(i)
```

![](https://i-blog.csdnimg.cn/blog_migrate/1f158a6eea020493242020c80e19734d.png)

思考：如果我们执行以下代码，能得到什么？，还是报错？

```
x for i in range(9,2):   
    print(i)
```

单独使用：

1、独自打印

![](https://i-blog.csdnimg.cn/blog_migrate/9ff4c0ceb1c2ade4f01d067d6d56f727.png)

2. 索引  
![](https://i-blog.csdnimg.cn/blog_migrate/d6669a3c20de35fc300558ce66a53273.png)

思考: 那么可以切片吗？如果可以，又会得到怎样的结果呢？

四、总结
----

1、range 对象的使用和理解都不难，但是在 python 的使用中非常常用！

2、range 对象既不是函数也不是迭代器，可以叫它 “懒序列”

3、参数解释：start 为范围开始，stop 为范围结束，stop 为步长

4、range 对象经常和 for 循环配合使用

5、可以对 range 对象进行索引

> 刚接触 Python 小伙伴，有什么不懂得都可以问我。  
> 我还准备了数百本电子书，大量的视频教程以及源代码，直接点文末名片领取。

好了，今天的内容就分享到这里，我们明天见！

如果对你有帮助，不要忘记分享给好朋友哦！关注我，防止错过更多内容！