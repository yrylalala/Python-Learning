## Python基础知识(2)

#### Python关键字

###### 我们不能把它们用作任何标识符名称。Python 的标准库提供了一个 keyword 模块，可以输出当前版本的所有关键字
```python
import keyword
keyword.kwlist
```
![keyword](https://github.com/yrylalala/Python-Learning/blob/master/pic/Python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86(2)/1.jpg?raw=true)

#### 注释
###### Python中单行注释以 # 开头
```python
#这是一行注释
```

#### 多行语句
###### Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠 ( \\ ) 来实现多行语句
```python
test = test_1 + \
       test_2 + \
       test_3
```
在 [], {}, 或 () 中的多行语句，不需要使用反斜杠( \\ )
```python
test = [ 'test_1',
         'test_2',
         'test_3' ]
```

#### 显示帮助 help() 函数
调用 python 的 help() 函数可以打印输出一个函数的文档字符串
```python
help(max)
```
![help](https://github.com/yrylalala/Python-Learning/blob/master/pic/Python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86(2)/2.jpg?raw=true)


####[返回目录](https://yrylalala.github.io/Python-Learning/)
