## Python数据类型六：Set

###### 集合（set）是一个无序不重复元素的序列。

######基本功能是进行成员关系测试和删除重复元素。

###### 可以使用大括号 { } 或者 set() 函数创建集合，注意：创建一个空集合必须用 set() 而不是 { }，因为 { } 是用来创建一个空字典。

#### 格式：

```python
parame = {val1,val2,...}
set(val)
```



#### 示例：

```python
set_1 = {'a', 'b', 'c', 'd', 'a', 'b'}
print(set_1)   # 输出集合，重复的元素被自动去掉
 
# 成员测试
if('a' in set_1) :
    print('a 在集合中')
else :
    print('a 不在集合中')
 
# set可以进行集合运算
a = set('abcdefghij')
b = set('abcklmn')
 
print(a)
print(a - b)     # a和b的差集
print(a | b)     # a和b的并集
print(a & b)     # a和b的交集
print(a ^ b)     # a和b中不同时存在的元素
```



![Set](https://github.com/yrylalala/Python-Learning/blob/master/pic/Set/Set.png?raw=true)







