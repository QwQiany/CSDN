> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/python3-string.html) [Python3 数字 (Number)](https://www.runoob.com/python3/python3-number.html "Python3 数字(Number)")[Python3 列表](https://www.runoob.com/python3/python3-list.html "Python3 列表")

字符串是 Python 中最常用的数据类型。我们可以使用引号 ( `'` 或 `"` ) 来创建字符串。

创建字符串很简单，只要为变量分配一个值即可。例如：

```
var1 = 'Hello World!'
var2 = "Runoob"
```

Python 访问字符串中的值
---------------

Python 不支持单字符类型，单字符在 Python 中也是作为一个字符串使用。

Python 访问子字符串，可以使用方括号 `[]` 来截取字符串，字符串的截取的语法格式如下：

```
变量[头下标:尾下标]
```

索引值以 **0** 为开始值，**-1** 为从末尾的开始位置。

![](https://static.jyshare.com/wp-content/uploads/123456-20200923-1.svg)

![](https://www.runoob.com/wp-content/uploads/2014/05/python-str-runoob.png)

如下实例：

```
#!/usr/bin/python3
 
var1 = 'Hello World!'
var2 = "Runoob"
 
print ("var1[0]: ", var1[0])
print ("var2[1:5]: ", var2[1:5])
```

以上实例执行结果：

```
var1[0]:  H
var2[1:5]:  unoo
```

Python 字符串更新
------------

你可以截取字符串的一部分并与其他字段拼接，如下实例：

```
#!/usr/bin/python3
 
var1 = 'Hello World!'
 
print ("已更新字符串 : ", var1[:6] + 'Runoob!')
```

以上实例执行结果

```
已更新字符串 :  Hello Runoob!
```

Python 转义字符
-----------

在需要在字符中使用特殊字符时，python 用反斜杠 `\` 转义字符。如下表：

<table><thead><tr><th width="8%">转义字符</th><th>描述</th><th>实例</th></tr></thead><tbody><tr><td>\(在行尾时)</td><td>续行符</td><td><pre class="hljs ruby">&gt;&gt;&gt; print("line1 \
... line2 \
... line3")
line1 line2 line3
&gt;&gt;&gt;</pre></td></tr><tr><td>\\</td><td>反斜杠符号</td><td><pre class="hljs python">&gt;&gt;&gt; print("\\")
\</pre></td></tr><tr><td>\'</td><td>单引号</td><td><pre class="hljs bash">&gt;&gt;&gt; print('\'')
'</pre></td></tr><tr><td>\"</td><td>双引号</td><td><pre class="hljs python">&gt;&gt;&gt; print("\"")
"</pre></td></tr><tr><td>\a</td><td>响铃</td><td><pre class="hljs python">&gt;&gt;&gt; print("\a")</pre>执行后电脑有响声。</td></tr><tr><td>\b</td><td>退格 (Backspace)</td><td><pre class="hljs python">&gt;&gt;&gt; print("Hello \b World!")
Hello World!</pre></td></tr><tr><td>\000</td><td>空</td><td><pre class="hljs ruby">&gt;&gt;&gt; print("\000")

&gt;&gt;&gt;</pre></td></tr><tr><td>\n</td><td>换行</td><td><pre class="hljs ruby">&gt;&gt;&gt; print("\n")


&gt;&gt;&gt;</pre></td></tr><tr><td>\v</td><td>纵向制表符</td><td><pre class="hljs ruby">&gt;&gt;&gt; print("Hello \v World!")
Hello 
       World!
&gt;&gt;&gt;</pre></td></tr><tr><td>\t</td><td>横向制表符</td><td><pre class="hljs ruby">&gt;&gt;&gt; print("Hello \t World!")
Hello &nbsp;&nbsp;&nbsp;&nbsp; World!
&gt;&gt;&gt;</pre></td></tr><tr><td>\r</td><td>回车，将 <code>\r</code> 后面的内容移到字符串开头，并逐一替换开头部分的字符，直至将 <code>\r</code> 后面的内容完全替换完成。</td><td><pre class="hljs python">&gt;&gt;&gt; print("Hello\rWorld!")
World!
&gt;&gt;&gt; print('google runoob taobao\r123456')
123456 runoob taobao</pre></td></tr><tr><td>\f</td><td>换页</td><td><pre class="hljs ruby">&gt;&gt;&gt; print("Hello \f World!")
Hello 
       World!
&gt;&gt;&gt;</pre></td></tr><tr><td>\yyy</td><td>八进制数，y 代表 0~7 的字符，例如：\012 代表换行。</td><td><pre class="hljs python">&gt;&gt;&gt; print("\110\145\154\154\157\40\127\157\162\154\144\41")
Hello World!</pre></td></tr><tr><td>\xyy</td><td>十六进制数，以 \x 开头，y 代表的字符，例如：\x0a 代表换行</td><td><pre class="hljs python">&gt;&gt;&gt; print("\x48\x65\x6c\x6c\x6f\x20\x57\x6f\x72\x6c\x64\x21")
Hello World!</pre></td></tr><tr><td>\other</td><td>其它的字符以普通格式输出</td><td>&nbsp;</td></tr></tbody></table>

使用 `\r` 实现百分比进度：

```
import time

for i in range(101):
    print("\r{:3}%".format(i),end=' ')
    time.sleep(0.05)
```

以下实例，我们使用了不同的转义字符来演示单引号、换行符、制表符、退格符、换页符、ASCII、二进制、八进制数和十六进制数的效果：

```
print('\'Hello, world!\'')  # 输出：'Hello, world!'

print("Hello, world!\nHow are you?")  # 输出：Hello, world!
                                        #       How are you?

print("Hello, world!\tHow are you?")  # 输出：Hello, world!    How are you?

print("Hello,\b world!")  # 输出：Hello world!

print("Hello,\f world!")  # 输出：
                           # Hello,
                           #  world!

print("A 对应的 ASCII 值为：", ord('A'))  # 输出：A 对应的 ASCII 值为： 65

print("\x41 为 A 的 ASCII 代码")  # 输出：A 为 A 的 ASCII 代码

decimal_number = 42
binary_number = bin(decimal_number)  # 十进制转换为二进制
print('转换为二进制:', binary_number)  # 转换为二进制: 0b101010

octal_number = oct(decimal_number)  # 十进制转换为八进制
print('转换为八进制:', octal_number)  # 转换为八进制: 0o52

hexadecimal_number = hex(decimal_number)  # 十进制转换为十六进制
print('转换为十六进制:', hexadecimal_number) # 转换为十六进制: 0x2a
```

Python 字符串运算符
-------------

下表实例变量 a 值为字符串 "Hello"，b 变量值为 "Python"：

<table><tbody><tr><th width="10%">操作符</th><th>描述</th><th width="20%">实例</th></tr><tr><td>+</td><td>字符串连接</td><td>a + b 输出结果： HelloPython</td></tr><tr><td>*</td><td>重复输出字符串</td><td>a*2 输出结果：HelloHello</td></tr><tr><td>[]</td><td>通过索引获取字符串中字符</td><td>a[1] 输出结果 <b>e</b></td></tr><tr><td>[:]</td><td>截取字符串中的一部分，遵循<strong>左闭右开</strong>原则，str[0:2] 是不包含第 3 个字符的。</td><td>a[1:4] 输出结果 <b>ell</b></td></tr><tr><td>in</td><td>成员运算符 - 如果字符串中包含给定的字符返回 True</td><td><b>'H' in a</b> 输出结果 True</td></tr><tr><td>not in</td><td>成员运算符 - 如果字符串中不包含给定的字符返回 True</td><td><b>'M' not in a</b> 输出结果 True</td></tr><tr><td>r/R</td><td>原始字符串 - 原始字符串：所有的字符串都是直接按照字面的意思来使用，没有转义特殊或不能打印的字符。 原始字符串除在字符串的第一个引号前加上字母 <code>r</code>（可以大小写）以外，与普通字符串有着几乎完全相同的语法。</td><td><pre class="hljs python">print( r'\n' )
print( R'\n' )</pre></td></tr><tr><td>%</td><td>格式字符串</td><td>请看下一节内容。</td></tr></tbody></table>

```
#!/usr/bin/python3
 
a = "Hello"
b = "Python"
 
print("a + b 输出结果：", a + b)
print("a * 2 输出结果：", a * 2)
print("a[1] 输出结果：", a[1])
print("a[1:4] 输出结果：", a[1:4])
 
if( "H" in a) :
    print("H 在变量 a 中")
else :
    print("H 不在变量 a 中")
 
if( "M" not in a) :
    print("M 不在变量 a 中")
else :
    print("M 在变量 a 中")
 
print (r'\n')
print (R'\n')
```

以上实例输出结果为：

```
a + b 输出结果： HelloPython
a * 2 输出结果： HelloHello
a[1] 输出结果： e
a[1:4] 输出结果： ell
H 在变量 a 中
M 不在变量 a 中
\n
\n
```

Python 字符串格式化
-------------

Python 支持格式化字符串的输出 。尽管这样可能会用到非常复杂的表达式，但最基本的用法是将一个值插入到一个有字符串格式符 %s 的字符串中。

在 Python 中，字符串格式化使用与 C 中 sprintf 函数一样的语法。

```
#!/usr/bin/python3
 
print ("我叫 %s 今年 %d 岁!" % ('小明', 10))
```

以上实例输出结果：

```
我叫 小明 今年 10 岁!
```

python 字符串格式化符号:

<table><tbody><tr><th>&nbsp;&nbsp;&nbsp; 符&nbsp;&nbsp; 号</th><th>描述</th></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %c</td><td>&nbsp;格式化字符及其 ASCII 码</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %s</td><td>&nbsp;格式化字符串</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %d</td><td>&nbsp;格式化整数</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %u</td><td>&nbsp;格式化无符号整型</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %o</td><td>&nbsp;格式化无符号八进制数</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %x</td><td>&nbsp;格式化无符号十六进制数</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %X</td><td>&nbsp;格式化无符号十六进制数（大写）</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %f</td><td>&nbsp;格式化浮点数字，可指定小数点后的精度</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %e</td><td>&nbsp;用科学计数法格式化浮点数</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %E</td><td>&nbsp;作用同 %e，用科学计数法格式化浮点数</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %g</td><td>&nbsp;%f 和 %e 的简写</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %G</td><td>&nbsp;%f 和 %E 的简写</td></tr><tr><td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; %p</td><td>&nbsp;用十六进制数格式化变量的地址</td></tr></tbody></table>

格式化操作符辅助指令:

<table><tbody><tr><th>符号</th><th>功能</th></tr><tr><td>*</td><td>定义宽度或者小数点精度</td></tr><tr><td>-</td><td>用做左对齐</td></tr><tr><td>+</td><td>在正数前面显示加号 (+)</td></tr><tr><td>&lt;sp&gt;</td><td>在正数前面显示空格</td></tr><tr><td>#</td><td>在八进制数前面显示零 ('0')，在十六进制前面显示'0x'或者'0X'(取决于用的是'x'还是'X')</td></tr><tr><td>0</td><td>显示的数字前面填充'0'而不是默认的空格</td></tr><tr><td>%</td><td>'%%'输出一个单一的'%'</td></tr><tr><td>(var)</td><td>映射变量 (字典参数)</td></tr><tr><td>m.n.</td><td>m 是显示的最小总宽度, n 是小数点后的位数 (如果可用的话)</td></tr></tbody></table>

Python2.6 开始，新增了一种格式化字符串的函数 [str.format()](/python/att-string-format.html)，它增强了字符串格式化的功能。

Python 三引号
----------

python 三引号允许一个字符串跨多行，字符串中可以包含换行符、制表符以及其他特殊字符。实例如下

```
#!/usr/bin/python3
 
para_str = """这是一个多行字符串的实例
多行字符串可以使用制表符
TAB ( \t )。
也可以使用换行符 [ \n ]。
"""
print (para_str)
```

以上实例执行结果为：

```
这是一个多行字符串的实例
多行字符串可以使用制表符
TAB (    )。
也可以使用换行符 [ 
 ]。
```

三引号让程序员从引号和特殊字符串的泥潭里面解脱出来，自始至终保持一小块字符串的格式是所谓的 WYSIWYG（所见即所得）格式的。

一个典型的用例是，当你需要一块 HTML 或者 SQL 时，这时用字符串组合，特殊字符串转义将会非常的繁琐。

```
errHTML = '''


ERROR

%s






'''
cursor.execute('''
CREATE TABLE users (  
login VARCHAR(8), 
uid INTEGER,
prid INTEGER)
''')
```

f-string
--------

f-string 是 python3.6 之后版本添加的，称之为字面量格式化字符串，是新的格式化字符串的语法。

之前我们习惯用百分号 (%):

```
>>> name = 'Runoob'
>>> 'Hello %s' % name
'Hello Runoob'
```

**f-string** 格式化字符串以 `f` 开头，后面跟着字符串，字符串中的表达式用大括号 {} 包起来，它会将变量或表达式计算后的值替换进去，实例如下：

```
>>> name = 'Runoob'
>>> f'Hello {name}'  # 替换变量
'Hello Runoob'
>>> f'{1+2}'         # 使用表达式
'3'

>>> w = {'name': 'Runoob', 'url': 'www.runoob.com'}
>>> f'{w["name"]}: {w["url"]}'
'Runoob: www.runoob.com'
```

用了这种方式明显更简单了，不用再去判断使用 %s，还是 %d。

在 Python 3.8 的版本中可以使用 `=` 符号来拼接运算表达式与结果：

```
>>> x = 1
>>> print(f'{x+1}')   # Python 3.6

>>> x = 1
>>> print(f'{x+1=}')   # Python 3.8
x+1=2
```

Unicode 字符串
-----------

在 Python2 中，普通字符串是以 8 位 ASCII 码进行存储的，而 Unicode 字符串则存储为 16 位 unicode 字符串，这样能够表示更多的字符集。使用的语法是在字符串前面加上前缀 **u**。

在 Python3 中，所有的字符串都是 Unicode 字符串。

Python 的字符串内建函数
---------------

Python 的字符串常用内建函数如下：

<table><tbody><tr><th>序号</th><th>方法及描述</th></tr><tr><td>1</td><td><p><a href="/python3/python3-string-capitalize.html">capitalize()</a><br>将字符串的第一个字符转换为大写</p></td></tr><tr><td>2</td><td><p><a href="/python3/python3-string-center.html">center(width, fillchar)</a></p>返回一个指定的宽度 width 居中的字符串，fillchar 为填充的字符，默认为空格。</td></tr><tr><td>3</td><td><p><a href="/python3/python3-string-count.html">count(str, beg= 0,end=len(string))</a></p><br>返回 str 在 string 里面出现的次数，如果 beg 或者 end 指定则返回指定范围内 str 出现的次数</td></tr><tr><td>4</td><td><p><a href="/python3/python3-string-decode.html">bytes.decode(encoding="utf-8", errors="strict")</a></p><br>Python3 中没有 decode 方法，但我们可以使用 bytes 对象的 decode() 方法来解码给定的 bytes 对象，这个 bytes 对象可以由 str.encode() 来编码返回。</td></tr><tr><td>5</td><td><p><a href="/python3/python3-string-encode.html">encode(encoding='UTF-8',errors='strict')</a></p><br>以 encoding 指定的编码格式编码字符串，如果出错默认报一个 ValueError 的异常，除非 errors 指定的是'ignore'或者'replace'</td></tr><tr><td>6</td><td><p><a href="/python3/python3-string-endswith.html">endswith(suffix, beg=0, end=len(string))</a><br>检查字符串是否以 suffix 结束，如果 beg 或者 end 指定则检查指定的范围内是否以 suffix 结束，如果是，返回 True, 否则返回 False。</p></td></tr><tr><td>7</td><td><p><a href="/python3/python3-string-expandtabs.html">expandtabs(tabsize=8)</a></p><br>把字符串 string 中的 tab 符号转为空格，tab 符号默认的空格数是 8 。</td></tr><tr><td>8</td><td><p><a href="/python3/python3-string-find.html">find(str, beg=0, end=len(string))</a></p><br>检测 str 是否包含在字符串中，如果指定范围 beg 和 end ，则检查是否包含在指定范围内，如果包含返回开始的索引值，否则返回 - 1</td></tr><tr><td>9</td><td><p><a href="/python3/python3-string-index.html">index(str, beg=0, end=len(string))</a></p><br>跟 find() 方法一样，只不过如果 str 不在字符串中会报一个异常。</td></tr><tr><td>10</td><td><p><a href="/python3/python3-string-isalnum.html">isalnum()</a></p><br>检查字符串是否由字母和数字组成，即字符串中的所有字符都是字母或数字。如果字符串至少有一个字符，并且所有字符都是字母或数字，则返回 True；否则返回 False。</td></tr><tr><td>11</td><td><p><a href="/python3/python3-string-isalpha.html">isalpha()</a></p><br>如果字符串至少有一个字符并且所有字符都是字母或中文字则返回 True, 否则返回 False</td></tr><tr><td>12</td><td><p><a href="/python3/python3-string-isdigit.html">isdigit()</a></p><br>如果字符串只包含数字则返回 True 否则返回 False..</td></tr><tr><td>13</td><td><p><a href="/python3/python3-string-islower.html">islower()</a></p><br>如果字符串中包含至少一个区分大小写的字符，并且所有这些 (区分大小写的) 字符都是小写，则返回 True，否则返回 False</td></tr><tr><td>14</td><td><p><a href="/python3/python3-string-isnumeric.html">isnumeric()</a></p><br>如果字符串中只包含数字字符，则返回 True，否则返回 False</td></tr><tr><td>15</td><td><p><a href="/python3/python3-string-isspace.html">isspace()</a></p><br>如果字符串中只包含空白，则返回 True，否则返回 False.</td></tr><tr><td>16</td><td><p><a href="/python3/python3-string-istitle.html">istitle()</a></p><br>如果字符串是标题化的 (见 title()) 则返回 True，否则返回 False</td></tr><tr><td>17</td><td><p><a href="/python3/python3-string-isupper.html">isupper()</a></p><br>如果字符串中包含至少一个区分大小写的字符，并且所有这些 (区分大小写的) 字符都是大写，则返回 True，否则返回 False</td></tr><tr><td>18</td><td><p><a href="/python3/python3-string-join.html">join(seq)</a></p><br>以指定字符串作为分隔符，将 seq 中所有的元素 (的字符串表示) 合并为一个新的字符串</td></tr><tr><td>19</td><td><p><a href="/python3/python3-string-len.html">len(string)</a></p><br>返回字符串长度</td></tr><tr><td>20</td><td><p><a href="/python3/python3-string-ljust.html">ljust(width[, fillchar])</a></p><br>返回一个原字符串左对齐, 并使用 fillchar 填充至长度 width 的新字符串，fillchar 默认为空格。</td></tr><tr><td>21</td><td><p><a href="/python3/python3-string-lower.html">lower()</a></p><br>转换字符串中所有大写字符为小写.</td></tr><tr><td>22</td><td><p><a href="/python3/python3-string-lstrip.html">lstrip()</a></p><br>截掉字符串左边的空格或指定字符。</td></tr><tr><td>23</td><td><p><a href="/python3/python3-string-maketrans.html">maketrans()</a></p><br>创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标。</td></tr><tr><td>24</td><td><p><a href="/python3/python3-string-max.html">max(str)</a></p><br>返回字符串 str 中最大的字母。</td></tr><tr><td>25</td><td><p><a href="/python3/python3-string-min.html">min(str)</a></p><br>返回字符串 str 中最小的字母。</td></tr><tr><td>26</td><td><p><a href="/python3/python3-string-replace.html">replace(old, new [, max])</a></p><br>把 将字符串中的 old 替换成 new, 如果 max 指定，则替换不超过 max 次。</td></tr><tr><td>27</td><td><p><a href="/python3/python3-string-rfind.html">rfind(str, beg=0,end=len(string))</a></p><br>类似于 find() 函数，不过是从右边开始查找.</td></tr><tr><td>28</td><td><p><a href="/python3/python3-string-rindex.html">rindex(str, beg=0, end=len(string))</a></p><br>类似于 index()，不过是从右边开始.</td></tr><tr><td>29</td><td><p><a href="/python3/python3-string-rjust.html">rjust(width,[, fillchar])</a></p><br>返回一个原字符串右对齐, 并使用 fillchar(默认空格）填充至长度 width 的新字符串</td></tr><tr><td>30</td><td><p><a href="/python3/python3-string-rstrip.html">rstrip()</a></p><br>删除字符串末尾的空格或指定字符。</td></tr><tr><td>31</td><td><p><a href="/python3/python3-string-split.html">split(str="", num=string.count(str))</a></p>以 str 为分隔符截取字符串，如果 num 有指定值，则仅截取 num+1 个子字符串</td></tr><tr><td>32</td><td><p><a href="/python3/python3-string-splitlines.html">splitlines([keepends])</a></p><br>按照行 ('\r', '\r\n', \n') 分隔，返回一个包含各行作为元素的列表，如果参数 keepends 为 False，不包含换行符，如果为 True，则保留换行符。</td></tr><tr><td>33</td><td><p><a href="/python3/python3-string-startswith.html">startswith(substr, beg=0,end=len(string))</a></p><br>检查字符串是否是以指定子字符串 substr 开头，是则返回 True，否则返回 False。如果 beg 和 end 指定值，则在指定范围内检查。</td></tr><tr><td>34</td><td><p><a href="/python3/python3-string-strip.html">strip([chars])</a></p><br>在字符串上执行 lstrip() 和 rstrip()</td></tr><tr><td>35</td><td><p><a href="/python3/python3-string-swapcase.html">swapcase()</a></p><br>将字符串中大写转换为小写，小写转换为大写</td></tr><tr><td>36</td><td><p><a href="/python3/python3-string-title.html">title()</a></p><br>返回 "标题化" 的字符串, 就是说所有单词都是以大写开始，其余字母均为小写 (见 istitle())</td></tr><tr><td>37</td><td><p><a href="/python3/python3-string-translate.html">translate(table, deletechars="")</a></p><br>根据 table 给出的表 (包含 256 个字符) 转换 string 的字符, 要过滤掉的字符放到 deletechars 参数中</td></tr><tr><td>38</td><td><p><a href="/python3/python3-string-upper.html">upper()</a></p><br>转换字符串中的小写字母为大写</td></tr><tr><td>39</td><td><p><a href="/python3/python3-string-zfill.html">zfill (width)</a></p><br>返回长度为 width 的字符串，原字符串右对齐，前面填充 0</td></tr><tr><td>40</td><td><p><a href="/python3/python3-string-isdecimal.html">isdecimal()</a></p>检查字符串是否只包含十进制字符，如果是返回 true，否则返回 false。</td></tr></tbody></table>