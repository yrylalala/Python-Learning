## Python3 中有6种标准数据类型
- #### Number （数字）
- #### String （字符串）
- #### List （列表）
- #### Tuple （元组）
- #### Sets （集合）
- #### Dictionary （字典）
---

## Python数据类型一：Number
- **int**
- **float**
- **bool**
- **complex**

###### Python3 中只有一种整数类型 int，而且是长整型，没有 Python2 中的 Long。
###### Python2 中是没有布尔型的，它用数字 0 表示 False，用 1 表示 True。到 Python3 中，把 True 和 False 定义成关键字了，但它们的值还是 1 和 0，它们可以和数字相加。

#### 变量赋值
###### 当进行赋值操作的时候，Number 对象就会被创建，无须进行变量类型声明。
```python
var = 1
var = 10.0
```
###### Python 可以对多个变量同时赋值，如
```python
var1,var2,var3 = 1,2,3
```
###### 由于变量不需要声明变量类型,一个变量可以通过赋值指向不同类型的对象，变量的类型由赋予它的值来决定，如
```python
a = 1
a = 1.1
a = "python"
# 程序结束的时候，变量 a，只保留了字符串类型的值。
```

###### 有创建也有删除
```python
del var
del var1,var2
```
#### 数值运算
- ##### 算术运算符
```python
5 + 4   #加法
4 - 2   #减法
3 * 7   #乘法
2 / 4   #除法，得到一个浮点数
2 // 4  #除法，得到一个整数
17 % 3  #取余
2 ** 5  #乘方
```
###### 数值的除法（/）总是返回一个浮点数，要获取整数使用（//）操作符。
###### 在混合计算时，Python 会把整型转换成为浮点数。
###### Python 还支持复数，复数由实数部分和虚数部分构成，可以用a + bj,或者complex(a,b)表示， 复数的实部a和虚部b都是浮点型。

- ##### 比较运算符

| 运算符  | 描述   |
| :--: | ---- |
|  ==  | 等于   |
|  !=  | 不等于  |
|  >   | 大于   |
|  <   | 小于   |
|  >=  | 大于等于 |
|  <=  | 小于等于 |
###### 比较运算均有返回值，True 或者 Flase

- ##### 赋值运算符

| 运算符  | 描述                     |
| :--: | ---------------------- |
|  =   | 简单赋值操作                 |
|  +=  | c += a 等效于 c = c + a   |
|  -=  | c -= a 等效于 c = c - a   |
|  *=  | c *= a 等效于 c = c * a   |
|  /=  | c /= a 等效于 c = c / a   |
|  %=  | c %= a 等效于 c = c % a   |
| **=  | c **= a 等效于 c = c ** a |
| //=  | c //= a 等效于 c = c // a |

- ##### 位运算符

| 运算符  | 描述                                       |
| :--: | ---------------------------------------- |
|  &   | **按位与运算符**：参与运算的两个值,如果两个相应位都为1,则该位的结果为1,否则为0 |
|  \|  | **按位或运算符**：只要对应的二个二进位有一个为1时，结果位就为1。      |
|  ^   | **按位异或运算符**：当两对应的二进位相异时，结果为1             |
|  ~   | **按位取反运算符**：对数据的每个二进制位取反,即把1变为0,把0变为1。~x 类似于 -x-1 |
|  <<  | **左移动运算符**：运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0。 |
|  >>  | **右移动运算符**：把">>"左边的运算数的各二进位全部右移若干位，">>"右边的数指定移动的位数 |

- ##### 逻辑运算符

| 运算符  | 描述                                       |
| :--: | ---------------------------------------- |
| and  | **布尔"与"** - 如果 x 为 False，x and y 返回 False，否则它返回 y 的计算值。 |
|  or  | **布尔"或"** - 如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值。 |
| not  | **布尔"非"** - 如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。 |
###### python 中的 and 从左到右计算表达式，若所有值均为真，则返回最后一个值，若存在假，返回第一个假值；
###### or 也是从左到有计算表达式，返回第一个为真的值；
###### 其中数字 0 是假，其他都是真；
###### 字符 "" 是假，其他都是真；


####[返回目录](https://yrylalala.github.io/Python-Learning/)
