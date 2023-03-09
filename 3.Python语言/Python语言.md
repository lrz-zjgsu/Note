封装思想:保护权限;忽略底层和细节
面向对象和面向过程

1.机器语言→汇编语言→C语言→Python、Java等语言
2.跨平台性:
  .java文件→(javac(编译器))→.class文件→(JVM)→运行
  .py文件→.pyc文件→(虚拟机)→运行
3.编译性:源代码→机器码(一次编译)
  解释性:源代码→字节码→机器码(运行时调用)
4.编译器和解释器的语法标准

### 基本数据结构速记

+ 字符串(string)
  ```python
  str_1="Hello,World!"
  str_1[0]
  "H" #索引
  str_1[0:4:2]
  "Hlo" #切片
  len(str_1);max(str_1);min(str_1)
  str_1.count("H") #计数
  str_1.isupper();str_1.islower();str_1.isdigit() #判断大小写;判断数字
  str_1.upper();str_1.lower() #改变大小写
  str_1.strip();str_1.lstrip();str_1.rstrip() #去空格;去左侧空格;去右侧空格
  str_1.replace(<老字符串>,<新字符串>) #替换
  str_1.split(<分隔符>) #分隔,改为列表
  ```

+ 列表(list)

  ```python
  list_1=[1,2,3,"a","b","c"]
  索引和访问(index),切片(slice)
  元素和搜索(search)
  插入(insert),追加(append),扩展(extend)
  删除(delete/pop)
  排序(reserve/sort)
  可变,不唯一
  ```

+ 元组(tuple)

  ```python
  tuple_1=(1,2,3,4,5,)
  索引(index),切片(slice)
  不可变,不唯一
  #核心是","
  ```

+ 集合(set)

  ```python
  set_1={1,2,3,4,5}
  #差集:-;并集:|;交集:&;对称差集:^
  删除(remove)
  添加(add/update)
  可变,唯一,没有索引
  
  #空集合要用set(),注意数据类型转换
  ```

+ 字典(dict)
  ```python
  dict_1={"a":1}
  添加:dict_1[<键>]=<值>
  删除:dict_1.pop(<键>);del dict_1[<键>]
  ```

### 代码习惯和规则

#### 1.注释
```python
# 我是注释
print("Hello,world!") # 我是注释
```
#### 2.折行、换行、空格空行缩进
```python
print("Well\
 \
done!")
```
#### 3.命名
+ 不能是关键字
+ 开头为字母、"\_",其它为字母、数字、"\_"
+ 在命名时,变量一般这样:``pretty_girl_1`
  函数一般这样:`i_love_you_1`
  类、实例一般这样:`ChinesePerson`、`ChineseBoy`
  属性一般这样:`black_hair`;方法一般这样:`love_china`;常量一般这样:`MALE`
### 变量(variable)
+ 存储数据:在内存中开辟或复用内存地址,存储变量值,变量名指向此变量值
  1. 变量名
  2. 变量值:数据
  3. 若修改了变量值,相同类型数据会进行覆盖,不同类型数据会开辟新的内存地址
  4. 变量值的数据类型:``age:int`
+ 赋值语句,像下面这样:
```python
age=18
```
+ 删除关键字:`del`,可以删除变量,删除变量名,释放变量值的内存地址;不可以删除常量(literal)

___
1. 查数据类型函数:
   ```python
   type(age)
   ```
   转化数据类型函数:
   ```python
   int();float();complex();bool()
   str()
   bin();oct();hex()
   set();tuple();dict();list()
   ```
2. 查内存地址函数:
```python
id(age)
```
```python
# 两个重要的和内存地址相关的关键字
is
is not
```
3. 查变量长度:
```python
len(age)
```
### 语句
#### 1.顺序语句
+ 顺序语句
  ```python
  ...
  ```
#### 2.条件语句
+ 条件语句(if-elif-else语句)
  ```python
  if 条件表达式:
  	...
  elif 条件表达式:
      ...
  ...
  else:
      ...
  ```

#### 3.循环语句

+ 遍历循环语句(for-in语句)
  ```python
  for 变量 in 有序性数据:
      ...
  else:
      ...
  ```
+ 条件循环语句(while语句)
  ```python
  while 条件表达式:
      ...
  else:
      ....
  ```
