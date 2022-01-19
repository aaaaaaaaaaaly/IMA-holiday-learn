## python复习

### 操作符

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

​             not>and>or

------

### 分支与循环

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

### 列表（list）

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

### 元组（tuple）

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

### 字符串（str）

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

### 字典

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





































