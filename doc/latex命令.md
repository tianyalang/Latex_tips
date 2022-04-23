# Latex 命令

[toc]

## 命令作用范围

一个分组。

- 一个环境是一个分组。最大的分组就是正文 `document` 环境
- 成对括号 `{}` 可产生一个分组


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