+ `break`关键字语句:终止此循环语句
+ `continue`关键字语句:终止本次循环,提前开始下一次循环

#### 4.关键字

+ ```python
  pass
  ```

+ ```python
  as
  ```

+ ```python
  with
  ```

#### 5.异常处理语句

+ 异常:异常不是语法错误,是在运行程序时,Python解释器无法处理的问题
  ```python
  try:
      ...
  except (<异常>):
      ...
  # Exception包含所有常见异常
  # TypeError、ValueError等,是Exception的子类
  # 不常见异常,比如SystemExit,在执行exit()命令时触发
  ...
  (else):
      ...
  (finally):
      ...
  
  
  raise Exception("...") #报错语句
  ```

### 基本数据类型一

#### 1.字符串(string)
1. 格式:`'I_am_a_string'`、`"我是一个字符串"`
2. 转义字符:
          `\r`:回车
          `\\`:反斜杠
          `\n`:换行
          `\'`:单引号
          `\"`:双引号
      ```python
      r"我不需要写转义转义字符"
      ```
3. 
      ```python
      name_of_my_best_friend="Karl Marx"
      f"Hello,my friend,{name_of_my_best_friend}!"
      ```
___
+ 运算:
  1. 拼接:
     ```python
     frist_name="润泽"
     last_name="李"
     full_name=last_name+first_name
     ```
  
  2. 重复:
     ```python
     ten_times_of_my_name=full_name*10
     ```
  
  3. `in`:
     `not in`:
  
  4. 解码:
     编码:
     UTF-8:
     GBK:
     ASCII:
___
+ 有序性
  ```python
  a="abcdefghijklmnopqrstuvwxy"
  a[start=0:stop=-1:step=1] #取位于[start+1,stop-1]范围内的数,间隔为step,顺序为从左往右
  ```
+ 不可变性:变量值不可以修改
  ```python
  a.replace(<被替换的字符串>,<替换的字符串>,<替换次数>)
  a.strip()
  ```
  
#### 2.数字(number)

##### 2.1.整数(integer)、浮点数(float point number)
1. 整数格式:`1`、`1_000_000`
1. 浮点数格式:`0.123`
1. 十六进制数(hexadecimal number)格式:`0x123ABC`
   八进制数(octal number)格式:`0o1234567`
   二进制数(binary number)格式:`0b1001`
1. 科学计数法的浮点数格式:`1.1e-10`
___
1. `+`:加
   `-`:减
   `*`:乘
   `/`:除,结果的数据类型为浮点数(float)
   `//`:求余
   `%`:求模
   `**`:乘方
   `+=`
2. `>`:大于
   `<`:小于
   `==`:等于
   `!=`:不等于
   `>=`:大于等于
   `<=`:小于等于
3. `()`:优先级
4. `&`:按位且
   `|`:按位或
   `^`:按位异
   `~`:按位取反
   `<<`:左移:将被左移的值转化为二进制数值,向左移动一定位数,低位补0
   `>>`:右移:将被右移的值转化为二进制数值,向右移动一定位数,非负数则高位补0,复数则高位补1
5. 二进制表示所有整数:表正负位、表绝对值位、反码、补码

##### 2.2.复数(complex)

1. 格式:`0j`、`1j`、`3+4j`、`(3+4j)`
___
1. `+`:加
   `-`:减
##### 2.3.布尔数(bool)
1. 格式:`True`、`False`
___
1. `not`:非
   `or`:或,非布尔数运算真前假后
   `and`:且,非布尔数运算真后假前
___
1. 数据类型转化为布尔数函数:`bool()`
   可转化为False的其它值:`0`、`""`、`None`、`[]`、`()`、`{}`
   可转化为True的其它值:

___

+ 无序性
+ 不可变性

### 基本数据类型二

#### 1.集合(set)

+ 集合:元素只有值;有冻结集合(frozenset),不可变性
  格式:`{"a","b","c"}`

___

