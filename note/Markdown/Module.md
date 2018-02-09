## Module

######                 为了编写可维护的代码，我们把很多函数分组，分别放到不同的文件里，这样，每个文件包含的代码就相对较少，很多编程语言都采用这种组织代码的方式。在Python中，一个.py文件就称之为一个模块（Module）。这样定义的函数和变量不会因为解释器的退出而消失。

######                 模块最大的好处是大大提高了代码的可维护性。其次，编写代码不必从零开始。当一个模块编写完毕，就可以被其他地方引用。使用模块还可以避免函数名和变量名冲突。相同名字的函数和变量完全可以分别存在不同的模块中，因此，我们自己在编写模块时，不必考虑名字会与其他模块冲突。

######         另外，为了避免模块名冲突，Python又引入了按目录来组织模块的方法，称为包（Package）。

###### 结构示例

```
mycompany             # 顶层包结构
 ├─ web               # 子包
 │  ├─ __init__.py    # 包目录下必须存在的模块，可以是空文件也可以有代码，模块名就是包的名字 web
 │  ├─ utils.py       # 模块名字就是 mycompany.web.utils
 │  └─ www.py
 ├─ __init__.py
 ├─ abc.py
 └─ xyz.py
```



创建自己的模块时，要注意：

- 模块名要遵循Python变量命名规范，不要使用中文、特殊字符；
- 模块名不要和系统模块名冲突，最好先查看系统是否已存在该模块，检查方法是在 Python 交互环境执行import abc ，若成功则说明系统存在此模块。



#### import 语句

###### 想使用 Python 模块，只需在另一个源文件里执行 import 语句。

###### 语法

```python
import module1[, module2[,... moduleN]
```

###### 当解释器遇到 import 语句，如果模块在当前的搜索路径就会被导入。搜索路径是一个解释器会先进行搜索的所有目录的列表。

```python
#!/usr/bin/env python3       注释，可以让该文件直接在 Unix/Linux/Mac 上运行
# -*- coding: utf-8 -*-      注释，表示本身是使用 utf-8

' a test module '    # 一个字符串，表示模块的文档注释，任何模块代码的第一个字符串都被视为模块的文档注释

__author__ = 'Michael Liao'  # 使用 __author__ 变量把作者写进去

import sys                   # 使用 sys 模块，利用import 语句导入 sys 模块

def test():
    args = sys.argv                # 在导入模块 sys 之后，就可以利用变量 sys 来访问模块中的所有功能
    if len(args)==1:               # sys 模块中的变量argv，用 list 保存了命令行的所有参数。其中至少
        print('Hello, world!')     # 有一个参数， 因为第一个参数永远是该.py文件的名称
    elif len(args)==2:
        print('Hello, %s!' % args[1])
    else:
        print('Too many arguments!')

if __name__=='__main__':   # 当我们在命令行运行该模块文件时，Python 解释器把一个特殊变量 __name__ 置
    test()                 # 为__main__，而如果在其他地方导入该模块时，if判断将失败，因此，这种if测试                            # 可以让一个模块通过命令行运行时执行一些额外的代码，最常见的就是运行测试。
```

![module1](https://github.com/yrylalala/Python-Learning/blob/master/pic/Module/module1.png?raw=true)



#### from…import 语句

###### from...import 语句可以从模块中导入一个指定的部分到当前命名空间中。

###### 语法

```python
from modname import name1[, name2[, ... nameN]]
```

###### 示例

![module](https://github.com/yrylalala/Python-Learning/blob/master/pic/Module/module2.png?raw=true)



#### 作用域

######         在一个模块中，可能会定义很多函数和变量，但有的函数和变量仅仅在模块内部使用，不希望被外界调用。在Python中，是通过 `_` 前缀来实现的。

- ###### 正常的函数和变量名是公开的（public），可以被直接引用，比如：`abc`，`x123`，`PI` 等；

- ###### 类似 `__xxx__` 这样的变量是特殊变量，可以被直接引用，但是有特殊用途，比如上面的 `__author__`，`__name__` 就是特殊变量，`hello` 模块定义的文档注释也可以用特殊变量 `__doc__` 访问，我们自己的变量一般不要用这种变量名；

- ###### 类似 `_xxx` 和 `__xxx` 这样的函数或变量就是非公开的（private），不应该被直接引用，比如 `_abc`，`__abc` 等。

###### 注意，private函数和变量 <u>*不应该*</u> 被直接引用，而不是 *<u>不能</u>* 被直接引用，是因为Python并没有一种方法可以完全限制访问 private 函数或变量，但是，从编程习惯上不应该引用 private 函数或变量。

####[返回目录](https://yrylalala.github.io/Python-Learning/)
