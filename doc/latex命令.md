# Latex 命令

[toc]

## [自定义命令](./自定义命令.md)

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
\hspace{2em} 空两个中文字符
```

## 段落

```latex
\setlength{\parskip}{1ex} % 段间距
```

## 无序列表行间距过大

```latex
\begin{itemize}
    \setlength{\itemsep}{0pt}
    \setlength{\parsep}{0pt}
    \item 233
    \item 666
\end{itemize}
或者
\begin{itemize}[parsep=0pt, itemsep=0pt]
    \item 233
    \item 666
\end{itemize}
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
