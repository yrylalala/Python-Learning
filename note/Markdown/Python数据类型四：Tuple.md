## Python数据类型四：Tuple

###### 元组（tuple）与列表类似，不同之处在于元组的元素不能修改。元组写在小括号 ( **( )** ) 里，元素之间用逗号隔开。（也可不用小括号，用逗号隔开，用分号结束）。

###### 元组中的元素也可以不相同。

###### 示例：

```python
tuple = ("abcd", 'efg', 123, 1.23)
tinytuple = (123,'hijk')

print (tuple)             # 输出完整元组
print (tuple[0])          # 输出元组的第一个元素
print (tuple[-1])         # 输出元组最后一个元素，负数即为从最后往前读
print (tuple[1:3])        # 输出从第二个元素开始到第三个元素
print (tuple[2:])         # 输出从第三个元素开始的所有元素
print (tinytuple * 2)     # 输出两次元组
print (tuple + tinytuple) # 连接元组
```

![Tuple](https://github.com/yrylalala/Python-Learning/blob/master/pic/Tuple/Tuple1.png?raw=true)



#### 元组可以包含可变的对象及赋值的特殊语法规则

```python
list = [0,1,2]
tuple_1 = (0,1,list) # 可以包含可变的列表

tuple_2 = ()           # 空的数组
tuple_3 = (1,)		   # 一个元素，需要在元素后加逗号，如果不加逗号，括号就会被当做运算符
tuple_4 = 'a',1,"de";  # 可以不加小括号，用逗号隔开，分号结束
```

![Tuple](https://github.com/yrylalala/Python-Learning/blob/master/pic/Tuple/Tuple3.png?raw=true)



#### 元组中的元素值是不允许被删除和修改的

![Tuple2.png](https://github.com/yrylalala/Python-Learning/blob/master/pic/Tuple/Tuple2.png?raw=true)

###### 可以用 del 删除整个元组

![Tuple4](https://github.com/yrylalala/Python-Learning/blob/master/pic/Tuple/Tuple4.png?raw=true)

#### 元组运算符

```python
tup_1 = (0,1,2,3)
tup_2 = (4,5,6)

len(tup_1)   			# 计算长度
tup_1 + tup_2 		    # 拼接
tup_3 = ('a',)*4 		# 重复
2 in tup_1     		    # 元素是否在列表中
for x in tup_1: print (x, end="") # 迭代
```

![Tuple5](https://github.com/yrylalala/Python-Learning/blob/master/pic/Tuple/Tuple5.png?raw=true)



#### 元素内置函数

| 函数         | 描述          |
| ---------- | ----------- |
| len(tuple) | 计算元组元素个数。   |
| max(tuple) | 返回元组中元素最大值。 |
| min(tuple) | 返回元组中元素最小值。 |
| tuple(seq) | 将列表转换为元组。   |



###### string、list 和 tuple 都属于 sequence（序列）。

**注意：**

- 1、与字符串一样，元组的元素不能修改。
- 2、元组也可以被索引和切片，方法一样。
- 3、注意构造包含0或1个元素的元组的特殊语法规则。
- 4、元组也可以使用+操作符进行拼接。

####[返回目录](https://yrylalala.github.io/Python-Learning/)
