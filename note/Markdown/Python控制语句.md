## Python 控制语句

#### if 语句

###### 语法形式：

```python
if 表达式1:
    语句
elif 表达式2:
    语句
else:
    语句
```

###### if 嵌套

```python
if 表达式1:
    语句
    if 表达式2:
        语句
    elif 表达式3:
        语句
    else:
        语句
elif 表达式4:
    语句
else:
    语句
```

**注意：**

- 1、每个条件后面要使用冒号（ : ），表示接下来是满足条件后要执行的语句块。
- 2、使用缩进来划分语句块，相同缩进数的语句在一起组成一个语句块。
- 3、在 Python 中没有 switch – case 语句。




#### while 语句

###### 语法形式：

```python
while 判断条件：
    语句
```

###### while 循环使用 else

```python
while 判断条件：
	语句
else:            # 当判断条件为 false 的时候才执行 else
    语句
```

###### while 无线循环

```python
var = 1
while var ==1:
    语句         # 无限循环可以用 ctrl + C 停下来
```

###### 简单语句组

示例：

```python
var = 1
while (var): print('easy') # 这样可以写在同一行中
```

**注意：**

- 1、每个条件后面要使用冒号（ : ），表示接下来是满足条件后要执行的语句块。
- 2、使用缩进来划分语句块，相同缩进数的语句在一起组成一个语句块。
- 3、在 Python 中没有 do..while 循环。




#### for 语句

###### Python for循环可以遍历任何序列的项目，如一个列表或者一个字符串。

###### 语法格式：

```python
for <variable> in <sequence>:
    <statements>
else:
    <statements>
```

###### range() 函数

###### python 提供了一个内置函数可以方便 for 语句来遍历数字序列

```   python
for i in range(5):
    print(i)          # 可以输出 0 1 2 3 4

for i in range(3,9):
    print(i)          # 可以输出 3 4 5 6 7 8

for i in range(0,10,2):
    print(i)          # 可以按照步长输出 0 2 4 6 8
```



#### break

###### break 是可以跳出 while 和 for 循环体

```python
var = 10
while var > 0:
    var = var-1
    if var==5:
    	break
    print(var,end='')
```

![break](https://github.com/yrylalala/Python-Learning/blob/master/pic/%E6%8E%A7%E5%88%B6%E8%AF%AD%E5%8F%A5/break.png?raw=true)



#### continue

###### continue 是用来跳过当前一次循环，可以跳过当前循环块中的剩下语句，继续下一轮循环。

```python
var = 10
while var > 0:
    var = var-1
    if var==5:
    	continue
    print(var,end='')
```

![continue](https://github.com/yrylalala/Python-Learning/blob/master/pic/%E6%8E%A7%E5%88%B6%E8%AF%AD%E5%8F%A5/continue.png?raw=true)



#### else

###### python中 的 else 可以作为 while 还有 for 循环语句的字句。

###### 它在穷尽列表(以 for 循环)或条件变为 false (以 while 循环)导致循环终止时被执行，但循环被 break 终止时不执行。

```python
for n in range(2, 10):           # 查询质数
    for x in range(2, n):
        if n % x == 0:
            print(n, '等于', x, '*', n//x)
            break
    else:
        # 循环中没有找到元素
        print(n, ' 是质数')
```

![else](https://github.com/yrylalala/Python-Learning/blob/master/pic/%E6%8E%A7%E5%88%B6%E8%AF%AD%E5%8F%A5/else.png?raw=true)

#### pass

###### Python pass是空语句，是为了保持程序结构的完整性。

###### pass 不做任何事情，一般用做占位语句，在代码段中或定义函数的时候，如果没有内容，或者先不做任何处理，直接跳过，就可以使用pass。

```python
for i in range(5):
    pass
    print('run pass')
print('Over')
```

![pass](https://github.com/yrylalala/Python-Learning/blob/master/pic/%E6%8E%A7%E5%88%B6%E8%AF%AD%E5%8F%A5/pass.png?raw=true)

####[返回目录](https://yrylalala.github.io/Python-Learning/)