+ 运算
  `in`、`not in`
  `<集合>.add(<元素>)`:添加
  `<集合>.discard(<元素>)`、`<集合>.remove(<元素>)`:删减
  `frozenset()`:转化为冻结集合数据类型
  `<集合1>.union(<集合2>)`、`|`:并集
  `<集合1>.intersection(<集合2>)`、`&`:交集
  `<集合1>.difference(<集合2>)`、`-`:差集
  `>=`、`<=`:包含、属于
+ 集合解析式
  可以尝试for-in语句、if语句写在同一行

___

+ 无序性:不可迭代
+ 不可重复性:
+ 可变性:

#### 2.字典(dictionary)

+ 字典:元素=键(key)+值(value)
  格式:`{"a":1,"b":2,"c":3}`

___

+ 运算
  ```python
  # 索引
  info_of_mine={"name":"李润泽","age":18,"gender":"男"}
  info_of_mine["name"]
  info_of_mine.get("name",<若没有返回这个东西,可不写>)
  ```

  ```python
  # 增加、修改
  info_of_mine["gender"]="女"
  ```

+ 字典解析
  ```python
  {<键解析式:值解析式> for <(i,j)> in <列表,元素为键值对元组>}
  ```

+ 字典合并:`{**a,**b}`

___

+ 可迭代性:键是可迭代的
  ```python
  >>> info_of_mine.items()
  >>> [("name","李润泽"),("age",18),("gender","男")]
  >>> info_of_mine.keys()
  >>> ["name","age","gender"]
  >>> info_of_mine.values()
  >>> ["李润泽",18,"男"]
  ```

+ 可映射性:键(key)对应值(value),列表是索引(位置)(index)对应值(value)

+ 不可重复性:键是不可重复的,值是可重复的

+ 可变性

#### 3.列表(list)

+ 列表:实现链表数据结构,存放多个数据
           列表的变量名指向列表的变量值和所在内存地址,列表元素(位置+值)所在内存地址
+ 格式:`["Jack","Tom","Bob","Mary"]`

___

+ 运算
  `<列表>.append(<元素>)`:追加
  `<列表>.insert(<元素索引(index)>,<元素>)`:加
  `<列表>.pop(<元素索引(index)>)`:减
  `<列表>.remove(<元素值>)`:减
  `+`:拼接;`*`:重复
  
+ 拆包(unpack)和打包(pack)
  ```python
  # *<变量>=<有序性数据类型>,数据类型为列表
  nums=[0,1,2,3,4,5,6,7,8,9,10]
  num_0,num_1,num_2,num_3,*num_others,num_the_last_one=nums
  # *<有序性数据类型>是拆包
  # *(1,2,3)等价于1,2,3
  # **<可映射数据类型>是拆包
  # **{"x"=1,"y"=2,"z"=3}等价于x=1,y=2,z=3
  ```
  
+ 迭代
  1. 枚举
     ```python
     ages_1=[18,22,25,35]
     # enumerate函数,返回值的数据类型是枚举,类似于这样[(0,18),(1,22),(2,25),(3,35)]
     >>> ages_2=enumerate(ages_1)
     >>> type(ages_2)
     >>> <class 'enumerate'>
     ```
  
  2. 迭代器
     ```python
     ages_1=[18,22,25,35]
     # iter函数,返回值的数据类型是迭代器
     >>> ages_2=iter(ages)
     >>> type(ages_2)
     >>> <class 'list_iterator'>
     # next函数,迭代一次
     >>> next(ages_2)
     >>> 18
     >>> next(ages_2)
     >>> 22
     >>> next(ages_2)
     >>> 25
     >>> next(ages_2)
     >>> 35
     >>> next(ages_2)
     >>> StopIteration
     ```
  
  3. map函数
     遍历一个列表(组合数据)的元素,并且对每个元素执行一个操作;返回值是一个迭代器,类似于列表,包含所有结果
  
     ```python
     ages_1=[18,22,25,35]
     results_iterator_the_older_ages=map(lambda a:a+1,ages_1)
     ```
  
  4. filter函数
     对一个列表(组合数据),过滤掉不符合要求的元素,留下符合要求的元素;返回值是一个过滤器,类似于列表,包含所有结果
  
     ```python
     ages_1=[18,22,25,35]
     results_iterator_the_adult_ages=filter(lambda a:a>=18,ages_1)
     ```
  
  5. reduce函数
     对一个列表(组合数据),按要求计算,得到唯一结果
  
     ```python
     x=[1,2,3,4,5,6,7,8,9]
     sum_of_x=reduce(lambda a,b:a+b,x)
     ```
  
  6. 列表表达式
     对一个列表操作,生成新列表
  
     ```python
     [<列表表达式,可以看作函数解析式> for <元素变量> in <列表,可以看作函数定义域>]
     ```

