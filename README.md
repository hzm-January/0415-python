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
## Python标识符
* 字母、数字、下划线组成
* 区分大小写
* 不能以数字开头
* 单下划线开头：（例：_foo）表示不能直接访问的类属性，需通过类提供的接口进行访问，不能用 from xxx import * 而导入
* 双下划线开头：（例：__foo）表示私有成员
* 双下划线开头并结尾：（例：__foo__）Python 里特殊方法专用的标识（例：__init__()）表示类的构造函数
* 同一行可以书写多条语句，需要使用分号`;`隔开
### Python保留字
| | | |
|:-:|:-:|:-:|
and	    |  exec	    |not
assert	|  finally	|or
break	|  for	    |pass
class	|  from	    |print
continue|  global	|raise
def	    |  if	    |return
del	    |  import	|try
elif	|  in	    |while
else	|  is	    |with
except	|  lambda	|yield

