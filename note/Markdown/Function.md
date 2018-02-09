## Function

### 定义函数

###### 语法

```python
def 函数名（参数列表）:
    函数体
```

- 函数代码块以 **def** 关键词开头，后接函数标识符名称和圆括号 **()**。
- 任何传入参数和自变量必须放在圆括号中间，圆括号之间可以用于定义参数。
- 函数的第一行语句可以选择性地使用文档字符串—用于存放函数说明。
- 函数内容以冒号起始，并且缩进。
- **return [表达式]** 结束函数，选择性地返回一个值给调用方。不带表达式的 return 相当于返回 None。

###### 示例

```python
def Sum (a, b):
    return a+b
```

###### 函数名其实就是指向一个函数对象的引用，完全可以把函数名赋给一个变量，相当于给这个函数起了一个“别名”。

###### 示例

```python
temp = Sum
temp(1,2)
```

![function0](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function0.png?raw=true)



### 调用函数

###### 默认情况下，参数值和参数名称是按函数声明中定义的的顺序匹配起来的。

###### 示例

```python
result = Sum(1,2)
print(result)
```

![function1](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function1.png?raw=true)



###### python 函数返回多个值

###### 示例

```python
def Calculate(a,b):
    return a+b,a*b,a-b,a//b

x,y,m,n = Calculate(1,2)
print(x,y,m,n)              # 这样可以同时得到返回值

k = Calculate(1,2)
print(k)                    # 事实上函数返回的依然是单一的值，一个 tuple
```

![function2](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function2.png?raw=true)



### 参数

***python 中，类型属于对象，变量是没有类型的，变量仅仅是一个对象的引用（一个指针）。***

- **不可改变对象**（string, tuples, numbers）：变量赋值 a=5 后再赋值 a=10，这里实际是新生成一个 int 值对象 10，再让 a 指向它，而 5 被丢弃，不是改变a的值，相当于新生成了 a。
- **可改变对象**（list, dict）：变量赋值 a=[1,2,3,4] 后再赋值 a[2]=5 则是将 list a 的第三个元素值更改，本身 a 没有动，只是其内部的一部分值被修改了。



#### 参数传递

- **不可变对象：**类似 C++ 的值传递，如 整数、字符串、元组。如fun(a)，传递的只是 a 的值，没有影响 a 对象本身。
- **可变对象：** 类似 C++ 的引用传递，如 列表，字典。如 fun(a)，则是将 a 真正的传过去，修改后 fun 外部的 a 也会受影响。



#### 参数类型

- **必需参数**

  ###### 必需参数须以正确的顺序传入函数。调用时的数量必须和声明时的一样。上述示例中就是这种参数类型。


- **默认参数** 

  ###### 调用函数时，如果没有传递参数，则会使用默认参数。默认参数必须指向不变对象！

  ###### 示例

  ``` python
  def add_end(L = []):
      L.append('END')
      return L

  add_end([1,2,3])      # 正常调用
  add_end()             # 调用默认参数
  add_end()             # 继续调用默认参数
  add_end()             # 再次调用默认参数，由于默认参数是一个变量，没调用一次都会改变它的值
  ```

  ![function4](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function4.png?raw=true)

  ​



- **不定长参数（可变参数）**

  ###### 你可能需要一个函数能处理比当初声明时更多的参数。这些参数叫做不定长参数，和上述2种参数不同，声明时不会命名。

  ###### 语法

  ```python
  def functionname([formal_args,] *var_args_tuple ):    # 可以和必需参数一起使用
     function_suite
     return [expression]
  ```

  ###### 加了星号（*）的变量名会存放所有未命名的变量参数。如果在函数调用时没有指定参数，它就是一个空元组。我们也可以不向函数传递未命名的变量。

  ###### 示例

  ```python
  def printinfo(name, *val):
      print(name)
      for n in val:
          print(n)    
         
  printinfo('abc')          # 可以接受 0 个参数
  printinfo('abc',10,20,30) # 也可以接受多个参数 
  temp = [10,20,30]
  printinfo('abc',*temp)    # 也可以直接调用一个 list 或者 tuple
  ```

  ![function5](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function5.png?raw=true)

  ​


- **关键字参数**

  ###### 关键字参数和函数调用关系紧密，函数调用使用关键字参数来确定传入的参数值。

  ###### 使用关键字参数允许函数调用时参数的顺序与声明时不一致，因为 Python 解释器能够用参数名匹配参数值。

  ###### 示例

  ```python
  def person(name, age, city):
      print(name, age, city)
      
  person(age = 20, name = 'abc', city = 'HZ')   # 这里利用关键字参数，可以不按照声明的顺序传入参数
  ```
  ​

  ###### **关键字参数也可以允许你传入 0 个或任意个含参数名的参数，这些关键字参数在函数内部自动组装为一个dict**。

  ###### 示例

  ```python
  def person(name, age, city, **info):
      print(name, age, city, info)
      
  person('abc', 20, 'HZ')        # 可以接受只传入必需参数
  person('abc', 20, 'HZ', gender='M', job ='programer')  # 也可以传入任意个数的关键字参数
                                                         # 注意这里的 gender 和 job 是参数名，不                                                        # 是 dict 的 key。
  other = { 'gender': 'M', 'job': 'programer'}   # 也可以将定义好的 dict 传入函数，这里的gender 
  person('abc', 20, 'HZ', **other)               # 和 job 是 dict 的 key，所以需要加上引号。  
  ```

  ![function3(1)](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function3(1).png?raw=true)

- **命名关键字参数**

  ###### 如果要限制关键字参数的名字，就可以用命名关键字参数*命名关键字参数*。 命名关键字参数需要一个特殊分隔符  \* ， \*  后面的参数被视为命名关键字参数。

  ###### 示例

  ```python
  def person(name, age, *,city, gender):  # city gender 都是命名关键字
      print(name, age, city, gender)
      
  person('abc', 20, city = 'HZ', gender='M')  

  def person_(name, age, *val, city, gender): # 当有一个不定长参数的时候，就不需要一个特殊分隔符了
      print(name, age, city, gender)
      for n in val:
          print(n) 
          
  person_('abc', 20, 10,20,30, city = 'HZ', gender='M') # 但是，命名关键字参数必须带上关键字
  ```

  ![function3(2)](https://github.com/yrylalala/Python-Learning/blob/master/pic/function/function3(2).png?raw=true)




#### 参数组合

######         在 Python 中定义函数，可以用必需参数、默认参数、不定长参数、关键字参数和命名关键字参数，这 5 种参数都可以组合使用。但是请注意，参数定义的顺序必须是：<u>必需参数、默认参数、不定长参数、命名关键字参数和关键字参数</u>。



  