___
+ 有序性
  ```python
  #使用sort方法,要求对象具有有序性、可变性
  <列表>.sort(reverse=False,key=None)#返回值位None,改原变量值,内存地址不变
  #使用reverse方法(逆序方法),要求对象具有有序性、可变性
  <列表>.reverse()#返回值位None,改变原变量值,内存地址不变
  #使用sorted函数
  sorted(<有序性的数据类型>)#返回值位新创建的变量
  ```
+ 可变性:元素值可以修改,内存地址不变
  ```python
  a=["a","b","c"]
  id(a)
  a[0]="1"
  id(a)
  ```
+ 可重复性:值可重复
___
#### 4.元组(tuple)

+ 元组:不可变性的列表
+ 格式:`(1,2,3)`、`1,2,3`、`(1,)`、`1,`

___

+ 运算
  `+`:拼接;`*`:重复

___

+ 有序性
+ 不可变性
+ 不唯一性

#### 5.其它数据类型
+ 范围(range):`range(<start>,<stop>,<step>)`
+ 不存在的数据类型:`None`

### 文件处理

#### 1.模块(module)和包(package)

+ 模块:.py文件
  包:包含\_\_init\_\_.py文件的文件夹
+ 导入模块
  ```python
  # 搜索方法1:按如下顺序搜索,内置模块→当前路径→环境变量→安装  python时配置的依赖路径
  # 搜索方法2:绝对路径
  # 搜索路径保存在sys.path变量中
  (from <包>) import <模块> (as <模块名>)
  <包>.<模块>.<调用变量、函数、类等>
  from <模块> import <变量、函数、类等> (as <变  量、函数、类等的名>)
  <调用变量、函数、类等>
  ```
+ 导出模块
+ 判断.py文件被导入
  ```python
  # 当执行一个.py文件时,变量__name__的值为"__main__"
  # 当一个.py文件被导入其它.py文件时,变量__name__的值为"模块名"
  ```

#### 2.文件处理

##### 2.1.编码、解码

##### 2.2.访问文件

```python
# 打开文件函数,返回值是什么未知
file_1=open(file=<文件名>,mode=<"r"(读模式)、"w"(写模式)、"a"(续写模式)、"+"、"t"、"b">,encoding=<编码解码模式,如"utf-8"、"gbk">)
# 读文件函数
file_1.read()
# 写文件函数
file_1.write()
# 关闭文件方法
file_1.close()
# 补充
import os
os.path.exists(<文件名>)
os.path.isfile(<文件或文件夹名>)
os.path.isdir(<文件或文件夹名>)
os.rename(<原文件或文件夹>,<新文件或文件夹>)
os.remove(<文件或文件夹>)
```

##### 2.3.访问文件夹

```python
import os
os.getcwd() #当前工作文件夹路径名
os.chdir(<文件夹>) #切换当前文件夹
os.mkdir(<文件夹>) #在当前文件夹创建文件夹
os.rmdir(<文件夹>) #删除文件夹
os.walk(<文件夹>) #遍历文件夹,返回值是一个迭代器.元素是dirpath、dirnames、filenames的元组
```

##### 2.4.pip、PyPI、虚拟环境

pip(package installer for python)和PyPI

```python
python -m pip install --upgrade pip #升级pip
pip --version
pip install <包> #安装包的最新版本
pip install <包>==<版本号>  #安装包的指定版本
pip install --upgrade <包> #升级包
pip uninstall <包> #卸载包
```

Python主程序安装:一台设备可以有多套Python程序,第一次用安装包安装的为主程序

Python虚拟环境安装

```python
pip install virtualenv #下载虚拟环境插件
python -m venv <虚拟环境名> #安装虚拟环境
<虚拟环境名>\Scripts\activate.bat #打开虚拟环境
<虚拟环境名>\Scripts\deactivate.bat #关闭虚拟环境
```

