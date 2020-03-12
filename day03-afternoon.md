
# 1. Python 
## 1.1 认识Python
1991年诞生
人生苦短，我用Python

* 优点
  * 简单
  * 易学
  * 免费、开源
  * 高层语言
  * 可移植性
  * 解释性
  * 丰富的库
  * 规范的代码
* 缺点
  * 运行速度
  * 国内市场小
  * 中文资料匮乏
  * 框架选择太多
* Python应用场景
  * web应用开发-mod_wsgi模块
  * 操作系统管理、服务器运维的自动化脚本
  * 科学计算
  * 桌面软件-pyQi、PySide、wxPython、PyGTK是开发桌面应用程序的利器。
  * 服务器软件（网络软件）
  * 游戏
  * 构思实现，产品早期原型和迭代



## 1.2 第一个Python程序
1. 打开超级终端；
2. 输入python3或者python；
3. 运行print("Hello World")
![helloworld](images/day3-2.jpg)
发现除了print一些字符之外python还能执行一些数学计算。

iPython是交互式的python。

python 和 python3的区别：
* Python3 可以补全命令；

* 在代码第一行写入执行时的Python解释器路径，编辑完后需要对此python文件添加‘x'权限
```
#!/usr/bin/python3
#coding=utf-8  
#该行必须放在顶端，也不能加空格
print("hello world!")
```
写出来的程序保存为1.py；需要手动加执行权限之后才能使用./1.py来运行。   
![1py](images/day3-3.jpg)

## 1.3 注释
可以使用"#"来给代码注释该段代码的意思： 
* 单行注释
* 多行注释
* 文本注释

## 1.4 变量以及类型
1. 变量的定义
在python中如果需要存储一个数据，则需要使用变量的概念：  
名字 = 值  

```
a = 100
b = 200
c = a + b
print(“c”)
```

print(“c”) 加上""之后输出是c；去掉""之后输出300.   
![print](images/day3-4.jpg)

2. 变量类型
   * number:
     * int ---整数类型
     * long ---长整型[也可以代表八进制和十六进制]
     * float ---浮点型
     * complex ---复数
   * 布尔类型
     * true
     * false
   * string --- 字符型
   * List --- 列表
   * Tuple --- 元祖
   * Dictionary --- 字典
如何判断字符类型：   
* 示例代码：
```
#!/usr/bin/python3
#coding=utf-8
print("hello world!")
name = "jack"
age = 20
a = 100
b = 200
c = a + b
print(c)
print(type(age))
print(type(name))
```
* 输出结果如下,可以看到通过type()可以自动识别变量类型：
![type](images/day3-5.jpg)

注意点：   
***Print函数建议加括号()；如果不加括号，python3无法识别。***

## 1.5 标识符和关键字
标示符：开发人员在程序中自定义的一些符号和名称。   
标示符由字母、下划线和数字组成；只允许字母或者_开头；数字不允许开头。   
**python标示符中区分大小写**
### 命名规则
* 见名知意
* 驼峰命名法---如：userName,userLoginVar,myCar

### 关键字
python一些具有特殊功能的标示符，这就是所谓的关键字；   
关键字，是python已经在使用的了，所以不允许开发者自己定义相同名字的标示符。   
可以使用如下方法导出系统默认关键字列表：   
1. 使用ipython3输入import keyword；
2. 然后再输入keyword.kwlist可以print所有的默认关键字。
```
'False',
 'None',
 'True',
 'and',
 'as',
 'assert',
 'break',
 'class',
 'continue',
 'def',
 'del',
 'elif',
 'else',
 'except',
 'finally',
 'for',
 'from',
 'global',
 'if',
 'import',
 'in',
 'is',
 'lambda',
 'nonlocal',
 'not',
 'or',
 'pass',
 'raise',
 'return',
 'try',
 'while',
 'with',
 'yield'
```

## 1.6 输出
格式化输出
```
\n  表示换行
\t  表示tab键
+   可以把变量加一起显示
```
示例1：   
```
root@k8s-node1:~# cat 6.py 
#output

print("name:xiaotu")
print("联系方式:181*********")
print("地址:南京*****")
root@k8s-node1:~# python3 6.py 
name:xiaotu
联系方式:181*********
地址:南京*****
root@k8s-node1:~# vim 6.py 
root@k8s-node1:~# cat 6.py 
#output

print("name:\nxiaotu")
print("联系方式:\t181*********")
print("地址:南京*****")
root@k8s-node1:~# python3 6.py 
name:
xiaotu
联系方式:       181*********
地址:南京*****
```
示例2：   
```
root@k8s-node1:~# cat 6.py 
#output
name = "xiaotu"
phone = 181
address = "nanjing"
print("name:\nxiaotu")
print("联系方式:\t181*********")
print("地址:南京*****")
print(name+address)
root@k8s-node1:~# python3 6.py 
name:
xiaotu
联系方式:       181*********
地址:南京*****
xiaotunanjing
root@k8s-node1:~# 
```
示例3：   
```
 

```



## 1.7 输入


## 1.8 运算符


## 1.9  


## 1.10 


## 1.11 


## 1.12 


## 1.13


## 1.14 

***
有兴趣一起学习的可以加我微信，大家一起交流。加我请备注“13天Python学习”
![mywechat](https://github.com/i4leader/python-learning-notes/blob/master/images/mywechat.jpeg)