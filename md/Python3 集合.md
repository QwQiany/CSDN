> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/python3-set.html) [Python3 字典](https://www.runoob.com/python3/python3-dictionary.html "Python3 字典") [Python3 条件控制](https://www.runoob.com/python3/python3-conditional-statements.html "Python3 条件控制")

集合（set）是一个无序的不重复元素序列。

集合中的元素不会重复，并且可以进行交集、并集、差集等常见的集合操作。

可以使用大括号 `{ }` 创建集合，元素之间用逗号 `,` 分隔， 或者也可以使用 `set()` 函数创建集合。

**创建格式：**

```
parame = {value01,value02,...}
或者
set(value)
```

以下是一个简单实例：

```
set1 = {1, 2, 3, 4}            # 直接使用大括号创建集合
set2 = set([4, 5, 6, 7])      # 使用 set() 函数从列表创建集合
```

**注意：**创建一个空集合必须用 `set()` 而不是 `{ }`，因为 `{ }` 是用来创建一个空字典。

更多实例演示：

```
>>> basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
>>> print(basket)                      # 这里演示的是去重功能
{'orange', 'banana', 'pear', 'apple'}
>>> 'orange' in basket                 # 快速判断元素是否在集合内
True
>>> 'crabgrass' in basket
False

>>> # 下面展示两个集合间的运算.
...
>>> a = set('abracadabra')
>>> b = set('alacazam')
>>> a                                  
{'a', 'r', 'b', 'c', 'd'}
>>> a - b                              # 集合a中包含而集合b中不包含的元素
{'r', 'd', 'b'}
>>> a | b                              # 集合a或b中包含的所有元素
{'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}
>>> a & b                              # 集合a和b中都包含了的元素
{'a', 'c'}
>>> a ^ b                              # 不同时包含于a和b的元素
{'r', 'd', 'b', 'm', 'z', 'l'}
```

类似列表推导式，同样集合支持集合推导式 (Set comprehension):

```
>>> a = {x for x in 'abracadabra' if x not in 'abc'}
>>> a
{'r', 'd'}
```

集合的基本操作
-------

### 1、添加元素

**语法格式如下：**

```
s.add( x )
```

将元素 x 添加到集合 s 中，如果元素已存在，则不进行任何操作。

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> thisset.add("Facebook")
>>> print(thisset)
{'Taobao', 'Facebook', 'Google', 'Runoob'}
```

还有一个方法，也可以添加元素，且参数可以是列表，元组，字典等，语法格式如下：

```
s.update( x )
```

x 可以有多个，用逗号分开。

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> thisset.update({1,3})
>>> print(thisset)
{1, 3, 'Google', 'Taobao', 'Runoob'}
>>> thisset.update([1,4],[5,6])  
>>> print(thisset)
{1, 3, 4, 5, 6, 'Google', 'Taobao', 'Runoob'}
>>>
```

### 2、移除元素

**语法格式如下：**

```
s.remove( x )
```

将元素 x 从集合 s 中移除，如果元素不存在，则会发生错误。

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> thisset.remove("Taobao")
>>> print(thisset)
{'Google', 'Runoob'}
>>> thisset.remove("Facebook")   # 不存在会发生错误
Traceback (most recent call last):
  File "", line 1, in 
KeyError: 'Facebook'
>>>
```

此外还有一个方法也是移除集合中的元素，且如果元素不存在，不会发生错误。格式如下所示：

```
s.discard( x )
```

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> thisset.discard("Facebook")  # 不存在不会发生错误
>>> print(thisset)
{'Taobao', 'Google', 'Runoob'}
```

我们也可以设置随机删除集合中的一个元素，语法格式如下：

```
s.pop()
```

```
thisset = set(("Google", "Runoob", "Taobao", "Facebook"))
x = thisset.pop()

print(x)
```

输出结果：

```
Runoob
```

多次执行测试结果都不一样。

set 集合的 pop 方法会对集合进行无序的排列，然后将这个无序排列集合的左面第一个元素进行删除。

### 3、计算集合元素个数

**语法格式如下：**

```
len(s)
```

计算集合 s 元素个数。

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> len(thisset)
```

### 4、清空集合

**语法格式如下：**

```
s.clear()
```

清空集合 s。

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> thisset.clear()
>>> print(thisset)
set()
```

### 5、判断元素是否在集合中存在

**语法格式如下：**

```
x in s
```

判断元素 x 是否在集合 s 中，存在返回 True，不存在返回 False。

```
>>> thisset = set(("Google", "Runoob", "Taobao"))
>>> "Runoob" in thisset
True
>>> "Facebook" in thisset
False
>>>
```

### 集合内置方法完整列表

<table><tbody><tr><th>方法</th><th>描述</th></tr><tr><td><a href="ref-set-add.html" target="_blank" rel="noopener noreferrer">add()</a></td><td>为集合添加元素</td></tr><tr><td><a href="ref-set-clear.html" target="_blank" rel="noopener noreferrer">clear()</a></td><td>移除集合中的所有元素</td></tr><tr><td><a href="ref-set-copy.html" target="_blank" rel="noopener noreferrer">copy()</a></td><td>拷贝一个集合</td></tr><tr><td><a href="ref-set-difference.html" target="_blank" rel="noopener noreferrer">difference()</a></td><td>返回多个集合的差集</td></tr><tr><td><a href="ref-set-difference_update.html" target="_blank" rel="noopener noreferrer">difference_update()</a></td><td>移除集合中的元素，该元素在指定的集合也存在。</td></tr><tr><td><a href="ref-set-discard.html" target="_blank" rel="noopener noreferrer">discard()</a></td><td>删除集合中指定的元素</td></tr><tr><td><a href="ref-set-intersection.html" target="_blank" rel="noopener noreferrer">intersection()</a></td><td>返回集合的交集</td></tr><tr><td><a href="ref-set-intersection_update.html" target="_blank" rel="noopener noreferrer">intersection_update()</a></td><td>返回集合的交集。</td></tr><tr><td><a href="ref-set-isdisjoint.html" target="_blank" rel="noopener noreferrer">isdisjoint()</a></td><td>判断两个集合是否包含相同的元素，如果没有返回 True，否则返回 False。</td></tr><tr><td><a href="ref-set-issubset.html" target="_blank" rel="noopener noreferrer">issubset()</a></td><td>判断指定集合是否为该方法参数集合的子集。</td></tr><tr><td><a href="ref-set-issuperset.html" target="_blank" rel="noopener noreferrer">issuperset()</a></td><td>判断该方法的参数集合是否为指定集合的子集</td></tr><tr><td><a href="ref-set-pop.html" target="_blank" rel="noopener noreferrer">pop()</a></td><td>随机移除元素</td></tr><tr><td><a href="ref-set-remove.html" target="_blank" rel="noopener noreferrer">remove()</a></td><td>移除指定元素</td></tr><tr><td><a href="ref-set-symmetric_difference.html" target="_blank" rel="noopener noreferrer">symmetric_difference()</a></td><td>返回两个集合中不重复的元素集合。</td></tr><tr><td><a href="ref-set-symmetric_difference_update.html" target="_blank" rel="noopener noreferrer">symmetric_difference_update()</a></td><td>移除当前集合中在另外一个指定集合相同的元素，并将另外一个指定集合中不同的元素插入到当前集合中。</td></tr><tr><td><a href="ref-set-union.html" target="_blank" rel="noopener noreferrer">union()</a></td><td>返回两个集合的并集</td></tr><tr><td><a href="ref-set-update.html" target="_blank" rel="noopener noreferrer">update()</a></td><td>给集合添加元素</td></tr><tr><td><a href="python3-string-len.html" target="_blank" rel="noopener noreferrer">len()</a></td><td>计算集合元素个数</td></tr></tbody></table>