命令行操作
```python
ls #当前文件夹包含的文件和文件夹
cd <文件夹> #从当前文件夹到目标文件夹
```

### 函数(fnction)

#### 1.内置函数

+ 打印函数(print函数)

  1. 第一种格式化输出:`print("<①>" % <②>)`
     <①>`%d`:十进制整数
     		`%x`:十六进制数;`%o`:八进制数;`%b`:二进制数
     		`%f`:浮点数;`%e`:科学计数法的浮点数
     		`%s`:字符串

     ​		`%.99f`:保留99位小数

     ​		`%-100.10s`:左对齐,长度为100,保留10位字符
     <②>格式化输出的东西

  2. 第二种格式化输出:`print("{<①>}".format(<②>))`
     <①>`:d`:整数
             `:x`:十六进制数;`:o`:八进制数;`:b`:二进制数
             `:.3f`:浮点数,保留3位小数;`:e`:科学计数法的浮点数
             `:~^10s`:字符串,用"~"填充,居中对齐,长度为10

  3. 切割符和结束符:`print(...,...,sep="$",end="￥")`

+ 问答函数(input函数)

  1. `input("我是提示语")`
  2. 返回值的数据类型为字符串

+ 帮助函数(help函数)

#### 2.自定义函数

1. 函数,函数名指向内存地址
   ```python
   def <函数名>(<位置参数1(关键字参数1)的名>,<位置参数1(关键字参数1)的名>,...):
       <表达式>
   # 调用函数
   <函数名>(<位置参数1(关键字参数1)的值>,<位置参数1(关键字参数1)的值>,...)
   ```

2. 参数:参数的本质是变量
   1. 参数名
      1. 位置参数、关键字参数:
         ```python
         def <函数名>(<位置参数1(关键字参数1)>,<位置参数1(关键字参数1)>,...,<函数1>,<函数2>,...):
             <函数的主体,类似于数学函数解析式>
         ```
      
      2. 
         ```python
         # "\"之前的全是位置参数,"*"之后的全是关键字参数
         # *<参数>包含所有多余位置参数,是元组
         # **<参数>包含所有多余关键字参数,是字典
         def function(a,b,c,\,d,e,f,*,g,h,i,*j,**k)
         ```
      
      3. 
   2. 参数值
      1. 默认参数值
         ```python
         def print_my_age(my_age=18):
             print(f"我的年龄为{my_age}")
         ```
      2. 参数值的数据类型
         ```python
         def print_my_full_name(first_name:str,last_name:str)->str:
             full_name=first_name+" "+last_name
             print(f"我的姓名是{full_name}")
             return full_name
         ```
      
      3. 全局变量、局部变量
         ```python
         global <在函数内部自定义的变量名>
         ```

3. 返回值、返回值的数据类型
   ```python
   def print_my_full_name(first_name:str,last_name:str)->str:
       full_name=first_name+" "+last_name
       print(f"我的姓名是{full_name}")
       return full_name
   ```

4. 匿名函数
   ```python
   lambda <参数>:<返回值>
   ```

5. 递归

### 面向对象
#### 1.类(class)
+ 自定义类:
  ```python
  class Stuent(<>):
      ...
  print(Student);print(type(Student))
  <class '__main__.Student'>
  <class 'type'> #Student是type的对象
  ```

+ 枚举
  ```python
  from enum import Enum
  
  class Gender(Enum): #可遍历
      MALE=1
      FEMALE=2
  
  class Student:
      def __init__(self,gender:Gender):
          self.gender=gender
  
  me=Student(Gender.MALE)
  
  >>> print(Gender) #Gender的数据类型是
  >>> <class 'enum.EnumType'>
  >>> print(Gender.MALE) #Gender.MALE的数据类型
  >>> <enum 'Gender'>
  
  >>> print(Gender.MALE.name)
  >>> MALE
  >>> print(Gender.MALE.value)
  >>> 1
  
  >>> print(Gender["FEMALE"])
  >>> Gender.FEMALE
  >>> print(Gender(2))
  >>> Gender.FEMALE
  ```
  枚举的元素(主名、别名、值)
  ```python
  class Status(Enum):
      SUCCESS_1=1 #值为1,主名为SUCCESS_1
      SUCCESS_2=1 #别名为SUCCESS_2,主名是唯一的
      FAIL_1=1
      FAIL_2=2
  
  >>> print(Status.___members__)
  >>> {"SUCCESS_1":<Status.SUCCESS_1:1>,"SUCCESS_2":<Status.SUCCESS_2:1>,"FAIL_1":<Status.FAIL_1:1>,"FAIL_2":<Status.FAIL_2:1>}
  
  @enum.unique #此装饰器用于强制不重复
  class Status(Enum):
      SUCCESS_1=1
      SUCCESS_2=1
      FAIL_1=1
      FAIL_2=2
  ```

