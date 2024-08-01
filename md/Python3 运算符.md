> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/python3-basic-operators.html) [Python3 注释](https://www.runoob.com/python3/python3-comment.html "Python3 注释") [Python3 数字 (Number)](https://www.runoob.com/python3/python3-number.html "Python3 数字(Number)")

什么是运算符？
-------

本章节主要说明 Python 的运算符。

举个简单的例子:

```
4 + 5 = 9
```

例子中，**4** 和 **5** 被称为**操作数**，`+` 称为**运算符**。

Python 语言支持以下类型的运算符:

*   [算术运算符](#ysf1)
*   [比较（关系）运算符](#ysf2)
*   [赋值运算符](#ysf3)
*   [逻辑运算符](#ysf4)
*   [位运算符](#ysf5)
*   [成员运算符](#ysf6)
*   [身份运算符](#ysf7)
*   [运算符优先级](#ysf8)

接下来让我们一个个来学习 Python 的运算符。

Python 算术运算符
------------

以下假设变量 `a=10`，变量 `b=21`：

<table><tbody><tr><th>运算符</th><th>描述</th><th>实例</th></tr><tr><td>+</td><td>加 - 两个对象相加</td><td>a + b 输出结果 31</td></tr><tr><td>-</td><td>减 - 得到负数或是一个数减去另一个数</td><td>a - b 输出结果 -11</td></tr><tr><td>*</td><td>乘 - 两个数相乘或是返回一个被重复若干次的字符串</td><td>a * b 输出结果 210</td></tr><tr><td>/</td><td>除 - x 除以 y</td><td>b / a 输出结果 2.1</td></tr><tr><td>%</td><td>取模 - 返回除法的余数</td><td>b % a 输出结果 1</td></tr><tr><td>**</td><td>幂 - 返回 x 的 y 次幂</td><td>a**b 为 10 的 21 次方</td></tr><tr><td>//</td><td>取整除 - 往小的方向取整数</td><td><pre class="hljs cpp">&gt;&gt;&gt; 9//2
&gt;&gt;&gt; -9//2
-5</pre></td></tr></tbody></table>

以下实例演示了 Python 所有算术运算符的操作：

```
#!/usr/bin/python3
 
a = 21
b = 10
c = 0
 
c = a + b
print ("1 - c 的值为：", c)
 
c = a - b
print ("2 - c 的值为：", c)
 
c = a * b
print ("3 - c 的值为：", c)
 
c = a / b
print ("4 - c 的值为：", c)
 
c = a % b
print ("5 - c 的值为：", c)
 
# 修改变量 a 、b 、c
a = 2
b = 3
c = a**b 
print ("6 - c 的值为：", c)
 
a = 10
b = 5
c = a//b 
print ("7 - c 的值为：", c)
```

以上实例输出结果：

```
1 - c 的值为： 31
2 - c 的值为： 11
3 - c 的值为： 210
4 - c 的值为： 2.1
5 - c 的值为： 1
6 - c 的值为： 8
7 - c 的值为： 2
```

Python 比较运算符
------------

以下假设变量 a 为 10，变量 b 为 20：

<table><tbody><tr><th width="10%">运算符</th><th>描述</th><th>实例</th></tr><tr><td>==</td><td>等于 - 比较对象是否相等</td><td>(a == b) 返回 False。</td></tr><tr><td>!=</td><td>不等于 - 比较两个对象是否不相等</td><td>(a != b) 返回 True。</td></tr><tr><td>&gt;</td><td>大于 - 返回 x 是否大于 y</td><td>(a&gt; b) 返回 False。</td></tr><tr><td>&lt;</td><td>小于 - 返回 x 是否小于 y。所有比较运算符返回 1 表示真，返回 0 表示假。这分别与特殊的变量 True 和 False 等价。注意，这些变量名的大写。</td><td>(a &lt; b) 返回 True。</td></tr><tr><td>&gt;=</td><td>大于等于 - 返回 x 是否大于等于 y。</td><td>(a&gt;= b) 返回 False。</td></tr><tr><td>&lt;=</td><td>小于等于 - 返回 x 是否小于等于 y。</td><td>(a &lt;= b) 返回 True。</td></tr></tbody></table>

以下实例演示了 Python 所有比较运算符的操作：

```
#!/usr/bin/python3
 
a = 21
b = 10
c = 0
 
if ( a == b ):
   print ("1 - a 等于 b")
else:
   print ("1 - a 不等于 b")
 
if ( a != b ):
   print ("2 - a 不等于 b")
else:
   print ("2 - a 等于 b")
 
if ( a < b ):
   print ("3 - a 小于 b")
else:
   print ("3 - a 大于等于 b")
 
if ( a > b ):
   print ("4 - a 大于 b")
else:
   print ("4 - a 小于等于 b")
 
# 修改变量 a 和 b 的值
a = 5
b = 20
if ( a <= b ):
   print ("5 - a 小于等于 b")
else:
   print ("5 - a 大于  b")
 
if ( b >= a ):
   print ("6 - b 大于等于 a")
else:
   print ("6 - b 小于 a")
```

以上实例输出结果：

```
1 - a 不等于 b
2 - a 不等于 b
3 - a 大于等于 b
4 - a 大于 b
5 - a 小于等于 b
6 - b 大于等于 a
```

Python 赋值运算符
------------

以下假设变量 a 为 10，变量 b 为 20：

<table><tbody><tr><th>运算符</th><th>描述</th><th>实例</th></tr><tr><td>=</td><td>简单的赋值运算符</td><td>c = a + b 将 a + b 的运算结果赋值为 c</td></tr><tr><td>+=</td><td>加法赋值运算符</td><td>c += a 等效于 c = c + a</td></tr><tr><td>-=</td><td>减法赋值运算符</td><td>c -= a 等效于 c = c - a</td></tr><tr><td>*=</td><td>乘法赋值运算符</td><td>c *= a 等效于 c = c * a</td></tr><tr><td>/=</td><td>除法赋值运算符</td><td>c /= a 等效于 c = c / a</td></tr><tr><td>%=</td><td>取模赋值运算符</td><td>c %= a 等效于 c = c % a</td></tr><tr><td>**=</td><td>幂赋值运算符</td><td>c **= a 等效于 c = c ** a</td></tr><tr><td>//=</td><td>取整除赋值运算符</td><td>c //= a 等效于 c = c // a</td></tr><tr><td>:=</td><td>海象运算符，这个运算符的主要目的是在表达式中同时进行赋值和返回赋值的值。<strong>Python3.8 版本新增运算符</strong>。</td><td><p>在这个示例中，赋值表达式可以避免调用 len() 两次:</p><pre class="hljs python">if (n := len(a)) &gt; 10:
    print(f"List is too long ({n} elements, expected &lt;= 10)")</pre></td></tr></tbody></table>

以下实例演示了 Python 所有赋值运算符的操作：

```
#!/usr/bin/python3
 
a = 21
b = 10
c = 0
 
c = a + b
print ("1 - c 的值为：", c)
 
c += a
print ("2 - c 的值为：", c)
 
c *= a
print ("3 - c 的值为：", c)
 
c /= a 
print ("4 - c 的值为：", c)
 
c = 2
c %= a
print ("5 - c 的值为：", c)
 
c **= a
print ("6 - c 的值为：", c)
 
c //= a
print ("7 - c 的值为：", c)
```

以上实例输出结果：

```
1 - c 的值为： 31
2 - c 的值为： 52
3 - c 的值为： 1092
4 - c 的值为： 52.0
5 - c 的值为： 2
6 - c 的值为： 2097152
7 - c 的值为： 99864
```

在 Python 3.8 及更高版本中，引入了一种新的语法特性，称为 "海象运算符"（Walrus Operator），它使用 `:=` 符号。这个运算符的主要目的是在表达式中同时进行赋值和返回赋值的值。

使用海象运算符可以在一些情况下简化代码，尤其是在需要在表达式中使用赋值结果的情况下。这对于简化循环条件或表达式中的重复计算很有用。

下面是一个简单的实例，演示了海象运算符的使用：

```
# 传统写法
n = 10
if n > 5:
    print(n)

# 使用海象运算符
if (n := 10) > 5:
    print(n)
```

1.  `if (n := 10) > 5:`：这是使用海象运算符（`:=`）的写法。海象运算符在表达式中进行赋值操作。
    *   `(n := 10)`：将变量 `n` 赋值为 10，同时返回这个赋值结果。
    *   `> 5`：检查赋值后的 `n` 是否大于 5。如果条件为真，则执行接下来的代码块。
2.  `print(n)`：如果条件为真，打印变量 `n` 的值（即 10）。

**海象运算符的优点：**

*   海象运算符（`:=`）允许在表达式内部进行赋值，这可以减少代码的重复，提高代码的可读性和简洁性。
*   在上述例子中，传统写法需要单独一行来赋值 `n`，然后在 `if` 语句中进行条件检查。而使用海象运算符的写法可以在 `if` 语句中直接进行赋值和条件检查。

Python 位运算符
-----------

按位运算符是把数字看作二进制来进行计算的。Python 中的按位运算法则如下：

下表中变量 a 为 60，b 为 13 二进制格式如下：

```
a = 0011 1100

b = 0000 1101

-----------------

a&b = 0000 1100

a|b = 0011 1101

a^b = 0011 0001

~a  = 1100 0011
```

<table><tbody><tr><th>运算符</th><th>描述</th><th>实例</th></tr><tr><td>&amp;</td><td>按位与运算符：参与运算的两个值, 如果两个相应位都为 1, 则该位的结果为 1, 否则为 0</td><td>(a &amp; b) 输出结果 12 ，二进制解释： 0000 1100</td></tr><tr><td>|</td><td>按位或运算符：只要对应的二个二进位有一个为 1 时，结果位就为 1。</td><td>(a | b) 输出结果 61 ，二进制解释： 0011 1101</td></tr><tr><td>^</td><td>按位异或运算符：当两对应的二进位相异时，结果为 1</td><td>(a ^ b) 输出结果 49 ，二进制解释： 0011 0001</td></tr><tr><td>~</td><td>按位取反运算符：对数据的每个二进制位取反, 即把 1 变为 0, 把 0 变为 1。<code>~x</code> 类似于 <code>-x-1</code></td><td>(~a) 输出结果 -61 ，二进制解释： 1100 0011， 在一个有符号二进制数的补码形式。</td></tr><tr><td>&lt;&lt;</td><td>左移动运算符：运算数的各二进位全部左移若干位，由 "&lt;&lt;" 右边的数指定移动的位数，高位丢弃，低位补 0。</td><td>a &lt;&lt; 2 输出结果 240 ，二进制解释： 1111 0000</td></tr><tr><td>&gt;&gt;</td><td>右移动运算符：把 "&gt;&gt;" 左边的运算数的各二进位全部右移若干位，"&gt;&gt;" 右边的数指定移动的位数</td><td>a &gt;&gt; 2 输出结果 15 ，二进制解释： 0000 1111</td></tr></tbody></table>

以下实例演示了 Python 所有位运算符的操作：

```
#!/usr/bin/python3
 
a = 60            # 60 = 0011 1100 
b = 13            # 13 = 0000 1101 
c = 0
 
c = a & b        # 12 = 0000 1100
print ("1 - c 的值为：", c)
 
c = a | b        # 61 = 0011 1101 
print ("2 - c 的值为：", c)
 
c = a ^ b        # 49 = 0011 0001
print ("3 - c 的值为：", c)
 
c = ~a           # -61 = 1100 0011
print ("4 - c 的值为：", c)
 
c = a << 2       # 240 = 1111 0000
print ("5 - c 的值为：", c)
 
c = a >> 2       # 15 = 0000 1111
print ("6 - c 的值为：", c)
```

以上实例输出结果：

```
1 - c 的值为： 12
2 - c 的值为： 61
3 - c 的值为： 49
4 - c 的值为： -61
5 - c 的值为： 240
6 - c 的值为： 15
```

Python 逻辑运算符
------------

Python 语言支持逻辑运算符，以下假设变量 a 为 10, b 为 20:

<table><tbody><tr><th>运算符</th><th>逻辑表达式</th><th>描述</th><th>实例</th></tr><tr><td>and</td><td>x and y</td><td>布尔 "与" - 如果 x 为 False，x and y 返回 x 的值，否则返回 y 的计算值。</td><td>(a and b) 返回 20。</td></tr><tr><td>or</td><td>x or y</td><td>布尔 "或" - 如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值。</td><td>(a or b) 返回 10。</td></tr><tr><td>not</td><td>not x</td><td>布尔 "非" - 如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。</td><td>not(a and b) 返回 False</td></tr></tbody></table>

以上实例输出结果：

```
#!/usr/bin/python3
 
a = 10
b = 20
 
if ( a and b ):
   print ("1 - 变量 a 和 b 都为 true")
else:
   print ("1 - 变量 a 和 b 有一个不为 true")
 
if ( a or b ):
   print ("2 - 变量 a 和 b 都为 true，或其中一个变量为 true")
else:
   print ("2 - 变量 a 和 b 都不为 true")
 
# 修改变量 a 的值
a = 0
if ( a and b ):
   print ("3 - 变量 a 和 b 都为 true")
else:
   print ("3 - 变量 a 和 b 有一个不为 true")
 
if ( a or b ):
   print ("4 - 变量 a 和 b 都为 true，或其中一个变量为 true")
else:
   print ("4 - 变量 a 和 b 都不为 true")
 
if not( a and b ):
   print ("5 - 变量 a 和 b 都为 false，或其中一个变量为 false")
else:
   print ("5 - 变量 a 和 b 都为 true")
```

以上实例输出结果：

```
1 - 变量 a 和 b 都为 true
2 - 变量 a 和 b 都为 true，或其中一个变量为 true
3 - 变量 a 和 b 有一个不为 true
4 - 变量 a 和 b 都为 true，或其中一个变量为 true
5 - 变量 a 和 b 都为 false，或其中一个变量为 false
```

Python 成员运算符
------------

除了以上的一些运算符之外，Python 还支持成员运算符，测试实例中包含了一系列的成员，包括字符串，列表或元组。

<table><tbody><tr><th>运算符</th><th>描述</th><th>实例</th></tr><tr><td>in</td><td>如果在指定的序列中找到值返回 True，否则返回 False。</td><td>x 在 y 序列中 , 如果 x 在 y 序列中返回 True。</td></tr><tr><td>not in</td><td>如果在指定的序列中没有找到值返回 True，否则返回 False。</td><td>x 不在 y 序列中 , 如果 x 不在 y 序列中返回 True。</td></tr></tbody></table>

以下实例演示了 Python 所有成员运算符的操作：

```
#!/usr/bin/python3
 
a = 10
b = 20
list = [1, 2, 3, 4, 5 ]
 
if ( a in list ):
   print ("1 - 变量 a 在给定的列表中 list 中")
else:
   print ("1 - 变量 a 不在给定的列表中 list 中")
 
if ( b not in list ):
   print ("2 - 变量 b 不在给定的列表中 list 中")
else:
   print ("2 - 变量 b 在给定的列表中 list 中")
 
# 修改变量 a 的值
a = 2
if ( a in list ):
   print ("3 - 变量 a 在给定的列表中 list 中")
else:
   print ("3 - 变量 a 不在给定的列表中 list 中")
```

以上实例输出结果：

```
1 - 变量 a 不在给定的列表中 list 中
2 - 变量 b 不在给定的列表中 list 中
3 - 变量 a 在给定的列表中 list 中
```

Python 身份运算符
------------

身份运算符用于比较两个对象的存储单元

<table><tbody><tr><th width="10%">运算符</th><th>描述</th><th>实例</th></tr><tr><td>is</td><td>is 是判断两个标识符是不是引用自一个对象</td><td><strong>x is y</strong>, 类似 <strong>id(x) == id(y)</strong> , 如果引用的是同一个对象则返回 True，否则返回 False</td></tr><tr><td>is not</td><td>is not 是判断两个标识符是不是引用自不同对象</td><td><strong>x is not y</strong> ， 类似 <strong>id(x) != id(y)</strong>。如果引用的不是同一个对象则返回结果 True，否则返回 False。</td></tr></tbody></table>

**注：** [id()](/python/python-func-id.html) 函数用于获取对象内存地址。

以下实例演示了 Python 所有身份运算符的操作：

```
#!/usr/bin/python3
 
a = 20
b = 20
 
if ( a is b ):
   print ("1 - a 和 b 有相同的标识")
else:
   print ("1 - a 和 b 没有相同的标识")
 
if ( id(a) == id(b) ):
   print ("2 - a 和 b 有相同的标识")
else:
   print ("2 - a 和 b 没有相同的标识")
 
# 修改变量 b 的值
b = 30
if ( a is b ):
   print ("3 - a 和 b 有相同的标识")
else:
   print ("3 - a 和 b 没有相同的标识")
 
if ( a is not b ):
   print ("4 - a 和 b 没有相同的标识")
else:
   print ("4 - a 和 b 有相同的标识")
```

以上实例输出结果：

```
1 - a 和 b 有相同的标识
2 - a 和 b 有相同的标识
3 - a 和 b 没有相同的标识
4 - a 和 b 没有相同的标识
```

> is 与 == 区别：
> 
> is 用于判断两个变量引用对象是否为同一个， == 用于判断引用变量的值是否相等。
> 
> ```
> >>>a = [1, 2, 3]
> >>> b = a
> >>> b is a 
> True
> >>> b == a
> True
> >>> b = a[:]
> >>> b is a
> False
> >>> b == a
> True
> ```

Python 运算符优先级
-------------

以下表格列出了从最高到最低优先级的所有运算符， 相同单元格内的运算符具有相同优先级。 运算符均指二元运算，除非特别指出。 相同单元格内的运算符从左至右分组（除了幂运算是从右至左分组）：

<table><colgroup><col> <col> </colgroup><thead><tr><th><p>运算符</p></th><th><p>描述</p></th></tr></thead><tbody><tr><td><p><code>(expressions...)</code>,</p><p><code>[expressions...]</code>, <code>{key: value...}</code>, <code>{expressions...}</code></p></td><td><p>圆括号的表达式</p></td></tr><tr><td><p><code>x[index]</code>, <code>x[index:index]</code>, <code>x(arguments...)</code>, <code>x.attribute</code></p></td><td><p>读取，切片，调用，属性引用</p></td></tr><tr><td><p>await x</p></td><td><p>await 表达式</p></td></tr><tr><td><p><code>**</code></p></td><td><p>乘方 (指数)</p></td></tr><tr><td><p><code>+x</code>, <code>-x</code>, <code>~x</code></p></td><td><p>正，负，按位非 NOT</p></td></tr><tr><td><p><code>*</code>, <code>@</code>, <code>/</code>, <code>//</code>, <code>%</code></p></td><td><p>乘，矩阵乘，除，整除，取余</p></td></tr><tr><td><p><code>+</code>, <code>-</code></p></td><td><p>加和减</p></td></tr><tr><td><p><code>&lt;&lt;</code>, <code>&gt;&gt;</code></p></td><td><p>移位</p></td></tr><tr><td><p><code>&amp;</code></p></td><td><p>按位与 AND</p></td></tr><tr><td><p><code>^</code></p></td><td><p>按位异或 XOR</p></td></tr><tr><td><p><code>|</code></p></td><td><p>按位或 OR</p></td></tr><tr><td><p><code><code>in</code>,<code>not in</code>, <code>is</code>,<code>is not</code>, <code>&lt;</code>, <code>&lt;=</code>, <code>&gt;</code>, <code>&gt;=</code>, <code>!=</code>, <code>==</code></code></p></td><td><p>比较运算，包括成员检测和标识号检测</p></td></tr><tr><td><p><code><code>not x</code></code></p></td><td><p>逻辑非 NOT</p></td></tr><tr><td><p><code><code>and</code></code></p></td><td><p>逻辑与 AND</p></td></tr><tr><td><p><code><code>or</code></code></p></td><td><p>逻辑或 OR</p></td></tr><tr><td><p><code><code>if</code> -- <code>else</code></code></p></td><td><p>条件表达式</p></td></tr><tr><td><p><code><code>lambda</code></code></p></td><td><p>lambda 表达式</p></td></tr><tr><td><p><code>:=</code></p></td><td><p>赋值表达式</p></td></tr></tbody></table>

以下实例演示了 Python 所有运算符优先级的操作：

```
#!/usr/bin/python3
 
a = 20
b = 10
c = 15
d = 5
e = 0
 
e = (a + b) * c / d       #( 30 * 15 ) / 5
print ("(a + b) * c / d 运算结果为：",  e)
 
e = ((a + b) * c) / d     # (30 * 15 ) / 5
print ("((a + b) * c) / d 运算结果为：",  e)
 
e = (a + b) * (c / d)    # (30) * (15/5)
print ("(a + b) * (c / d) 运算结果为：",  e)
 
e = a + (b * c) / d      #  20 + (150/5)
print ("a + (b * c) / d 运算结果为：",  e)
```

以上实例输出结果：

```
(a + b) * c / d 运算结果为： 90.0
((a + b) * c) / d 运算结果为： 90.0
(a + b) * (c / d) 运算结果为： 90.0
a + (b * c) / d 运算结果为： 50.0
```

and 拥有更高优先级:

```
x = True
y = False
z = False
 
if x or y and z:
    print("yes")
else:
    print("no")
```

以上实例先计算 `y and z` 并返回 False ，然后 `x or False` 返回 True，输出结果：

```
yes
```

> **注意：**Python3 已不支持 `<>` 运算符，可以使用 `!=` 代替，如果你一定要使用这种比较运算符，可以使用以下的方式：
> 
> ```
> >>> from __future__ import barry_as_FLUFL
> >>> 1 <> 2
> True
> ```

```
x = True
y = False
z = False

if x or y and z:
    print("yes")
else:
    print("no")
```

```
x = True
y = False
z = False

if not x or y:
    print(1)
elif not x or not y and z:
    print(2)
elif not x or y or not y and x:
    print(3)
else:
    print(4)
```

[课后练习](#)

x 的 y 次方 (xy) 以下表达式正确的是?

*   [x^y](#)
*   [x**y](#)
*   [x^^y](#)
*   [Python 没有提到](#)

22 % 3 表达式输出结果为？

*   [7](#)
*   [1](#)
*   [0](#)
*   [5](#)

3*1**3 表达式输出结果为？

*   [27](#)
*   [9](#)
*   [3](#)
*   [1](#)

9//2 表达式输出结果为？

*   [1](#)
*   [2](#)
*   [3](#)
*   [4](#)

如果表达式的操作符有相同的优先级，则运算规则是？

*   [左到右](#)
*   [右到左](#)
*   [看心情](#)

```
x = True
y = False
z = False

if x or y and z:
    print("yes")
else:
    print("no")
```

以上代码输出结果为？

*   [yes](#)
*   [no](#)
*   [编译出错](#)

```
x = True
y = False
z = False

if not x or y:
    print(1)
elif not x or not y and z:
    print(2)
elif not x or y or not y and x:
    print(3)
else:
    print(4)
```

以上代码输出结果为？

*   [1](#)
*   [2](#)
*   [3](#)
*   [4](#)

[下一题](#)[完成](#)[重新测验](#)