# Python笔记
## 安装Python
1. 下载对应系统的安装包
2. 配置环境变量
3. 测试是否配置成功  
`python --version`
## HelloWorld
1. 新建hello.py文件，并编写以下内容  
`print('Hello, World!')`
2. 执行该文件 
`python hello.py`
## 基础语法
### Python标识符
* 字母、数字、下划线组成
* 区分大小写
* 不能以数字开头
* 单下划线开头：（例：_foo）表示不能直接访问的类属性，需通过类提供的接口进行访问，不能用 from xxx import * 而导入
* 双下划线开头：（例：__foo）表示私有成员
* 双下划线开头并结尾：（例：__foo__）Python 里特殊方法专用的标识（例：__init__()）表示类的构造函数
* 同一行可以书写多条语句，需要使用分号`;`隔开
### Python保留字
* 保留字不能用作常数或变数，或任何其他标识符名称
* 关键字只包含小写字母

and	    |  exec	    |not
|:-:|:-:|:-:|
assert	|  finally	|or
break	|  for	    |pass
class	|  from	    |print
continue|  global	|raise
def	    |  if	    |return
del	    |  import	|try
elif	|  in	    |while
else	|  is	    |with
except	|  lambda	|yield

### 行和缩进
* Python 的代码块使用**缩进**来控制类、函数以及其他逻辑判断，而不使用大括号 {}
* 代码块中的缩进必须严格一致
* 建议每个缩进层次使用 单个制表符 或 两个空格 或 四个空格
>IndentationError: unindent does not match any outer indentation level错误表明，你使用的缩进方式不一致，有的是 tab 键缩进，有的是空格缩进，改为一致即可。  
 IndentationError: unexpected indent 错误, 则 python 编译器是在告诉你"你的文件里格式不对了，可能是tab和空格没对齐的问题"。
 
### 多行语句
* 以新行作为语句的结束符
* 若需要多行显示一行语句，可以使用斜杠（\）将一行的语句分为多行显示
<pre name="code" class="python">
total = item_one + \
        item_two + \
        item_three
</pre>
### 引号
* Python 可以使用引号( ' )、双引号( " )、三引号( ''' 或 """ ) 来表示字符串
* 引号的开始与结束必须的相同类型的
* 三引号可以由多行组成，编写多行文本的快捷语法，常用于文档字符串，在文件的特定地点，被当做注释
<pre name="code" class="python">
word = 'word'
sentence = "这是一个句子。"
paragraph = """这是一个段落。
包含了多个语句"""
</pre>
### 注释
* 单行注释：使用#开头
* 多行注释：使用三个单引号或三个双引号包裹

>\#!/usr/bin/python  
\# -*- coding: UTF-8 -*-  
\# 文件名：test.py  

>'''  
这是多行注释，使用三个单引号包裹。  
'''  
"""  
这是多行注释，使用三个双引号。  
"""
### Python 空行
* 函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。
* 类和函数入口之间也用一行空行分隔，以突出函数入口的开始。
* 空行与代码缩进不同，空行并不是Python语法的一部分，书写时不插入空行，Python解释器运行也不会出错，作用在于分隔两段不同功能或含义的代码。
### Print 输出
* print 默认输出是换行的
* print 末尾加上逗号(,)可以实现不换行需要在变量
### 多个语句组成代码组
### 命令行参数
<pre name="code" class="shell">
$ python -h 
usage: python [option] ... [-c cmd | -m mod | file | -] [arg] ... 
Options and arguments (and corresponding environment variables): 
-c cmd : program passed in as string (terminates option list) 
-d     : debug output from parser (also PYTHONDEBUG=x) 
-E     : ignore environment variables (such as PYTHONPATH) 
-h     : print this help message and exit 
 
[ etc. ] 
</pre>