+ 描述符

  ```python
  #举个问题例子
  class Student:
      def __init__(self, first_name, last_name):
          self.first_name = first_name
          self.last_name = last_name
  
      @property
      def first_name(self):
          return self.__first_name
  
      @first_name.setter
      def first_name(self, first_name):
          if not isinstance(first_name, str):
              raise Exception
          if len(first_name) == 0:
              raise Exception
          self.__first_name = first_name
  
      @property
      def last_name(self):
          return self.__last_name
  
      @last_name.setter
      def last_name(self, last_name):
          if not isinstance(last_name, str):
              raise Exception
          if len(last_name) == 0:
              raise Exception
          self.__last_name = last_name
  ```

  ```python
  #运用描述符类解决上述问题
  class RequiredString:
      def __set_name__(self,owner,name):
          self.__property_name=name
      def __set__(self,instance,value):
          instance.__dict__[self.__property_name]=value
  	def __get__(self,instance,owner):
          return instance.__dict__[self.__property_name]
  
  class Student:
      first_name=RequiredString() #调用__set_name__方法,first_name传给参数name
  	last_name=RequiredString()
  
  student_1=Student()
  student_1.first_name="李"
  # 调用描述符对象的__set__方法,student_1传给参数instance,"李"传给参数value
  student_1.last_name="润泽"
  ```

+ 类的继承、重写

  ```python
  # 类的继承,如下,Student继承了Person所有的属性、方法
  class Person(object): #object是内置的类
      def __init__(self,name,age):
          self.name=name
          self.age=age
  class Student(Person):
      def __init__(self,university):
          self.university=university
  
  class Mom:
      def hello(self):
          print("Hello,Mommy!")
      def hi(self):
          print("Hi,Mommy!")
  class Dad:
      def hello(self):
          print("Hello,Daddy!")
      def hi(self):
          print("Hi,Mommy!")
  class Baby(Mom, Dad): #多继承
      def hello(self): #覆盖
          super().hello() #自动调用父类方法
      def hi(self):
          Dad.hi(self) #手动调用父类方法
  ```
#### 2.实例(instance)
+ 自定义对象:
  ```python
  student_1=Student()
  print(student_1);print(type(student_1))
  <__main__.Student object at <内存地址>>
  <class '__main__.Student'> #student_1是Student的实例
  ```
  ```python
  >>> isinstance(student_1,Student)
  >>> True
  ```

+ 抽象类:没有实例的类
  ```python
  from abc import ABC,abstractmethod
  
  class mn(ABC): #自定义抽象类
      @abstractmethod #自定义抽象方法
      def mn_1(self):
          print("我是抽象方法mn_1")
  ```

#### 3.属性(attribute)
+ 属性的本质是变量,包含类变量、实例变量

+ 类变量
  1.类变量:类属性
  2.内置类变量:如,`__name__`,存储类名
  3.自定义类变量:
  ```python
  class Student:
      student_count=8
  ```
  4.取得、修改类变量的值:
  ```python
  # 取得类变量的值
  Student.student_count
  getattr(Student,"student_count",(<若不存在此类变量,则赋此值>))
  # 修改类变量的值
  Student.student_count=11
  setattr(Student,"student_count",11)
  # 添加类变量
  Student.student_count=11
  ```
  5.删除类变量
  ```python
  # 删除类变量
  delattr(Student,"student_count")
  ```
  6.类变量的存储:全部存储在类变量`__dict__`中
  
+ 实例变量

