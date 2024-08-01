> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/python3-number.html) [Python3 运算符](https://www.runoob.com/python3/python3-basic-operators.html "Python3 运算符") [Python3 字符串](https://www.runoob.com/python3/python3-string.html "Python3 字符串")

Python 数字数据类型用于存储数值。

数据类型是不允许改变的，这就意味着如果改变数字数据类型的值，将重新分配内存空间。

以下实例在变量赋值时 Number 对象将被创建：

```
var1 = 1
var2 = 10
```

您也可以使用 del 语句删除一些数字对象的引用。

del 语句的语法是：

```
del var1[,var2[,var3[....,varN]]]
```

您可以通过使用 del 语句删除单个或多个对象的引用，例如：

```
del var
del var_a, var_b
```

Python 支持三种不同的数值类型：

*   **整型 (int)** - 通常被称为是整型或整数，是正或负整数，不带小数点。Python3 整型是没有限制大小的，可以当作 Long 类型使用，所以 Python3 没有 Python2 的 Long 类型。布尔 (bool) 是整型的子类型。
    
*   **浮点型 (float)** - 浮点型由整数部分与小数部分组成，浮点型也可以使用科学计数法表示（2.5e2 = 2.5 x 102 = 250）
    
*   **复数 ((complex))** - 复数由实数部分和虚数部分构成，可以用 a + bj, 或者 complex(a,b) 表示， 复数的实部 a 和虚部 b 都是浮点型。
    

我们可以使用十六进制和八进制来代表整数：

```
>>> number = 0xA0F # 十六进制
>>> number

>>> number=0o37 # 八进制
>>> number
```

<table><tbody><tr><th>int</th><th>float</th><th>complex</th></tr><tr><td>10</td><td>0.0</td><td>3.14j</td></tr><tr><td>100</td><td>15.20</td><td>45.j</td></tr><tr><td>-786</td><td>-21.9</td><td>9.322e-36j</td></tr><tr><td>080</td><td>32.3e+18</td><td>.876j</td></tr><tr><td>-0490</td><td>-90.</td><td>-.6545+0J</td></tr><tr><td>-0x260</td><td>-32.54e100</td><td>3e+26J</td></tr><tr><td>0x69</td><td>70.2E-12</td><td>4.53e-7j</td></tr></tbody></table>

*   Python 支持复数，复数由实数部分和虚数部分构成，可以用 a + bj, 或者 complex(a,b) 表示， 复数的实部 a 和虚部 b 都是浮点型。

Python 数字类型转换
-------------

有时候，我们需要对数据内置的类型进行转换，数据类型的转换，你只需要将数据类型作为函数名即可。

*   **int(x)** 将 x 转换为一个整数。
    
*   **float(x)** 将 x 转换到一个浮点数。
    
*   **complex(x)** 将 x 转换到一个复数，实数部分为 x，虚数部分为 0。
    
*   **complex(x, y)** 将 x 和 y 转换到一个复数，实数部分为 x，虚数部分为 y。x 和 y 是数字表达式。
    

以下实例将浮点数变量 a 转换为整数：

```
>>> a = 1.0
>>> int(a)
```

Python 数字运算
-----------

Python 解释器可以作为一个简单的计算器，您可以在解释器里输入一个表达式，它将输出表达式的值。

表达式的语法很直白： `+`, `-`, `*` 和 `/`, 和其它语言（如 Pascal 或 C）里一样。例如：

```
>>> 2 + 2
>>> 50 - 5*6
>>> (50 - 5*6) / 4
5.0
>>> 8 / 5  # 总是返回一个浮点数
1.6
```

**注意：**在不同的机器上浮点运算的结果可能会不一样。

在整数除法中，除法 `/` 总是返回一个浮点数，如果只想得到整数的结果，丢弃可能的分数部分，可以使用运算符 `//` ：

```
>>> 17 / 3  # 整数除法返回浮点型
5.666666666666667
>>>
>>> 17 // 3  # 整数除法返回向下取整后的结果
>>> 17 % 3  # ％操作符返回除法的余数
>>> 5 * 3 + 2
```

**注意：**`//` 得到的并不一定是整数类型的数，它与分母分子的数据类型有关系。

```
>>> 7//2
>>> 7.0//2
3.0
>>> 7//2.0
3.0
>>>
```

等号 `=` 用于给变量赋值。赋值之后，除了下一个提示符，解释器不会显示任何结果。

```
>>> width = 20
>>> height = 5*9
>>> width * height
```

Python 可以使用 `**` 操作来进行幂运算：

```
>>> 5 ** 2  # 5 的平方
>>> 2 ** 7  # 2的7次方
```

变量在使用前必须先 "定义"（即赋予变量一个值），否则会出现错误：

```
>>> n   # 尝试访问一个未定义的变量
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'n' is not defined
```

不同类型的数混合运算时会将整数转换为浮点数：

```
>>> 3 * 3.75 / 1.5
7.5
>>> 7.0 / 2
3.5
```

在交互模式中，最后被输出的表达式结果被赋值给变量 **_** 。例如：

```
>>> tax = 12.5 / 100
>>> price = 100.50
>>> price * tax
12.5625
>>> price + _
113.0625
>>> round(_, 2)
113.06
```

此处， **_** 变量应被用户视为只读变量。

数学函数
----

<table><tbody><tr><th>函数</th><th>返回值 (描述)</th></tr><tr><td><a target="_blank" href="/python3/python3-func-number-abs.html" rel="noopener noreferrer">abs(x)</a></td><td>返回数字的绝对值，如 abs(-10) 返回 10</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-ceil.html" rel="noopener noreferrer">ceil(x)</a></td><td>返回数字的上入整数，如 math.ceil(4.1) 返回 5</td></tr><tr><td><p>cmp(x, y)</p></td><td>如果 x &lt;y 返回 -1, 如果 x == y 返回 0, 如果 x&gt; y 返回 1。 <strong>Python 3 已废弃，使用 (x&gt;y)-(x&lt;y) 替换</strong>。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-exp.html" rel="noopener noreferrer">exp(x)</a></td><td>返回 e 的 x 次幂 (e<sup>x</sup>), 如 math.exp(1) 返回 2.718281828459045</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-fabs.html" rel="noopener noreferrer">fabs(x)</a></td><td>以浮点数形式返回数字的绝对值，如 math.fabs(-10) 返回 10.0</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-floor.html" rel="noopener noreferrer">floor(x)</a></td><td>返回数字的下舍整数，如 math.floor(4.9) 返回 4</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-log.html" rel="noopener noreferrer">log(x)</a></td><td>如 math.log(math.e) 返回 1.0,math.log(100,10) 返回 2.0</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-log10.html" rel="noopener noreferrer">log10(x)</a></td><td>返回以 10 为基数的 x 的对数，如 math.log10(100) 返回 2.0</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-max.html" rel="noopener noreferrer">max(x1, x2,...)</a></td><td>返回给定参数的最大值，参数可以为序列。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-min.html" rel="noopener noreferrer">min(x1, x2,...)</a></td><td>返回给定参数的最小值，参数可以为序列。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-modf.html" rel="noopener noreferrer">modf(x)</a></td><td>返回 x 的整数部分与小数部分，两部分的数值符号与 x 相同，整数部分以浮点型表示。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-pow.html" rel="noopener noreferrer">pow(x, y)</a></td><td>x**y 运算后的值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-round.html" rel="noopener noreferrer">round(x [,n])</a></td><td><p>返回浮点数 x 的四舍五入值，如给出 n 值，则代表舍入到小数点后的位数。</p><p><strong>其实准确的说是保留值将保留到离上一位更近的一端。</strong></p></td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-sqrt.html" rel="noopener noreferrer">sqrt(x)</a></td><td>返回数字 x 的平方根。</td></tr></tbody></table>

随机数函数
-----

随机数可以用于数学，游戏，安全等领域中，还经常被嵌入到算法中，用以提高算法效率，并提高程序的安全性。

Python 包含以下常用随机数函数：

<table><tbody><tr><th>函数</th><th>描述</th></tr><tr><td><a target="_blank" href="/python3/python3-func-number-choice.html" rel="noopener noreferrer">choice(seq)</a></td><td>从序列的元素中随机挑选一个元素，比如 random.choice(range(10))，从 0 到 9 中随机挑选一个整数。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-randrange.html" rel="noopener noreferrer">randrange ([start,] stop [,step])</a></td><td>从指定范围内，按指定基数递增的集合中获取一个随机数，基数默认值为 1</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-random.html" rel="noopener noreferrer">random()</a></td><td>随机生成下一个实数，它在 [0,1) 范围内。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-seed.html" rel="noopener noreferrer">seed([x])</a></td><td>改变随机数生成器的种子 seed。如果你不了解其原理，你不必特别去设定 seed，Python 会帮你选择 seed。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-shuffle.html" rel="noopener noreferrer">shuffle(lst)</a></td><td>将序列的所有元素随机排序</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-uniform.html" rel="noopener noreferrer">uniform(x, y)</a></td><td>随机生成下一个实数，它在 [x,y] 范围内。</td></tr></tbody></table>

三角函数
----

Python 包括以下三角函数：

<table><tbody><tr><th>函数</th><th>描述</th></tr><tr><td><a target="_blank" href="/python3/python3-func-number-acos.html" rel="noopener noreferrer">acos(x)</a></td><td>返回 x 的反余弦弧度值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-asin.html" rel="noopener noreferrer">asin(x)</a></td><td>返回 x 的反正弦弧度值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-atan.html" rel="noopener noreferrer">atan(x)</a></td><td>返回 x 的反正切弧度值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-atan2.html" rel="noopener noreferrer">atan2(y, x)</a></td><td>返回给定的 X 及 Y 坐标值的反正切值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-cos.html" rel="noopener noreferrer">cos(x)</a></td><td>返回 x 的弧度的余弦值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-hypot.html" rel="noopener noreferrer">hypot(x, y)</a></td><td>返回欧几里德范数 sqrt(x*x + y*y)。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-sin.html" rel="noopener noreferrer">sin(x)</a></td><td>返回的 x 弧度的正弦值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-tan.html" rel="noopener noreferrer">tan(x)</a></td><td>返回 x 弧度的正切值。</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-degrees.html" rel="noopener noreferrer">degrees(x)</a></td><td>将弧度转换为角度, 如 degrees(math.pi/2) ， 返回 90.0</td></tr><tr><td><a target="_blank" href="/python3/python3-func-number-radians.html" rel="noopener noreferrer">radians(x)</a></td><td>将角度转换为弧度</td></tr></tbody></table>

数学常量
----

<table><tbody><tr><th>常量</th><th>描述</th></tr><tr><td>pi</td><td>数学常量 pi（圆周率，一般以π来表示）</td></tr><tr><td>e</td><td>数学常量 e，e 即自然常数（自然常数）。</td></tr></tbody></table>