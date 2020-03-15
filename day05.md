## Day5-字符串、列表、元祖、字典
### 字符串介绍
#### python 中字符串的格式
如下定义的变量a，存储的是数字类型的值   
```
a = 100
```
如下定义的变量b，存储的是字符串类型的值   
```
b = "hello github.com"
c = 'hello github.com'
```
小总结：   
* 双引号或者单引号中的数据，就是字符串
* 
### 字符串输出


### 字符串输入
input获取的数据，都是以字符串方式进行保存，包含输入的数字也是以字符串的方式保存。   
demo:   
```
userName = "i4leader"
print("用户名为:%s"%userName)

password = input("请输入密码:")
print("密码为:%s"%password)
```
结果：(根据输入的不同结果也不同)   
```
请输入用户名：i4leader
用户名为：i4leader
请输入密码:xxxxxxx
密码为:xxxxxxx
```



### 下标和切片
### 1. 下标索引
所谓“下标”，就是编号，就好比超市中的存储柜的编号，通过这个编号就能找到相应的存储空间
* 生活中的下标
  超市储物柜
* 字符串中’下标‘的使用
  **列表与元组支持下标索引好理解，字符串实际上就是字符的数组，所以也支持下标索引。**
  如果有字符串：name = 'i4leader' ,在内存中的实际存储如下：
|i|4|l|e|a|d|e|r|   
name[0]指"i"   
name[3]指"e"   
如果想取出部分字符，那么可以通过下标的方法，（注意在python中下标从0开始）   
**示例代码：**   
```
name = 'i4leader'
print(name)
print("-"*20)
print(name[0])
print("-"*20)
print(name[4])
```   
**输出结果：**
![xiabiao](images/day5-1.jpg)   


### 字符串常见操作


### 列表介绍


### 列表的循环遍历


### 列表的常见操作


### 列表的嵌套


### 元组


### 字典介绍


### 字典的常见操作1


### 字典的常见操作2


### 字典的遍历


### 公共方法


### 引用


### 作业


***
有兴趣一起学习的可以加我微信，大家一起交流。加我请备注“13天Python学习”
![mywechat](https://github.com/i4leader/python-learning-notes/blob/master/images/mywechat.jpeg)