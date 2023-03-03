# Markdown语法

## 1.文本
### 1.1.标题
源代码:
```markdown
<H1>
====
<H2>
----
```
效果:
![标题效果图1](C:\Users\李润泽\Documents\笔记和帮助文档\计算机笔记和帮助文档\Markdown笔记\Markdown笔记插图1.png)
- - -
源代码:
```markdown
# <H1>
## <H2>
### <H3>
···
###### <H6>
```
效果:
![标题效果图2](C:\Users\李润泽\Documents\笔记和帮助文档\计算机笔记和帮助文档\Markdown笔记\Markdown笔记插图2.png)
### 1.2.正文
源代码:
```markdown
我
是
换行
```
效果:
我
是
换行
- - -
源代码:
```markdown
看这里

这是一个空行
```
效果:
看这里

这是一个空行
- - -
源代码:
```markdown
看这里 这是一个空格
```
效果:
看这里 这是一个空格
### 1.3.字体字号颜色
源代码:
```markdown
**<加粗的字体>**
__<加粗的字体>__
*<加斜的字体>*
_<加斜的字体>_
***<加粗加斜的字体>***
___<加粗加斜的字体>___
~~加删除线的字体~~
```
效果:
**这个字体加粗了**
__这个字体加粗了__
*这个字体加斜了*
_这个字体加斜了_
***这个字体加粗加斜了***
___这个字体加粗加斜了___
~~这个字体加删除线了~~
- - -
源代码:
```markdown
<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑体字</font>
···
<font color=red>我是红色</font>
<font color=yellow>我是黄色</font>
<font color=blue>我是蓝色</font>
···
<font size=10>我是10号字</font>
···
```
效果:
<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑体字</font>
$\cdots$
<font color=red>我是红色</font>
<font color=yellow>我是黄色</font>
<font color=blue>我是蓝色</font>
$\cdots$
<font size=10>我是10号字</font>
$\cdots$
### 1.4.对齐
源代码:
```markdown
<center>我是居中对齐</center>
<p align="left">我是左对齐</p>
<p align="right">我是右对齐</p>
```
效果:
<center>我是居中对齐</center>
<p align="left">我是左对齐</p>
<p align="right">我是右对齐</p>
## 2.文档元素
### 2.1.分界线
源代码:
```markdown
***
- - -
___
```
效果:
***
- - -
___
___
### 2.2.引用
源代码:
```markdown
>这是引用
我不知道应该引用一些什么
```
效果:
> 这是引用
> 我不知道应该引用一些什么
___
### 2.3.无序列表
源代码:
```markdown
- 我是一个无序列表
  - 我也是一个无序列表
    - 我还是一个无序列表
+ 我是一个无序列表
```
效果:
- 我是一个无序列表
  - 我也是一个无序列表
    - 我还是一个无序列表
+ 我是一个无序列表
___
### 2.4.有序列表
源代码:
```markdown
1. 我是一个有序列表
8316917364. 我也是一个有序列表
```
效果:
1. 我是一个有序列表
8316917364. 我也是一个有序列表
___
### 2.5.表格
源代码:
```markdown
|我是一个表头|我也是一个表头|我还是一个表头|
|---:|:---:|:---|
|随便写点儿什么|不知道应该写什么|算了，不写了|
|||
```
效果:
|   我是一个表头 |  我也是一个表头  | 我还是一个表头 |
| -------------: | :--------------: | :------------- |
| 随便写点儿什么 | 不知道应该写什么 | 算了，不写了   |
||||
### 2.6.图片
源代码:
```markdown
![这是图片的替代文字](这是图片的链接或路径 "我是图片的标题,我可有可无")
```
效果:
![这是Markdown的标志](C:\Users\李润泽\Documents\笔记和帮助文档\计算机笔记和帮助文档\Markdown笔记\Markdown笔记插图3.png "Markdown")
___
源代码:
```markdown
![这是图片的替代文字][我是图片的参考]
[我是图片的参考]:这是图片的链接或路径 "我是图片的标题,我可有可无"
```
效果:
![这是Markdown的标志][图片文件来自于这里]
[图片文件来自于这里]:C:\Users\李润泽\Documents\笔记和帮助文档\计算机笔记和帮助文档\Markdown笔记\Markdown笔记插图3.png "Markdown"
___
源代码:
```markdown
<img src="C:\Users\李润泽\Documents\笔记和帮助文档\计算机笔记和帮助文档\Markdown笔记\Markdown笔记插图3.png" width="100" height="50" align="right" title="我是图片的标题,我可有可无">
```
效果:
<img src="C:\Users\李润泽\Documents\笔记和帮助文档\计算机笔记和帮助文档\Markdown笔记\Markdown笔记插图3.png" width="100" height="50" align="right"  title="Markdown">
### 2.7.链接
源代码:
```markdown
[我是超链接的名称](我是链接 "我是小标题")
```
效果:
[Markdown中文教程](https://markdown.com.cn/ "Markdown中文教程")
[Markdown Guide](https://www.markdownguide.org/ "Markdown Guide")
### 2.8.上下标
源代码:
```markdown
随便写几个字^这是上标^
随便写几个字~这是下标~
```
效果:
随便写几个字^这是上标^
随便写几个字~这是下标~
## 3.数学公式
Markdown和LaTeX有关数学公式的语法基本相同
## 4.代码块
源代码:
```markdown
`这是小代码块`
```
效果:
`这是小代码块`
___
源代码:
````markdown
```语言
这是独立代码块
```
````
效果:
```python
print("Hello,World!")
```