+ 私有属性和私有方法:
  1.核心思想是封装
  2.用更高的抽象简化内部细节
  3.保护内部不被篡改和窥察
  
  ```python
  # 前边加"_",允许外部访问,但有提醒
  # 前边加"__",不允许外部访问;若非要使用,前边加"_<类名>"
  ```
  
  ```python
  # property类
  class Rectangle:
      def __init__(self,length,width):
          self.length=length
          self.width=width
          self.area=length*width
  rectangle=Rectangle(5,2)
  rectangle.area=20 #错误地修改变量
  
  class Rectangle:
      def __init__(self,length,width):
          self.length=length
          self.width=width
      @property
      def area(self):
          return self.length*self.width
  
  #———————————————分隔线———————————————#
  
  # property装饰器,看这个例子
  class Student:
      def __init__(self,name,age):
          self.name=name
          self.__age=age
  
      @property
      def age(self): #只读;套马甲
          return self.__age
      @age.setter #在读之上加了写
      def age(self,age):
          ...
          self.__age=age
  
  student_1=Student("Jack",18)
  student.age
  student.age=1
  ```
  
+ 动态和静态属性
  静态属性:仅仅是一个属性

#### 4.方法(method)

+ 方法的本质是函数,包含实例函数(在类中创建,调用需要有实例)、类函数(直接调用)

+ 实例函数
  1.自定义实例函数

  ```python
  class Student:
      def say_hello(self,msg): #self参数必须有,指实例本身,self这个名时习惯,不是规则
          print(f"Hello!{msg}")
  ```
  
  2.调用实例函数
  
  ```python
  student_1=Student()
  student_1.say_hello("我是李润泽") #调用实例方法时,self参数被自动调用
  ```
  
  3.\_\_new\_\_方法:用于返回实例对象,也可用于初始化实例对象
     \_\_init\_\_方法:用于初始化实例对象
  
  ```python
  class UppercaseTuple(tuple):
      def __new__(cls,iterable):
          upper_iterable=(i.upper() for i in iterable)
          return super().__new__(cls,upper_iterable) #返回两个实例对象,tuple的方法
  
  # 实例对象的创建过程
  student_1=Student("李润泽","18","浙江工商大学")
  student_1=Student.__new__(Student)
  if isinstance(student_1,Student):
      type(student_1).__init__(student_1,"李润泽"."18","浙江工商大学") #type函数的返回值是类
      
  #python设计的工作流程
  ```
  
+ 类函数
  ```python
  class Student:
      @classmethod
      def hello(self): #self参数必须有,指类本身
          print(f"hello,{cls.__name__}.")
  
  Student.hello() #调用类方法时,self参数被自动调用
  ```

+ 动态和静态方法
  静态方法:仅仅是一个方法

  ```python
  class Student:
      @starticmethod
      def hello():
          print("Hello,everyone.")
  
  Student.hello()
  ```

+ 一些特殊方法
  ```python
  #__str__方法,用于返回描述本身的字符串,面向用户
  class Data:
      def __init__(self,year,month,day):
          self.year=year
          self.month=month
          self.day=day
      def __str__(self):
          print("emmmmm")
          return f"{self.year}-{self.month}-{self.day}" #返回值必须为字符串
  
  today=Data(2023,1,25)
  
  >>> str(today)
  >>> "2023-1-25" #返回值为__str__方法的返回值
  
  >>> print(today)
  >>> 2023-1-25 #打印__str__方法或__repr__方法的返回值,打印__str__方法的优先
  
  
  #__repr__方法,用于返回描述本身的字符串,面向机器和开发者
  class Data:
      def __init__(self,year,month,day):
          self.year=year
          self.month=month
          self.day=day
      def __repr__(self):
          return f"{self.year}-{self.month}-{self.day}" #返回值必须为字符串
  
  today=Data(2023,1,25)
  
  >>> repr(today)
  >>> "2023-1-25" #返回值为__repr__方法的返回值
  ```

  ```python
  #__eq__方法
      def __eq__(self,other):
          ...
          return ... #返回值为布尔数
  
  today==tomorrow==yesterday
  ```
  
  ```python
  #__hash__方法,返回值为hash值
  #__bool__方法,返回值为布尔值
  ```
  
  ```python
  #__del__方法,在找不到名后,值会被垃圾回收
  ```