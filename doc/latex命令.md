# Latex 命令

[toc]

## 自定义命令

新命令符合命令构成规则，不能与系统和已调用宏包命令重名。

```latex
\newcommand{新命令}[参数数量][默认值]{定义内容}
```

+ 参数数量：可选，用于指定该命令具有参数个数，默认为0，即无参数。新定义命令参数不得含有抄录命令\verb 和抄录环境verbatim以及相关命令和环境。
+ 默认值：可选，用于设定第一个参数的默认值，如果定义时给出默认值，表面命令第一个参数可选，新命令最多只能有一个可选参数，而且必须是第一个参数。
+ 命令内容：涉及某个参数时用符号#n表示，如#1  #2

:chestnut:&nbsp;&nbsp;**E.g.**

```latex
\newcommand{\mytextcolor}[1]{\textcolor{black}{{}#1}}
```

+ 第一个花括号：新命令的名字
+ \[1]:表示有一个参数
+ 后面的大花括号表示新命令的内容。\textcolor{black}{{}#1}:#1指出参数的位置

使用：`\mytextcolor{text}` 的效果和`\textcolor{black}{text}`相同。这个命令就可以用于快捷地定义颜色的种类。在修改论文时十分有用。

## input / include

+ 换页方式
  * `\input` 内容会嵌入在调用的位置，与原内容是在同页连续的。
  * `\include` 的内容在嵌入会在后面加上一个换页，使其后面的内容重新一页开始。
+ 编码原理
  * `\input` 编译前就插入原文件，形成一个文件再编译。
  * `\include` 先单独编译，然后将生成的各自的PDF再进行合并，这也是换页产生的原因。
+ `\input` 可以写进导言区，`\include`不可以。
+ `\input` 可以递归使用，`\include` 不可以。

`\includeonly` 放在导言区，用来指定正文区中include的那一部分（或者全部）参与当前编译，对于大型文档的中间调试非常有用，不用修改正文区，只改includeonly的列表就可以实现分步调试了。

include 每次可以把该部分文件编译后的辅助文件保留，从而includeonly里的内容变化时，可以加快整个文件的编译速度

## 换行，空格

```latex
\par   换行
\quad  空格
\qquad 两个空格
```

## 有用的宏包

```latex
\usepackage{ulem}

\uline{下划线}
\uuline{双下划线}
\uwave{波浪线}
\sout{中间删除线}
\xout{斜删除线}
\dashuline{虚线}
\dotuline{加点}
```
