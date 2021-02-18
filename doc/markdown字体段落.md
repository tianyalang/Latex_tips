# Markdown 字体、段落设置

[toc]

## 文字

### 高亮、加粗、斜体

`文本高亮`
**加粗**
*倾斜*
***倾斜加粗***
~~删除线~~

### 字号、字体、颜色

+ 借助 `html` 语言进行设置

<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=red>我是红色</font>
<font color=#008000>我是绿色</font>
<font color=Blue>我是蓝色</font>
<font size=5>我是尺寸</font>
<font face="黑体" color=green size=5>我是黑体，绿色，尺寸为5</font>

### emoji 表情

:tea: :cry: :sheep: :horse: :rocket:
:chestnut: :bug: :scissors: :memo: :recycle:
[一份完整表情列表的链接](https://gist.github.com/rxaviers/7360908)

### svg代码

<svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink">
   <defs>
    <path id="path1" d="M75,20 a1,1 0 0,0 100,0" /path>
  </defs>
  <text x="10" y="100" style="fill:red;">
    <textPath xlink:href="#path1">I love SVG I love SVG</textPath>
  </text>
</svg>

## 列表

### 无序列表

+ 一级条目1
+ 一级条目2
  + 二级条目1
  + 二级条目2
    + 三级条目1
    + 三级条目2
    * 三级条目3
  * 二级条目3
- 一级条目3

### 有序列表

1. 观点一
1. 观点二
1. 观点三

## 待办

+ [ ] 哈哈
+ [x] did

## 表格

内部对齐方式

| cccccccc | xxxxxxxxxx | kkkkkkkkk |
| :------- | :--------: | --------: |
| f        |     l      |         d |
| f        |     l      |         t |

## 段落

### 对齐方式

<center>居中</center>
<p align="left">左对齐</p>
<p align="right">右对齐</p>
<p align="justify">两端对齐</p>

### 换行

换行</br>标记

### 空格

只能识别**一个**空格。

+ dd ddd   ddd
+ 我是 中国  人民的   儿子。

用命令插入空格

+ 一个&nbsp;半角空格
+ 两个&ensp;半角空格
+ 四个&emsp;半角空格
+ 细&thinsp;空格

### 多行注释

<!--
哈哈我是多段
注释，
不会在浏览器中显示。
-->

[//]: # ( 哈哈我是注释，不会在浏览器中显示。)

### 分割线

***

### 文本链接

参见[同级文件](数学符号公式.md)
参见[上级文件](../README.md)

### 引用

这里[^id]引用

[^id]:  "Optional Title Here"
