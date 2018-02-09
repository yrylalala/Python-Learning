## Python数据类型三：List
###### List（列表） 是 Python 中使用最频繁的数据类型。
###### 列表可以完成大多数集合类的数据结构实现。列表中元素的类型可以不相同，它支持数字，字符串甚至可以包含列表（所谓嵌套）。

###### 列表是写在方括号 ( [ ] ) 之间、用逗号分隔开的元素列表。

###### 和字符串一样，列表同样可以被索引和截取，列表被截取后返回一个包含所需元素的新列表。

###### 列表截取的语法格式如下：
```python
变量[头下标:尾下标]
```



#### 列表创建、访问和输出

示例：

```python
list = [ 'abcd', 123 , 1.23, 'e' ]
tinylist = [list, 'fghi']     # 列表支持嵌套

print (list)            # 输出完整列表
print (list[0])         # 输出列表第一个元素
print (list[-1])        # 输出列表最后一个元素,负数即为从最后往前读
print (list[1:3])       # 从第二个开始输出到第三个元素
print (list[2:])        # 输出从第三个元素开始的所有元素
print (tinylist * 2)    # 输出两次列表
print (list + tinylist) # 连接列表
```

![List1](https://github.com/yrylalala/Python-Learning/blob/master/pic/List/List1.png?raw=true)

特殊的创建和访问：

![List1(2)](https://github.com/yrylalala/Python-Learning/blob/master/pic/List/List1(2).png?raw=true)

即按照步长2输出。遍历 [start,end)，间隔为 span，当 span>0 时顺序遍历, 当 span<0 时，逆着遍历。

start 不输入则默认为 0，end 不输入默认为长度。



#### 列表中的元素是可以进行修改的

![List2](https://github.com/yrylalala/Python-Learning/blob/master/pic/List/List2.png?raw=true)



#### 删除列表元素

![List3](https://github.com/yrylalala/Python-Learning/blob/master/pic/List/List3.png?raw=true)





#### 列表脚本操作符

```python
list_1 = [ 0, 1, 2, 3 ]
list_2 = [ 4, 5, 6 ]

len(list_1)    			# 计算长度
list_1 + list_2 		# 拼接
list_3 = ['a']*4 		# 重复
2 in list_1     		# 元素是否在列表中
for x in list_1: print(x, end="") # 迭代
```

![List4](https://github.com/yrylalala/Python-Learning/blob/master/pic/List/List4.png?raw=true)

#### 列表函数和方法

和 C++ 中的 vector 类似。

| 函数        | 描述        |
| --------- | --------- |
| len(list) | 列表元素个数    |
| max(list) | 返回列表元素最大值 |
| min(list) | 返回列表元素最小值 |
| list(seq) | 将元组转换为列表  |

| 方法                      | 描述                                |
| ----------------------- | --------------------------------- |
| list.append(obj)        | 在列表末尾添加新的对象                       |
| list.count(obj)         | 统计某个元素在列表中出现的次数                   |
| list.extend(seq)        | 在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表） |
| list.index(obj)         | 从列表中找出某个值第一个匹配项的索引位置              |
| list.insert(index, obj) | 将对象插入列表                           |
| list.pop(obj=list[-1\]) | 移除列表中的一个元素（默认最后一个元素），并且返回该元素的值    |
| list.remove(obj)        | 移除列表中某个值的第一个匹配项                   |
| list.reverse()          | 反向列表中元素                           |
| list.sort([func\])      | 对原列表进行排序                          |
| list.clear()            | 清空列表                              |
| list.copy()             | 复制列表                              |



#### 列表生成式

###### 列表生成式即 List Comprehensions，是Python内置的非常简单却强大的可以用来创建 list 的生成式。

###### 示例

```python
list(range(1,11))
[x * x for x in range(1, 11)]
[x * x for x in range(1, 11) if x % 2 == 0]
[m + n for m in 'ABC' for n in 'XYZ']
```

![list5](https://github.com/yrylalala/Python-Learning/blob/master/pic/List/List5.png?raw=true)



#### 注意：

- 1、List写在方括号之间，元素用逗号隔开。
- 2、和字符串一样，list可以被索引和切片。
- 3、List可以使用+操作符进行拼接。
- 4、List中的元素是可以改变的。

####[返回目录](https://yrylalala.github.io/Python-Learning/)
