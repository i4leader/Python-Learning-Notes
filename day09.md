
## day9-面向对象,异常处理
*** 
### 保护对象的属性
如果有一个对象,当需要对其进行修改属性的时候,2种方法:   
* 对象名.属性名 = 数据  ---->直接修改
* 对象名.方法() ---->间接修改   
    
为了更好的保存属性安全,即不能随意修改,一般的处理方法为
* 降属性定义为私有属性
* 添加一个可以调用的方法,供调用
    
```
#!/bin/bash/python3
#coding=utf-8
# 如果有(object)叫,新式类
# 原来的那种没有的,叫经典类
class People(object):

    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    def __str__(self):
        return "年龄为:" + str(self.__age)

    def getName(self):
        return self.__name

    def getAge(self):
        return self.__age

    def setName(self, newName):
        if len(newName) >= 5:
            self.__name = newName
        else:
            print("error:名字长度需要大于或者等于5")

    def setNewAge(self, newAge):
        if newAge>0 and newAge<80:
            self.__age = newAge

xiaoming = People("小明",18)

xiaoming.setNewAge(119)
print(xiaoming)
ageTemp = xiaoming.getAge()
print(ageTemp)
```   
输出结果:   
```
    年龄为:18
    18  
```   

### __del__方法
创建对象后,python解释器默认调用\_\_init\_\_()方法:   
当删除一个对象时,python解释器也会默认调用一个方法,这个方法为\_\_del\_\_()方法   
```
#!/bin/bash/python3
#coding=utf-8
import time
class Animal(object):

    # 初始化的事情
    def __init__(self, name):
        print('__init__方法被调用')
        self.__name = name


    # 结束之前要做的事情
    def __del__(self):
        print("__del__方法被调用")
        print("%s对象马上被干掉了..."%self.__name)

# 创建对象
dog = Animal("哈士奇")

# 删除对象
print("------1------")

dog1 = dog
dog2 = dog

print('---------2--------')
'''
说明1:
在python中,如果有多个变量保存了同一个对象,就相当于这个对象有3个名字.
但使用del删除的时候,就相当于把一个名字删除,如果使用了多次del把所有的名字删除掉,
只要一个对象没有了名字,那么python解释器就会把这个对象从内存
中进行删除,即会按到__del__方法被调用了
'''
del dog
del dog1
del dog2

print('-------3-------')
# 虽然没有调用__del__方法,那是谁调用的呢?
# python解释器,如果检测到一个对象没有任何用处了,那么就把这个对象kill掉
```   
   
### 继承介绍以及单继承

### 1.继承的概念

### 单继承

只要是一个对象一个类来自于单个叫单继承,来自于多个叫多继承.   
```
#!/bin/bash/python3
#coding=utf-8
import time
class Animal(object):

    # 初始化的事情
    def __init__(self, name = '动物', color = '白色'):
        print('__init__方法被调用')
        self.name = name
        self.color = color

    # 结束之前要做的事情
    def __del__(self):
        print("__del__方法被调用")
        print("%s对象马上被干掉了..."%self.name)


class Dog(Animal):
    # 初始化的事情

#    def __init__(self, name = '动物', color = '白色'):
#        print('__init__方法被调用')
#        self.__name = name
#        self.__color = color

    # 结束之前要做的事情
#    def __del__(self):
#        print("__del__方法被调用")
#        print("%s对象马上被干掉了..."%self.__name)

    def printInfo(self):
        print("名字是:%s"%self.name)
        print("颜色是:%s"%self.color)

wangcai = Dog()
wangcai.printInfo()
```   
运行结果:   
![继承](images/day8-8.jpg)   
   
#### 总结:
* 私有属性不会被继承,譬如__name以及__color;不能直接使用
* 如果通过继承的方法访问父类的私有属性是可以的
* 如果在子类中,自定义了一个方法,此方法不能访问父类中的私有属性
* 如果在方法名前面有2个下划线,那么这个方法就成了私有方法


### 多继承
```
#coding=utf-8
class Base(object):

    def test(self):
        print("---------Base test----------")

class A(Base):

    def testA(self):
        print("---------A test----------")

    def test2(self):
        print("---------A test----------")

class B(Base):

    def testB(self):
        print("---------B test----------")

    def test2(self):
        print("---------B test----------")

class C(A,B):
    pass

c = C()
#c.testA()
#c.testB()
c.test()
#可以查看C类的对象搜索方法时的先后顺序
print(C.__mro__) 
```   
![bianli](images/day8-10.jpg)   
   

* 按照"广度"进行遍历,即先遍历兄弟关系的类
    
### 重写父类方法与调用父类方法
#### 1. 重写父类方法 
所谓重写,就是子类中,有一个和父类相同名字的方法,在子类中的方法会覆盖掉父类中同名的方法   
```
#coding=utf-8
class Cat(object):
    def sayHello(self):
        print("hello----1")

class Bosi(Cat):
    # 在子类中重新编写方法,就叫做重写
    def sayHello(self):
        # 这就是调用父类的方法
        Cat.sayHello(self)  
        # super().bark()   ---> 这个也是调用父类的方法
        print("hello----2")

bosi = Bosi()

bosi.sayHello()
```   
运行结果:   
![fatherClass](images/day8-9.jpg) 
   

    
### 多态



### 类属性,示例属性



### 静态方法和类方法



### 异常介绍



### 捕获异常



### 抛出异常



***
有兴趣一起学习的可以加我微信，大家一起交流。加我请备注“13天Python学习”
![mywechat](https://github.com/i4leader/python-learning-notes/blob/master/images/mywechat.jpeg)