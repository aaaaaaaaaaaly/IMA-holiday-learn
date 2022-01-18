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

### 列表

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

### 元组

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

### 字符串

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

如果要把他转化为一个列表，使用`list(reversed(number))转化



##### enumerate()

枚举。(**index**,元素)的列表

![](https://s4.ax1x.com/2022/01/18/70BrLR.png)



##### zip()

- 返回一个迭代器对象，需要转化为列表

![](https://s4.ax1x.com/2022/01/18/70BIOA.png)



------

### 函数















































