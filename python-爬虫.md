# python复习

## 操作符

#### 算术操作符

** ：幂运算

// ：保留整数的除法

/  ：保留小数的除法

% ：模运算

+，- ，*

#### 比较操作符

![](https://s4.ax1x.com/2022/01/18/7wLsfS.png)

#### 逻辑操作符

and：全真才真

or：全假才假

not：一元操作符

#### 优先级问题

![](https://s4.ax1x.com/2022/01/18/7wL7pF.png)

**注意**：当幂运算左侧是一元运算符的时候，优先级逼幂运算高；当右侧是一元运算符的时候，优先级比他低

             not>and>or

------

## 分支与循环

分支：if-else语句；if-elif-else语句；

循环：while-else语句。

循环：for循环，range()

![](https://s4.ax1x.com/2022/01/18/7wxDxO.png)

![](https://s4.ax1x.com/2022/01/18/7wziw9.png)

分支循环嵌套：略。

break 和coontinue:略

**条件表达式：三元操作符**

```python
# x是条件
# y是 运算表达式1
# z是 运算表达式2
# 如果x为真，运行y，否则运行z
y if x else z
```

![](https://s4.ax1x.com/2022/01/18/7wvK1O.png)

断言：assert

![](https://s4.ax1x.com/2022/01/18/7wvJAI.png)



因为没有花括号，是通过**tab空格键来实现分层级**

------

## 基础

### 列表（list）[]

（数组）

![](https://s4.ax1x.com/2022/01/18/7wz6pV.png)

可以存储多种数据类型

#### 创建列表

```python
member=['as','bs','cs','ds']
member2=[1,'as','你好',3.14,[1,2,3]]
#空列表
empyt=[]
```



#### 向列表里添加元素

##### .append()

```pyhon
member.append()
```

![](https://s4.ax1x.com/2022/01/18/70Sa36.png)

##### .extend()

```
member.extend()
# 参数为列表，用一个列表扩展另一个列表
```

![](https://s4.ax1x.com/2022/01/18/70pC5R.png)

##### .insert()

```
member.insert(下标，元素)
```

![](https://s4.ax1x.com/2022/01/18/709Foj.png)

#### 从列表里获得元素

和数组一样，利用元素的索引值从列表获得单个元素

```
member[index]
```



#### 从列表删除元素

##### .remove()

```
member.remove(元素)
# 需要知道元素具体的值才能删除
```

##### del

```
del member[index]
del member # 把整个列表删除
```

##### .pop（）

- 默认下，把最后一个元素弹出来

![](https://s4.ax1x.com/2022/01/18/70nuXd.png)

- 也可以通过索引值删除

```
member.pop(1)
# 表示把索引值为1的元素删除
```



#### 列表分片（slice）

```
member[1:3]
#获得原列表的拷贝
# 获得下标为1，到下标为3，但是取不到下标为3的元素
member[:3]
member[:]
```



#### 列表的操作符

比较，逻辑，连接，重复，成员关系等操作符

- list.count(元素)
- list.reverse( )头尾颠倒
- list.index(元素，start，end)

- list.sort(reverse=False)

  reverse=False表示不逆序

  

------

### 元组（tuple）(,)

（带上枷锁的列表）

**和列表比较来学习**

**不能随意修改，创建的时候用（,），列表用的是[]**



- ()并不一定为元祖，还要加“ ，”

![](https://static01.imgkr.com/temp/b4cb4978533b462ea056473de7b45a8f.png)

![](https://static01.imgkr.com/temp/ba674d88fc964ed0a1ae1b7f85e3687e.png)

![](https://static01.imgkr.com/temp/e713021c3dc448c194128f4e775532c0.png)



- 创建空元组

```
empty=()
```

- 更新

元组是不能随意改变的，可以通过拷贝更新

![](https://static01.imgkr.com/temp/d67e7a51fce341e08c39aff63d969251.png)

- 删除

```
del temp
```

- 和元组相关的操作符

+：拼接

*：重复

in，not in：成员操作符

逻辑，比较操作符......



------

### 字符串（str）" "

字符串不能随意修改，修改方法和元组一样

![](https://static01.imgkr.com/temp/6eb80abbc940440388283c407906dbaa.png)

![](https://static01.imgkr.com/temp/2fe5ad1c1df84a4b8a4076b41cdfb636.png)

python机制：当没有标签指向，就会被回收

- 字符串的其他多种方法

![](https://static01.imgkr.com/temp/de9136fad6fa43a5a432008335e6deb8.png)



- 格式化

format( ),{里面是replacement，通常默认为为下标}

![](https://static01.imgkr.com/temp/baa090fdc7f240a1960e4326880be6d6.png)

- 如图所示，{0}，已经成为replacement，所以后面的不打印

![](https://static01.imgkr.com/temp/590a399c15374df18518a806fbc4d24a.png)

- ：表示下标为0,"0:"    .1f表示保留小数

![](https://s4.ax1x.com/2022/01/18/70t5VS.png)



![](https://s4.ax1x.com/2022/01/18/70NEqK.png)

- 例子

![](https://s4.ax1x.com/2022/01/18/70N3sP.png)

![](https://s4.ax1x.com/2022/01/18/70NtIg.png)

- 精度

![](https://s4.ax1x.com/2022/01/18/70NRJJ.png)

- 例子，5表示整个字符串加起来等于5个占位，保留1位小数

![](https://s4.ax1x.com/2022/01/18/70UkWj.png)

- 转义字符

![](https://s4.ax1x.com/2022/01/18/70as5F.png)



------

### 序列

#### 回顾

把列表，元组，字符串统称为序列

![](https://s4.ax1x.com/2022/01/18/70aH8H.png)

#### 内置方法

##### list（）

```
list()# 无参
list(iterable)# 有参
```

- 把可迭代对象转化为列表

![](https://s4.ax1x.com/2022/01/18/70dqFU.png)



##### tuple([iterable])

- 把一个可迭代对象转化为元祖，与列表一样

  

##### str(obj)

- 把obj对象转化为字符串

  

##### len()

- 返回元素的长度

  

##### max()

- 返回序列或者参数集合中的最大值

  

##### min()

- 返回序列或者参数集合中的最小值

  

##### sum(iterable[,start=0])

- 返回序列 iterable和可选参数start的总和

  

##### sorted()

和list.sort()的实现一样



##### reversed()

倒序，返回一个迭代器对象

如果要把他转化为一个列表，使用`list(reversed(number))`转化



##### enumerate()

枚举。产生一个(**index**,元素)的列表

![](https://s4.ax1x.com/2022/01/18/70BrLR.png)



##### zip()

- 对象是两个列表，实现下标一致的元素合并，返回一个迭代器对象，需要转化为列表

![](https://s4.ax1x.com/2022/01/18/70BIOA.png)



------

### 函数

#### 创建一个函数

语法：`def 函数名 ():`

函数调用：` 函数名 ()`     (函数定义需要在函数调用之前)

函数参数：由参数变量可以实现函数可变

```python
比如定义一个加法函数
def add (num1,num2):
    result=num1+num2
    print(result)
```

函数的返回值：需要关键字：return

```python
def add (num1,num2)：
    return (num1+num2)
print(add(1,2))
>>>3
```

#### 形参和实参

和c，c++一样：

![](https://s4.ax1x.com/2022/01/19/7DK8yD.png)

#### 函数文档

- 类似注释

```python
def add (num1,num2)：
    '这是一个实现加法的函数'
    return (num1+num2)
#正常打印的时候不会显示
#调用函数文档
add._doc_
help(add)
#或者
print._doc_
help(print)
```

#### 关键字参数

```python
def saysome(name,words):
    print(name+'->'+words)
    
#一种
saysome('ashelly','上课')
#第二种
saysome('上课'，'ashelly')
#第二种出现错误
#改正
saysome(words='上课',name='ashelly')
```

#### 默认参数

```python
# 定义的时候给默认值
def saysome(name='ashelly',words)
```

#### 收集参数

```python
def saysome(*params):
#加上* ，参数长度可变

def saysome(*params,exp=8)
# exp=8表示，变量exp固定大小为8
```

![](https://s4.ax1x.com/2022/01/19/7DM2uD.png)

参数用元组打包起来，用逗号隔开；上面示例中的params就是一个长度不定的元组

------

### 函数与过程

- 函数（function）：有返回值
- 过程（procrdure）：简单，特殊，没有返回值

python中没有过程，因为即使函数未定义return语句，也会返回'none',或者'type'

![](https://s4.ax1x.com/2022/01/19/7DlMYn.png)

#### 再谈返回值

c++，c中都是会确定返回值类型

而python是**动态确定   返回值类型，返回值数量**

python可以通过列表，或者元组打包返回值：

![](https://s4.ax1x.com/2022/01/19/7DldYR.png)

#### 函数变量的作用域问题

和c，c++的情况一样：

局部变量：（local variable）

全局变量：（global variable）

- 如果试图在函数内修改全局变量，python机制会创建一个新的变量，和该全局变量同名，来托放这个新赋的值。而全局变量的值并不会被改变

![](https://s4.ax1x.com/2022/01/19/7D3iKf.png)

- 全局变量在整个代码中都可以访问到，但是不要试图在（局部）函数内对全局变量进行修改；但是可以访问全局变量的值



#### 内嵌函数和闭包

全局变量在函数被修改，python机制会用屏蔽（shadowing)来保护全局变量

**用global关键字修改就可以实现对全局变量的修改**

![](https://s4.ax1x.com/2022/01/19/7D8wfs.png)

![](https://s4.ax1x.com/2022/01/19/7D8r60.png)

**内嵌函数**

在函数定义内部嵌套定义一个函数

- 失效同时打印两个函数

![](https://s4.ax1x.com/2022/01/19/7DGJ3R.png)

![](https://s4.ax1x.com/2022/01/19/7DGtjx.png)

- 成功打印两个函数

![](https://s4.ax1x.com/2022/01/19/7DGaDK.png)

**注意：内嵌函数只能在函数内部内被调用，不能在外部调用**



**闭包（closure）**

闭包，又称闭包函数或者闭合函数，其实和前面讲的嵌套函数类似。

不同之处在于，闭包中**外部函数返回的不是一个具体的值，而是一个函数**。

一般情况下，返回的函数会赋值给一个变量，这个变量可以在后面被继续执行调用。

![](https://s4.ax1x.com/2022/01/19/7DYKkF.png)

不仅是内嵌函数，返回值也是函数，调用闭包函数的两种方式（以上）。

内嵌函数要返回值，外部函数返回内部函数，就是返回内部函数返回的值

**容易出现的错误**：

![](https://s4.ax1x.com/2022/01/19/7DY51s.png)

内嵌函数，将fun1的内部环境当做外部环境，x对于fun2也是全局变量，因此不能修改全局变量，python机制会把x当作未定义的局部变量



**改进**

- 因为列表不存在栈中，不会被屏蔽，所以将x定义为列表再在内部函数调用

![](https://s4.ax1x.com/2022/01/19/7DtKDP.png)

- 事实上，python已经在这方面实现改进

使用关键字**nonlocal**在内部函数声明，就可以指向外部函数的变量x，并且实现修改

![](https://s4.ax1x.com/2022/01/19/7DtRDx.png)

------

### lambda表达式

![](https://s4.ax1x.com/2022/01/19/7DaGCD.png)

在**冒号**前面是函数参数

在**冒号**后边是函数的返回值

- 调用：赋值给一个变量，变量加（）传入值

![](https://s4.ax1x.com/2022/01/19/7Day8g.png)

![](https://s4.ax1x.com/2022/01/19/7DajVx.png)

#### 介绍两个内置函数

##### filter()

过滤器

![](https://s4.ax1x.com/2022/01/19/7DdqfS.png)

filter（过滤对象，被筛选对象）

none表示假，需要转化为可迭代对象才能打印

![](https://s4.ax1x.com/2022/01/19/7Dw31e.png)

![](https://s4.ax1x.com/2022/01/19/7D0oPf.png)

```python
# 用lambda简化
b=list(filter(lambda x:x%2,range(10)))
```

##### map()

映射

![](https://s4.ax1x.com/2022/01/19/7DBowR.png)

把range（5）中的元素，按照lambda的式子要求重新运算成新的列表（这里转化为可迭代对象，列表）

------

### 递归

类似c，c++

![](https://s4.ax1x.com/2022/01/19/7DrSvF.png)

斐波那契数列递归实现：（分治思想）

![](https://s4.ax1x.com/2022/01/19/7D6J8x.png)

汉诺塔

![](https://s4.ax1x.com/2022/01/19/7DRmFJ.png)

------

### 字典(dict) { }

是映射类型，类似字典上查询对应页码可以找到该查询对象

![](https://s4.ax1x.com/2022/01/19/7DRs0S.png)

#### 创建和访问字典

字典是大括号，不是数据类型，是映射类型

元素的定义`key：value`

![](https://s4.ax1x.com/2022/01/19/7DWGj0.png)

- 将元组转化为字典

![](https://s4.ax1x.com/2022/01/19/7DWf4H.png)

- 也可以通过之间指定创建字典

![](https://s4.ax1x.com/2022/01/19/7Df7W9.png)

**注意**:小甲鱼，苍井空不能加 " "

- 重新给key赋值

![](https://s4.ax1x.com/2022/01/19/7Dhdp9.png)



#### 内置函数

- fromkeys（），创建并且返回一个**新的字典**，s是key，第二个参数默认为none

![](https://s4.ax1x.com/2022/01/19/7DhT78.png)

- 例子

![](https://s4.ax1x.com/2022/01/19/7D4Yut.png)

##### 访问字典的方法

###### keys()

提取字典的键：key

![](https://s4.ax1x.com/2022/01/19/7D5e2j.png)

![](https://s4.ax1x.com/2022/01/19/7D5uMn.png)

###### values()

同keys（），提取字典的值

###### items()

同上，把所有项打印出来，形如：（key，values）

![](https://s4.ax1x.com/2022/01/19/7D5UMR.png)

###### get（）

定义当字典内没有这个项的时候，如何打印

![](https://s4.ax1x.com/2022/01/19/7D5czd.png)

###### 利用成员资格操作符判断该项是否存在

in

not in

**成员资格操作符，在序列中是用值判断，但是在字典中是用key判断**

![](https://s4.ax1x.com/2022/01/19/7DI9W4.png)

###### 清空.clean（）

使用   `dict.clean()`

###### 深拷贝浅拷贝

copy是浅拷贝，赋值不是浅拷贝

![](https://i.w3tt.com/2022/01/19/T1jzl.png)

###### .updata()

更新字典：b也是字典

![](https://i.w3tt.com/2022/01/19/T12Pg.png)

------

### 集合（set）

集合内数字唯一，会自动把重复的数字剔除；集合无序，所以不能通过`index`来找元素

- 创建结合

  直接用花括号

  利用`set（）`实现转化

```python
set1=set（list）
#可以把列表转化为集合

num1={1,2,3,4,1，2}
num1
>>>{1,2,3,4}
```

#### 集合元素的增加和删除

##### .add()

##### .remove()

#### 定义不可变集合

`rozenset()`,创建即可无法添加或者删除



------

## 文件

![](https://s4.ax1x.com/2022/01/20/76p0Lq.png)

![](https://s4.ax1x.com/2022/01/20/76pfyR.png)

- 使用完文件应及时关闭

```python
# 把文件转化为列表
list(f)
#迭代读取
lines=list(f)# 转化为列表
for each_line in lines:
    print(each_line)
#或者
for each_line in f:# 效果一致
    print(each_line)
```

- 示例

![](https://s4.ax1x.com/2022/01/20/769ynI.png)

- 以‘w',即写入的方式打开文件，覆盖



### 实际操作

#### 字符串操作方法

![](https://s4.ax1x.com/2022/01/20/76PQy9.png)

- split默认以空格划分

![](https://s4.ax1x.com/2022/01/20/76i8Xj.png)

- 目标：将文件内的说话内容分开为对话者文件，记录分别说的话
- 先把内容分别放到两个list，使用到`split`,使用方法append(),实现记录
- 文件名字记录，创建文件（以’w'打开），以`.writelines`将列表的内容写入
- 及时关闭文件

**优化，封装实现功能分割，更条理**

![](https://s4.ax1x.com/2022/01/20/76FaqA.png)

------

### 文件系统

#### 模块

![](https://s4.ax1x.com/2022/01/20/76F2rj.png)

- 需要的时候查文档

![](https://s4.ax1x.com/2022/01/20/76kdlF.png)

- 模块 `pickle `可以实现对象持久化储存
- 通过文件保存，相关查文档

```python
pickle_file=open('city_data.pkl','wb')
# 以文本的形式打开，覆盖写入
piickle.dump(city,pickle_file)
#pickle.dump(obj, file[, protocol])

#序列化对象，并将结果数据流写入到文件对象中。
#参数protocol是序列化模式，默认值为0，表示以文本的形式序列化。#protocol的值还可以是1或2，表示以二进制的形式序列化。
pickle.close()
pickle_file.close()
```

- load()方法

```
pickle.load(file)
　　反序列化对象。将文件中的数据解析为一个Python对象。
```

------

### 异常处理

- ***（小甲鱼：33，34集）**

![](https://s4.ax1x.com/2022/01/20/76VGTA.png)

**try语句**

```
try：
except：
else：
finally:
  f.closse()
```

1、使用try/except/else结构，try中存放**需要运行的代码**；

2、except 中**存放处理异常的代码**；

3、else里存放try语句**未发生异常时执行的代码**。

```
try:
finally:
```

python总会执行finally子句，无论try子句执行时是否发一异常。
1、如果没有发生异常，python运行try子句，然后是finally子句，然后继续。
2、如果在try子句发生了异常，python就会回来执行finally子句，然后把异常递交给上层try，控制流不会通过整个try语句。



**with语句**

with 语句适用于对资源进行访问的场合，确保**不管使用过程中是否发生异常都会执行必要的“清理”操作**，释放资源

比如文件使用后**自动**关闭／线程中锁的自动获取和释放等。

- 容易出现问题的代码（如果文件不存在会报错）

```
try:
    f = open('xxx')
except:
    print('fail to open')
    exit(-1)
try:
    do something
except:
    do something
finally:
    f.close()
```

- 有with语句的代码

减少冗长，还能自动处理上下文环境产生的异常

```
try：
with open("１.txt") as f:
except:
    print('fail to open')
    exit(-1)
try:
    do something
except:
    do something
```

------

## 界面入门

**easygui**（模块）

- 文档学习啊啊啊

界面学习势在必行（easyx or qt）🦍🦍

![img](C:/AppData/Local/Temp/SGPicFaceTpBq/21864/125D4C97.jpg)

------

## 类和对象

### 基础

**对象=属性+方法**

**属性：**变量

**方法：**函数

**类名要以大写字母开头**

- 和c++类和对象的创建和调用相似

![](https://s4.ax1x.com/2022/01/20/76QGGj.png)

- 封装，基础，多态

**继承可以继承方法**

![](https://s4.ax1x.com/2022/01/20/76Qqyt.png)

这里，list的方法被继承，所以类Mylist的对象可以使用append和sort

方法

**pass是占位符**



**多态**

![](https://s4.ax1x.com/2022/01/20/76lYkD.png)

就是同名函数的多种实现



### 面向对象编程

**ooa：面向对象分析**

**oop：面向对象编程**

**ood：面向对象设计**

**self相当于c++的this指针**，实现**指向**自身变量

![](https://s4.ax1x.com/2022/01/20/76szAe.png)

#### ___init__-(self)方法

（类似，c++中的构造函数，同名重写方法，创建对象的时候会被调用一次）

 定义了 `__init__()` 方法后，类的**实例化操作会自动调用该方法**

![](https://s4.ax1x.com/2022/01/20/76yIDf.png)

#### 公有和私有

name mangling:名字重造

在python中定义私有变量只需要在变量名或者函数名前加上**"__"**,两个下划线，那么这个函数或者变量就**会变为私有**

但是其实可以通过`_类名__成员变量`找到这个私有类

![](https://s4.ax1x.com/2022/01/20/76gicR.png)

#### 继承

![](https://s4.ax1x.com/2022/01/20/76Rpl9.png)

**继承是通过 class 类名 （父类名）**

python中没有继承的关键字

**多重继承**

语法`class 类名 (父类1，父类2)·



#### **random（）函数**

**random()** 方法返回随机生成的一个实数，它在[0,1)范围内。

以下是 random() 方法的语法:

```
import random

random.random()
```

**注意：**random()是不能直接访问的，需要**导入 random 模块，然后通过 random 静态对象调用该方法。**



#### 示例

子类重写父类的方法或者实例化，就会把父类相应的方法或者实例化覆盖掉

![](https://s4.ax1x.com/2022/01/20/76Wlv9.png) 

这里shark（）init重写（实例化对象的时候自动调用）

导致shark类中没有成员x，y，因为父类的实例化被覆盖

##### 解决问题

- 第一种方法

![](https://s4.ax1x.com/2022/01/20/76Wf2Q.png)

只需要在重写实例化的时候，首先对父类的示例话继承

语法:`父类名.-init-(self)`

- 第二种方法

使用`super()`函数

语法：`super().-init-()`

![](https://s4.ax1x.com/2022/01/20/76fmqI.png)



------

#### 组合

![](https://s4.ax1x.com/2022/01/20/76hFwq.png)

**组合就是把类的实例化放到一个新类里面，不需要继承**





## 类，类对象和实例对象

![](https://s4.ax1x.com/2022/01/20/764sbR.png)

![](https://s4.ax1x.com/2022/01/20/7647VI.png)

- 先把c的count赋值，这个时候会多出一个实例属性并且**把原来那个类属性覆盖**



**属性和方法的名字相同，属性会把方法的名字覆盖掉**

![](https://s4.ax1x.com/2022/01/20/765sSS.png)

- python是不需要声明对象，那么
- `c.x=1`表示初始化一个变量，属于c，就是c的成员
- 这个时候会把同名的`x()`方法覆盖



### 绑定

python严格要求方法需要有实例才能被调用，这种限制其实就是python所谓的绑定概念

**self**

![](https://s4.ax1x.com/2022/01/20/76op40.png)

### 一些BIF（build in Functions）

#### issubclass（class，classinfo）

如果class是classinfo的子类，就返回True

classinfo可以是类对象组成的元组，只要class是其中任何一个候选类的子类，就会返回True



#### isinstance（object，classinfo）

检查object是否为类的实例对象

如果第一个参数不是对象，会永远返回False；

如果第二个参数不是元组或者类，会抛出一个typerror的异常



#### hasattr（object，name）

测试对象是否有属性，name是属性名，object是对象



#### gettattr（object，name[,defaulf]

返回对象指定的属性值



#### setattr(object,name,value)

设置指定对象的属性



#### delattr(object,name)

删除指定对象的属性



#### property（fget=None，fset=None，fdel=None,doc=None)

通过属性设置属性



**等等需要的时候查文档**

------

## 魔法方法

### 构造和析构

![](https://s4.ax1x.com/2022/01/20/76jxQ1.png)



### -new-（cls[,...])

![](https://s4.ax1x.com/2022/01/20/76xHC4.png)

字符串str是不可以被改变的类型，将传入的字符串改为大写，可以调用new方法，在new方法里面调用upper（）方法，获得新的字符串，返回时，调用new方法把刚才新的string返回



### -del-（self）

python 的垃圾回收机制

**示例**

![](https://s4.ax1x.com/2022/01/20/7c9RiT.png)

del掉标签不会调用del，只有对象被del掉才行

类似c++的析构

### 算术运算

**工厂函数就是类对象**

![](https://s4.ax1x.com/2022/01/20/7cPwuj.png)

**类似c++重载**

![](https://s4.ax1x.com/2022/01/20/7cPRv4.png)

其中self指自身，other表示和self实现运算的另一个变量

**示例**

![](https://s4.ax1x.com/2022/01/20/7ciOYV.png)

**解决**

![](https://s4.ax1x.com/2022/01/20/7cF9m9.png)



（等等，运算符重载）

**反运算：a+b，当a无法实现，就会让b实现**

![](https://s4.ax1x.com/2022/01/20/7gK9ln.png)

**示例**：

![](https://s4.ax1x.com/2022/01/20/7gKWXq.png)

这里1没办法调用，就会启动b的反运算

**还有很多其他方法magically**

![](https://s4.ax1x.com/2022/01/20/7gMu4g.png)

------



## 简单定制

**要求**

![](https://s4.ax1x.com/2022/01/20/7gMgUO.png)

**需要的知识**

![](https://s4.ax1x.com/2022/01/20/7gQAG4.png)

**time.localtime([secs])**

接收时间戳，返回当地当下时间**元组t**

![](https://s4.ax1x.com/2022/01/20/7gQwo8.png)

**代码实现**

```python
import time as t
class Mytimer():
    def _init_ (self):
        self.prompt="计时未开始"
        self.lasted=[]
        # self.start=0注意不要和方法名字重复，否则变量会覆盖方法
        self.begin=0
        self.end=0
    def _str_ (self):
        #当使用print输出对象的时候，只要自己定义了__str__(self)方         法，那么就会打印从在这个方法中return的数据
        return self.prompt
    _repr_=_str_
    #重写repr，str让对象创建后调用可以直接显示结果
    #开始计时
    def start(self):
        self.begin=t.localtime()
        print("开始计时")
    #停止计时
    def stop(self):
        if not self.begin:
            print("调用start开始计时")
        else:
            
          self.end=t.localtime()
          self._clas()#调用方法
           print("计时结束")
    #内部方法，计算运行时间
    def _clas(self):
        self.lasted=[]
        self.prompt="总共运行了:"
        for index in range(6):
            self.lasted.append(self.stop[index]-self.start[index])
            self.prompt+=str(self.lasted[index])
       # print(self.prompt)
    #为下一轮做准备
        self.begin=0
        self.end=0
```



 **def _str_ (self)**:
       ** 当使用print输出对象的时候，只要自己定义了__str__(self)方         法，那么就会打印从在这个方法中return的数据 **





# 爬虫

## 基本篇

**基本流程**

- 连接到特定网址，抓取资料
- 解析资料，取得想要的部分



1. **Request**自动爬取页面提交请求
2. **robots.txt**爬虫排除标准
3. **Beautiful Soup**解析HTMl页面
4. 利用**正则表达式**详解提取页面关键信息



**抓取资料**

尽可能让程序模仿一个普通使用者的使用情况

- 如果是json模式的资料，用python内建的json模板来抓取即可
- 但是大部分是HTML格式的资料：使用第三方套件 **Beautifulsuop**来解析





## 基本代码

```python
# 抓取网页的原始码（HTMl）
import urllib.request as req
# 利用内置套件做网络的连线
url="https://movie.douban.com/top250"
# 建立一个Request物件，附加Request Headers的资讯
request=req.Request(url,headers={
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.80 Safari/537.36 Edg/98.0.1108.50"
})
with req.urlopen(request) as response:
    data=response.read().decode("utf-8")
#print(data)
import bs4#做解析
root=bs4.BeautifulSoup(data,"html.parser")
#会用html.parser帮我们做解析
#比如要获取网页的标题，用root代表整份网页，title是一个网页的标签
print(root.title.string)#.string表示抓到标签title里面的文字,就抓到网页的标题
"""
抓取文章的标题,需要观察源码文章标题的共同点:
<div class=''>
</div>
就是共同点
"""
titles=root.find_all("span",class_="title")
"""
""内是要找寻的标签名称，class_="title"是筛选的条件
.find_all就是找到所有符合条件的标签
会返回列表
"""
for title in titles:
    print(title)
"""
这样只会提取文字，不会附加<span>等代码
 titles表示span
.a代表符合条件的会被打印的title
.string代表内容
"""
```





## Requests库入门

### 主要有7个方法

#### requests.request()

构造一个请求，支撑一下各方法的基础方法



#### requests.get()

获取HTML网页的主要方法，对应于HTTP的GET  ![](https://s4.ax1x.com/2022/02/15/HRkFPK.png)![](https://s4.ax1x.com/2022/02/15/HRFN4K.png)



- Response对象的属性：

![](https://s4.ax1x.com/2022/02/15/HRk8xg.png)

其中：

`encoding`和`apparent_encoding`有内层区别

![](https://s4.ax1x.com/2022/02/15/HRAies.png)

#### requests.head()

获取HTML网页头信息的方法，对应于HTTP的HEAD

![](https://s4.ax1x.com/2022/02/15/HRJYV0.png)

#### requests.post()

想HTML网页提交POST请求的方法，对应于HTTP的POST

![](https://s4.ax1x.com/2022/02/15/HRJaPU.png)

#### requests.put()

向HTML网页提交PUT请求的方法，对应于HTTP的PUt

![](https://s4.ax1x.com/2022/02/15/HRYOTx.png)

#### requests.patch()

向HTML网页提交局部修改请求，对应于HTTP的PATCH

#### requests.delete()

向HTML的网页提交删除请求，对应于HTTP的DELETE

### 爬取网页的通用代码框架

理解代码框架： **异常需要重视**

#### 了解HTTP协议

![](https://s4.ax1x.com/2022/02/15/HREM38.png)



HTTP协议**有相应的方法：**

![](https://s4.ax1x.com/2022/02/15/HRZnl8.png)

- 其中，了解put和post的区别：

![](https://s4.ax1x.com/2022/02/15/HRQlvt.png)



HTTP协议的方法与Requests库**对应**

![](https://s4.ax1x.com/2022/02/15/HRQlvt.png)



#### 了解Requests库的异常

![](https://s4.ax1x.com/2022/02/15/HRlvY4.png)

有一个函数方法：

**r.raise_for_status()**

![](https://s4.ax1x.com/2022/02/15/HR1QnP.png)



#### 爬取网页的代码框架

![](https://s4.ax1x.com/2022/02/15/HR1aXq.png)

```python
import requests
def getHTMLTXT(url):
    try:
        r=requests.get(url,timeout=30)
        r.raise_for=status()
        r.encoding=r.qppqrent_encoding
        return r.text
    expect:
        return"异常处理"
if__name__=="__main__":
    url="heep://"
    print(getHTMLTXT(url))
```

**r.raise_for_status()**

表示：如果转台不是200，引发HTTPError异常



### 对**kwargs参数的理解

分为两种情况：

- **requests.request(method,url,kwargs) **

**kwargs，有13个参数**

![](https://s4.ax1x.com/2022/02/15/HRG96s.png)

**method，包含Requests的7种方法**

![](https://s4.ax1x.com/2022/02/15/HRGzE6.png)

- **requests.method(url,kwargs)**



#### params

![](https://s4.ax1x.com/2022/02/15/HRtb8S.png)



#### data



#### json

![](https://s4.ax1x.com/2022/02/15/HRNmUx.png)



#### headers

![](https://s4.ax1x.com/2022/02/15/HRNfRU.png)

可以更换选择浏览器



#### cookies

![](https://s4.ax1x.com/2022/02/15/HRNjzD.png)



#### auth



#### files

![](https://s4.ax1x.com/2022/02/15/HRUeyQ.png)



#### timeout

![](https://s4.ax1x.com/2022/02/15/HRaKje.png)



#### proxies

![](https://s4.ax1x.com/2022/02/15/HRaN38.png)



#### allow_redirects

#### stream

#### verify

#### cert

![](https://s4.ax1x.com/2022/02/15/HRa0Bj.png)





### 单元小结

最常用的，requests.get(),request.head()

![](https://s4.ax1x.com/2022/02/15/HRwdTs.png)

最基本的代码框架

![](https://s4.ax1x.com/2022/02/15/HRwcXF.png)





# 网络爬虫引发的问题

![](https://s4.ax1x.com/2022/02/16/HfQdxA.png)

## Robots协议

作用：告诉网络爬虫哪些可以抓取，哪些是不允许的

![](https://s4.ax1x.com/2022/02/16/HflOk8.png)

## Robots协议的遵守方式

网络爬虫：自动或人工识别Robots协议，再进行内容爬取

约束性：Robots协议是建议当时非约束性，网络爬虫可以不遵守，但是存在法律风险

![](https://s4.ax1x.com/2022/02/16/Hf8PiT.png)



# 实战

## 京东商品页面

```python
import requests
url="https://item.jd.com/2967929.html"
try:
    r=requests.get(url)
    r.raise_for_status()
    r.encoding=r.apparent_encoding
    print(r.text[:1000])
except:
    print("爬取失败")    
```



## 亚马逊商品页面

```python
import requests
"""
r.request.headers，查找头部发现显示为python
所以需要用到headers字段改头部信息
"""
url="https://www.amazon.cn/gp/product/B01M8L5Z3Y"
try:
    kv={'user-agent':'Mozilla/5.0'}#定义新的头部键值对
    r=requests.get(url,headers=kv)#使用headers字段
    r.raise_for_status()
    r.encoding=r.apparent_encoding
    print(r.text[1000:2000])
except:
    print("爬取失败")
```



## 百度/360搜索关键字提交

**搜索引擎关键字提交有接口：**

比如，百度关键词接口：https://www.baidu.com/s?wd=keyword

​            360关键词接口：https:///www.so.com?q=keyword

- 我们可以修改连接keyword部分，就可以提交关键词



百度搜索全代码

```python
import requests
url="https://www.daidu.com/s"
keyword="python"
try:
    kv={'wd':keyword}
    r=requests.get(url,params=kv)
    print(r.request.url)
    r.raise_for_status()
    print(len(r.text))
except:
    print("爬取失败")
```

360搜索全代码

```python
import requests
url="https://www.so.com/s"
keyword="python"
try:
    kv={'q':keyword}
    r=requests.get(url,params=kv)
    print(r.request.url)
    r.raise_for_status()
    print(len(r.text))
except:
    print("爬取失败")
```





## 网络图片的爬取和存储

![](https://s4.ax1x.com/2022/02/16/HfvcWQ.png)

```python
import requests
path="D:/abc.jpg"
url="  "#填入该照片的web地址
r=requests.get(url)
print(r.status_code)
with open(path,'wb')as f:
    f.write(r.content)
    #f.write(r.content)把文件返回二进制形式
f.close()#把文件关闭
```



**网络爬取的全代码**

```python
import requests
import os
url=" "#要爬取的图片web地址
root="D://pics//"#本地存储爬取的图片的根目录
path=root+url.split('/')[-1]
#取url最后一个/后的部分,就是图片的名字
try:
    if not os.path.exists(root):
        os.mkdir(root)
    if not os.path.exists(path):
        r=requests.get(url)
        with open(path,'wb') as f:
            f.write(r.content)
            f.close()
            print("文件保存成功")
    else:
        print("文件已经存在")
except:
    print("爬取失败")
```



## IP地址归属地自动查询

iP138的网站提供这样的功能：查询ip地址

iP138网站的网址：http://m.ip138.com/ip.asp?ip=ipaddress

可以看出网页链接的特征，会在id后面显示地址，我们考科一通过url接口爬取地址信息

```python
import requests
url="http://m.ip138.com/ip.asp?ip=ipaddress"
#ip=ipaddress就是ip地址
#我们用requests的方法提交一个ip地址
url="http://m.ip138.com/ip.asp?ip"
r=requests.get(url+'202.204.80.112')
#检测一下状态码
print(r.status_code)
#查看返回文本的相关内容
print(r.text[-500:])
```



- ip地址查询的全代码

```python
import requests
url="http://m.ip138.com/ip.asp?ip"
try:
    r=requests.get(url+'202.204.80.112')
    r.raise_for_status()
    r.encoding=r.apparent_encoding
    print(r.text[-500:])
except:
    print("爬取失败")
```





# **Beautiful Soup**

## 库的基本元素

**Beaytiful Soup**能够解析HTML网页

![](https://s4.ax1x.com/2022/02/16/Hhd6Nd.png)

- 对标签树的理解

![](https://s4.ax1x.com/2022/02/16/Hhw9UJ.png)

- 库的引用

![](https://s4.ax1x.com/2022/02/16/Hhwl8I.png)

- Beautiful Soup和HTML对应，能解析HTML

![](https://s4.ax1x.com/2022/02/16/Hhw2a4.png)

- Beautiful Soup库解析器

![](https://s4.ax1x.com/2022/02/16/Hh08Y9.png)



## bs4的基本使用代码

```python
from bs4 import BeautifulSoup
soup=BeautifulSoup('<p>data</p>','html.parser')
```

- 比如例子

```python
import requests
url="http://python123.io/ws/demo.html"
r=requests.get(url)
demo=r.text
from bs4 import BeautifulSoup
soup=BeautifulSoup(demo,"html.parser")
print(soup.prettify())
```



## 获得tag元素的相关方法

```python
import requests
url="http://python123.io/ws/demo.html"
r=requests.get(url)
demo=r.text
from bs4 import BeautifulSoup
soup=BeautifulSoup(demo,"html.parser")
#print(soup.prettify())
# print(soup.title)
```

- 获取链接标签内容，用.a

```python
##获得a标签的名字
print(soup.a.name)
```

- 获取p标签内容，用.p

```python
#获得p标签的名字
print(soup.p.name)
```

- 查询父标签的信息，比如名字

```python
#获得a父标签的名字
tag=soup.a
print(tag.parent.name)
#查看a父标签的父标签是谁
print(tag.parent.parent.name)
```

- 用attrs来获取标签属性

```python
#用.attrs来获取标签属性
print(tag.attrs)
#由于它是一个字典，我们可以利用字典对每一个属性实现提取
#比如我们希望获得class属性的值
print(tag.attrs['class'])
print(tag.attrs['href'])
```

- 获取标签间的string内容

```python
#获取string内容
#获得a标签的内容
print(soup.a.string)
#获取p标签的内容
print(soup.p.string)
```

- 新的“汤”

```python
newsoup=BeautifulSoup("<b><!--This is a comment--></b><p>This is not a comment</p>","html.parser")
print(newsoup.b.string)
print(type(newsoup.b.string))
print(newsoup.p.string)
print(type(newsoup.p.string))
```



## 基于bs4库的HTML的内容遍历方法

### html的标签树

![](https://s4.ax1x.com/2022/02/16/Hhhxr4.png)

#### 下行遍历

![](https://s4.ax1x.com/2022/02/16/HhIMgf.png)

- contens举例

![](https://s4.ax1x.com/2022/02/16/HhoZsU.png)

- 使用遍历来抓取子孙节点的内容

![](https://s4.ax1x.com/2022/02/16/Hho1Rx.png)



#### 上行遍历

![](https://s4.ax1x.com/2022/02/16/Hhoaod.png)

- 上行遍历的代码，注意需要判断是否有父标签

![](https://s4.ax1x.com/2022/02/16/HhTPmD.png)



#### 平行遍历

![](https://s4.ax1x.com/2022/02/16/HhT3kj.png)

**标签的平行遍历是有条件的，所有的平行遍历必须，发生在同一个父节点下**

![](https://s4.ax1x.com/2022/02/16/HhTwBF.png)

- 举例

![](https://s4.ax1x.com/2022/02/16/HhT5AH.png)

- 平行遍历的代码

![](https://s4.ax1x.com/2022/02/16/HhTo4A.png)



### 总结

![](https://s4.ax1x.com/2022/02/16/Hh7ivV.png)



## 如何让HTML页面更友好的显示

**用prettify()打印**

![](https://s4.ax1x.com/2022/02/16/Hh7Qv6.png)

让标签层级关系体现



## 单元小结

bs4库提供的5种基本元素：

1. 标签：Tag
2. 标签的名字：Name
3. 标签的属性：Attributes
4. 标签之间的字符串：NavigableString
5. 标签内注释的字符串：Comment

bs4的遍历功能：

1. 下行遍历

- contents
- children
- descendants

  2.上行遍历

- parent
- parents

  3.平行遍历

- next_sibling
- previous_sibling
- next_siblings
- previous_siblings



# 信息标记的三种形式

信息的标记

![](https://s4.ax1x.com/2022/02/17/H5PLCt.png)

HTML简称超文本标记语言

![](https://s4.ax1x.com/2022/02/17/H5iCUs.png)



国际公认的信息标记有3种形式：XML，JSON，YAML



## XML的格式

和html相关的格式非常接近

![](https://s4.ax1x.com/2022/02/17/H5Fb1P.png)

空元素的时候可以实现缩写

![](https://s4.ax1x.com/2022/02/17/H5kHUJ.png)



## Json的格式

对信息的定义叫key，对信息的赋值叫value，都要用“”来括，如果是数字就不需要

![](https://s4.ax1x.com/2022/02/17/H5AJMV.png)

如果一个key对应多个value，用方括号【】括起来

![](https://s4.ax1x.com/2022/02/17/H5AdIJ.png)

键值对可以嵌套使用，此时采用大括号：

![](https://s4.ax1x.com/2022/02/17/H5ABGR.png)



## YAMl的格式

也采用键值对，但是是无类型，没有双引号

![](https://s4.ax1x.com/2022/02/17/H5AHL8.png)

通过缩进的方式表达所属关系：

![](https://s4.ax1x.com/2022/02/17/H5AxWn.png)

用“-”表达并列关系：

![](https://s4.ax1x.com/2022/02/17/H5E9yV.png)

用|表示整块数据，#表示注释：

![](https://s4.ax1x.com/2022/02/17/H5EEFJ.png)

总的来说：

![](https://s4.ax1x.com/2022/02/17/H5EVY9.png)



# 三种信息标记形式的比较

- ## xml是一种用尖括号，标签表达信息的标签形式

最早的通用信息标记语言，可扩张性好，但是繁琐，网络上的信息交互和传递

![](https://s4.ax1x.com/2022/02/17/H5Eglq.png)

举例：

![](https://s4.ax1x.com/2022/02/17/H5Qstf.png)







- ## json是一种用有类型的键值对标机信息的标签形式

信息有类型，适合程序处理（js），较简洁

移动应用云端和节点的信息通信，无注释

![](https://s4.ax1x.com/2022/02/17/H5QJfO.png)

举例：

![](https://s4.ax1x.com/2022/02/17/H5Qg1g.png)









- ## yaml是一种用无类型的键值对表达信息的标签形式

信息无类别，文本信息比较高，可读性好

各类系统的配置文件，有注释易读

![](https://s4.ax1x.com/2022/02/17/H5QtpD.png)

举例：

![](https://s4.ax1x.com/2022/02/17/H5QIA0.png)





# 信息提取的一般方法

**方法1**：完整解析信息的标机形式，再提取关键信息

XML，JSON，YAML

需要标机解析器

例如bs4库 的标签数遍历

优点：信息解析准确

缺点：提取过程繁琐，速度慢



**方法2**：无视标记形式，直接搜索关键信息

搜索：

对信息的文本查找函数即可

优点：提取过程简洁，速度比较快

缺点：提取结果准确性与信息内容相关



**融合方法**：结合形式解析与搜索方法，提取关键信息

XML，JSON，YAML搜索

需要标记解析器及文本查找函数



**实例：**提取HTML中所有url链接

思路：1）搜索到所有<a>标签

​            2）解析<a>标签格式，提取href后链接的内容



```python
from bs4 import BeautifulSoup
soup=BeautifulSoup(demo,"html.parser")
for link in soup.find_all('a'):
    print(link.get('href'))
```



# 基于bs4库的HTML内容查找方法

