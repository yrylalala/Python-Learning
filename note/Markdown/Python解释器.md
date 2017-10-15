# Python解释器
原文地址：[廖雪峰教程之Python解释器](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/00143161198846783e33de56d4041058c3dfc7e44ee1203000)

---
&emsp;&emsp;**当我们编写Python代码时，我们得到的是一个包含Python代码的以.py为扩展名的文本文件。要运行代码，就需要Python解释器去执行.py文件。**
&emsp;&emsp;**由于整个Python语言从规范到解释器都是开源的，所以理论上，只要水平够高，任何人都可以编写Python解释器来执行Python代码（当然难度很大）。事实上，确实存在多种Python解释器。**


##### 1. CPython
&emsp;&emsp;当我们从Python官方网站下载并安装好Python 3.5后，我们就直接获得了一个官方版本的解释器：CPython。这个解释器是用C语言开发的，所以叫CPython。
在命令行下运行 ***python*** 就是启动CPython解释器。
&emsp;&emsp;CPython是使用最广的Python解释器。教程的所有代码也都在CPython下执行。

##### 2. IPython
&emsp;&emsp;IPython是基于CPython之上的一个交互式解释器，也就是说，IPython只是在交互方式上有所增强，但是执行Python代码的功能和CPython是完全一样的。好比很多国产浏览器虽然外观不同，但内核其实都是调用了IE。
&emsp;&emsp;**CPython用>>>作为提示符，而IPython用In [序号]:作为提示符。**

##### 3. PyPy
&emsp;&emsp;PyPy是另一个Python解释器，它的目标是**执行速度**。PyPy采用JIT技术，对Python代码进行动态编译（注意不是解释），所以可以显著提高Python代码的执行速度。
&emsp;&emsp;绝大部分Python代码都可以在PyPy下运行，但是PyPy和CPython有一些是不同的，这就导致相同的Python代码在两种解释器下执行可能会有**不同的结果**。如果你的代码要放到PyPy下执行，就需要了解PyPy和CPython的不同点。

##### 4. Jython
&emsp;&emsp;Jython是运行在Java平台上的Python解释器，可以直接把Python代码编译成**Java字节码**执行。

##### 5. IronPython
&emsp;&emsp;IronPython和Jython类似，只不过IronPython是运行在**微软.Net平台**上的Python解释器，可以直接把Python代码编译成 **.Net的字节码**。

---
### 小结
&emsp;&emsp;Python的解释器很多，但使用最广泛的还是**CPython**。如果要和Java或.Net平台交互，最好的办法不是用Jython或IronPython，而是**通过网络调用来交互**，确保各程序之间的独立性。


###[返回目录](https://yrylalala.github.io/Python-Learning/)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[下一篇](/note/Html/Python基础知识1.html)
