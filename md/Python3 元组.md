> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/python3-tuple.html) [Python3 列表](https://www.runoob.com/python3/python3-list.html "Python3 列表") [Python3 字典](https://www.runoob.com/python3/python3-dictionary.html "Python3 字典")

Python 的元组与列表类似，不同之处在于元组的元素不能修改。

元组使用小括号 `( )`，列表使用方括号 `[ ]`。

元组创建很简单，只需要在括号中添加元素，并使用逗号隔开即可。

![](https://www.runoob.com/wp-content/uploads/2016/04/tup-2020-10-27-10-26-2.png)

```
>>> tup1 = ('Google', 'Runoob', 1997, 2000)
>>> tup2 = (1, 2, 3, 4, 5 )
>>> tup3 = "a", "b", "c", "d"   #  不需要括号也可以
>>> type(tup3)
```

创建空元组

```
tup1 = ()
```

元组中只包含一个元素时，需要在元素后面添加逗号 `,` ，否则括号会被当作运算符使用：

```
>>> tup1 = (50)
>>> type(tup1)     # 不加逗号，类型为整型


>>> tup1 = (50,)
>>> type(tup1)     # 加上逗号，类型为元组
```

元组与字符串类似，下标索引从 0 开始，可以进行截取，组合等。

![](https://www.runoob.com/wp-content/uploads/2016/04/py-tup-10-26.png)

访问元组
----

元组可以使用下标索引来访问元组中的值，如下实例:

```
#!/usr/bin/python3
 
tup1 = ('Google', 'Runoob', 1997, 2000)
tup2 = (1, 2, 3, 4, 5, 6, 7 )
 
print ("tup1[0]: ", tup1[0])
print ("tup2[1:5]: ", tup2[1:5])
```

以上实例输出结果：

```
tup1[0]:  Google
tup2[1:5]:  (2, 3, 4, 5)
```

修改元组
----

元组中的元素值是不允许修改的，但我们可以对元组进行连接组合，如下实例:

```
#!/usr/bin/python3
 
tup1 = (12, 34.56)
tup2 = ('abc', 'xyz')
 
# 以下修改元组元素操作是非法的。
# tup1[0] = 100
 
# 创建一个新的元组
tup3 = tup1 + tup2
print (tup3)
```

以上实例输出结果：

```
(12, 34.56, 'abc', 'xyz')
```

删除元组
----

元组中的元素值是不允许删除的，但我们可以使用 del 语句来删除整个元组，如下实例:

```
#!/usr/bin/python3
 
tup = ('Google', 'Runoob', 1997, 2000)
 
print (tup)
del tup
print ("删除后的元组 tup : ")
print (tup)
```

以上实例元组被删除后，输出变量会有异常信息，输出如下所示：

```
删除后的元组 tup : 
Traceback (most recent call last):
  File "test.py", line 8, in <module>
    print (tup)
NameError: name 'tup' is not defined
```

元组运算符
-----

与字符串一样，元组之间可以使用 `+`、`+=`和 `*` 号进行运算。这就意味着他们可以组合和复制，运算后会生成一个新的元组。

<table><tbody><tr><th>Python 表达式</th><th>结果</th><th>描述</th></tr><tr><td><pre class="hljs">len((1, 2, 3))</pre></td><td>3</td><td>计算元素个数</td></tr><tr><td><pre class="hljs ruby">&gt;&gt;&gt; a = (1, 2, 3)
&gt;&gt;&gt; b = (4, 5, 6)
&gt;&gt;&gt; c = a+b
&gt;&gt;&gt; c
(1, 2, 3, 4, 5, 6)</pre></td><td>(1, 2, 3, 4, 5, 6)</td><td>连接，c 就是一个新的元组，它包含了 a 和 b 中的所有元素。</td></tr><tr><td><pre class="hljs ruby">&gt;&gt;&gt; a = (1, 2, 3)
&gt;&gt;&gt; b = (4, 5, 6)
&gt;&gt;&gt; a += b
&gt;&gt;&gt; a
(1, 2, 3, 4, 5, 6)</pre></td><td>(1, 2, 3, 4, 5, 6)</td><td>连接，a 就变成了一个新的元组，它包含了 a 和 b 中的所有元素。</td></tr><tr><td><pre class="hljs bash">('Hi!',) * 4</pre></td><td>('Hi!', 'Hi!', 'Hi!', 'Hi!')</td><td>复制</td></tr><tr><td><pre class="hljs bash">3 in (1, 2, 3)</pre></td><td>True</td><td>元素是否存在</td></tr><tr><td><pre class="hljs bash">for x in (1, 2, 3): 
    print (x, end=" ")</pre></td><td>1 2 3</td><td>迭代</td></tr></tbody></table>

元组索引，截取
-------

因为元组也是一个序列，所以我们可以访问元组中的指定位置的元素，也可以截取索引中的一段元素，如下所示：

元组：

```
tup = ('Google', 'Runoob', 'Taobao', 'Wiki', 'Weibo','Weixin')
```

![](https://www.runoob.com/wp-content/uploads/2016/04/py-tup-7.png)

<table><tbody><tr><th>Python 表达式</th><th>结果</th><th>描述</th></tr><tr><td>tup[1]</td><td>'Runoob'</td><td>读取第二个元素</td></tr><tr><td>tup[-2]</td><td>'Weibo'</td><td>反向读取，读取倒数第二个元素</td></tr><tr><td>tup[1:]</td><td>('Runoob', 'Taobao', 'Wiki', 'Weibo', 'Weixin')</td><td>截取元素，从第二个开始后的所有元素。</td></tr><tr><td>tup[1:4]</td><td>('Runoob', 'Taobao', 'Wiki')</td><td>截取元素，从第二个开始到第四个元素（索引为 3）。</td></tr></tbody></table>

运行实例如下：

```
>>> tup = ('Google', 'Runoob', 'Taobao', 'Wiki', 'Weibo','Weixin')
>>> tup[1]
'Runoob'
>>> tup[-2]
'Weibo'
>>> tup[1:]
('Runoob', 'Taobao', 'Wiki', 'Weibo', 'Weixin')
>>> tup[1:4]
('Runoob', 'Taobao', 'Wiki')
>>>
```

元组内置函数
------

Python 元组包含了以下内置函数

<table><tbody><tr><th>序号</th><th>方法及描述</th><th>实例</th></tr><tr><td>1</td><td>len(tuple)<br>计算元组元素个数。</td><td><pre class="hljs ruby">&gt;&gt;&gt; tuple1 = ('Google', 'Runoob', 'Taobao')
&gt;&gt;&gt; len(tuple1)
&gt;&gt;&gt;</pre></td></tr><tr><td>2</td><td>max(tuple)<br>返回元组中元素最大值。</td><td><pre class="hljs ruby">&gt;&gt;&gt; tuple2 = ('5', '4', '8')
&gt;&gt;&gt; max(tuple2)
'8'
&gt;&gt;&gt;</pre></td></tr><tr><td>3</td><td>min(tuple)<br>返回元组中元素最小值。</td><td><pre class="hljs ruby">&gt;&gt;&gt; tuple2 = ('5', '4', '8')
&gt;&gt;&gt; min(tuple2)
'4'
&gt;&gt;&gt;</pre></td></tr><tr><td>4</td><td>tuple(iterable)<br>将可迭代系列转换为元组。</td><td><pre class="hljs ruby">&gt;&gt;&gt; list1= ['Google', 'Taobao', 'Runoob', 'Baidu']
&gt;&gt;&gt; tuple1=tuple(list1)
&gt;&gt;&gt; tuple1
('Google', 'Taobao', 'Runoob', 'Baidu')</pre></td></tr></tbody></table>

### 关于元组是不可变的

所谓元组的不可变指的是元组所指向的内存中的内容不可变。

```
>>> tup = ('r', 'u', 'n', 'o', 'o', 'b')
>>> tup[0] = 'g'     # 不支持修改元素
Traceback (most recent call last):
  File "", line 1, in 
TypeError: 'tuple' object does not support item assignment
>>> id(tup)     # 查看内存地址
>>> tup = (1,2,3)
>>> id(tup)
4441088800    # 内存地址不一样了
```

从以上实例可以看出，重新赋值的元组 tup，绑定到新的对象了，不是修改了原来的对象。