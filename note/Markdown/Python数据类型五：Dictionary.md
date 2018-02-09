## Python数据类型五：Dictionary

###### 字典（dictionary）是Python中另一个非常有用的内置数据类型。

###### 列表是有序的对象结合，字典是无序的对象集合。两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。这有点类似向量和哈希表。

######字典是一种映射类型，字典用"{ }"标识，它是一个无序的**键(key) : 值(value)**对集合。

###### 键(key)必须使用不可变类型，所以可以用数字，字符串或元组充当，但用**列表**就不行。

######在同一个字典中，键(key)必须是唯一的。

```python
dict = {}
dict['one'] = "value"
dict[2]     = "值"

tinydict = {'key1': 1,'二':'ab', 3: 1.23}

print (dict['one'])      	 # 输出键为 'one' 的值
print (dict[2])         	 # 输出键为 2 的值
print (tinydict)         	 # 输出完整的字典
print (tinydict.keys())  	 # 输出所有键
print (tinydict.values()) 	 # 输出所有值
```

![Dictionary1](https://github.com/yrylalala/Python-Learning/blob/master/pic/Dict/Dictionary1.png?raw=true)

#### 构建字典

```python
dict1 = {'key1': 1,'二':'ab', 3: 1.23}
dict2 = dict([('key1', 1),('二', 'ab'), (3, 1.23)])  # 利用构造函数dict()
dict3 = dict( key1 = 1,二 = 'ab', 3 = 1.23)  # 注意这里不能利用3当键值，会报错(测试应该是不能用常数)
dict4 = dict( key1 = 1,二 = 'ab', three = 1.23) # 这里利用字符串就可以
```

![Dictionary2](https://github.com/yrylalala/Python-Learning/blob/master/pic/Dict/Dictionary2.png?raw=true)

#### 访问字典

```python
dict1 = {'key1': 1,'二':'ab', 3: 1.23}

print (dict1['key1'])     # 利用键值访问字典中的元素
print (dict1[4])          # 当要访问字典中没有的键值时，就会报错
```

![Dictionary3](https://github.com/yrylalala/Python-Learning/blob/master/pic/Dict/Dictionary3.png?raw=true)



#### 修改字典

字典中的键是不能修改的，但是值是可以修改的，并且值可以是变量。

```python
dict1 = {'key1': 1,'二':'ab', 3: 1.23}

dict1['key1'] =0   # 修改'key1'对应的值
dict1[4] = 'four'  # 添加一对键值
```

![Dictionary4](https://github.com/yrylalala/Python-Learning/blob/master/pic/Dict/Dictionary4.png?raw=true)



#### 删除字典中的元素

```python
dict1 = {'key1': 1,'二':'ab', 3: 1.23}

del dict1['key1']  # 删除键 'key1'
dict1.clear()      # 清空字典
del dict1          # 删除字典
```

![Dictionary5](https://github.com/yrylalala/Python-Learning/blob/master/pic/Dict/Dictionary5.png?raw=true)



#### 字典内置函数和方法

| 函数             | 描述                       |
| -------------- | ------------------------ |
| len(dict)      | 计算字典元素个数，即键的总数。          |
| str(dict)      | 输出字典，以可打印的字符串表示。         |
| type(variable) | 返回输入的变量类型，如果变量是字典就返回字典类型 |

| 方法                                 | 描述                                       |
| :--------------------------------- | ---------------------------------------- |
| dict.clear()                       | 删除字典内所有元素                                |
| dict.copy()                        | 返回一个字典的浅复制                               |
| dict.fromkeys(seq[, value]))       | 创建一个新字典，以序列seq中元素做字典的键，val为字典所有键对应的初始值   |
| dict.get(key, dafault=None)        | 返回指定键的值，如果值不在字典中返回default值               |
| key in dict                        | 如果键在字典dict里返回true，否则返回false              |
| dict.items()                       | 以列表返回可遍历的(键, 值) 元组数组                     |
| dict.keys()                        | 以列表返回一个字典所有的键                            |
| dict.setdefault(key, default=None) | 和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default  |
| dict.update(dict2)                 | 把字典dict2的键/值对更新到dict里                    |
| dict.values()                      | 以列表返回字典中的所有值                             |
| pop(key[,default\])]               | 删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。 |
| popitem()                          | 随机返回并删除字典中的一对键和值(一般删除末尾对)。               |



**注意：**

- 1、字典是一种映射类型，它的元素是键值对。
- 2、字典的关键字必须为不可变类型，且不能重复。
- 3、创建空字典使用 **{ }**。

####[返回目录](https://yrylalala.github.io/Python-Learning/)
