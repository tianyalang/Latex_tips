# Latex 命令

[toc]

## 自定义命令

### 语法

```latex
\newcommand{新命令}[参数数量][首参数默认值]{命令内容}
```

+ 新命令：**必选**
  - 符合命令构成规则，`\`开头，只能由字母组成，不能有数字和特殊字符
  - 不能与系统和已调用宏包命令重名
  - 对已有命令重定义，用`\renewcommand`, 用法类似
+ 参数数量：**可选**
  - 用于指定该命令具有的参数个数
  - 默认为0，最多9个
+ 首参数默认值：**可选**
  - 用于设定第一个参数的默认值，即`命令内容`中的`#1`参数
  - 如果定义时给出默认值，表明命令第一个参数为可选
  - 只能有一个可选参数，且必须是第一个参数
+ 命令内容：**必选**
  - 涉及某个参数时用符号`#N`表示，如#1 #2

### 举例

#### 不带参数

```latex
\newcommand{\diff}{\mathrm d} 

$\diff x$      % \diff = \mathrm d
```

编译后显示：$\mathrm d x$

#### 带一个参数

```latex
\newcommand{\mytextcolor}[1]{\textcolor{red}{#1}}

\mytextcolor{It is red}  % 'It is red'放入 #1 的位置
% 该命令依赖 'color' 宏包
```

编译后显示：<font face='Times New Roman' color=red>It is red</font>

#### 带多个参数

```latex
\newcommand{\cubic}[3]{#1^3 + #2^3 + #3^3}

$\cubic{x}{y}{z}$  % x,y,z 依次放入 #1 #2 #3 位置
```

编译后显示：$x^3+y^3+z^3$

#### 带默认参数

```latex
\newcommand{\judge}[3][10]{\sqrt{#1^2 - 4#2#3}}

$\judge{a}{c}$    % 命令包含3个参数，但只输入了2个。把这2个放入#2 #3位，默认参数放#1位
$\judge[b]{a}{c}$ % 命令包含3个参数，输入3个，依次放入#1#2#3位置
$\judge[5]{a}{c}$ % 注意：[]中内容替换默认参数
```

编译后显示：
&emsp;$\sqrt{10^2-4ac}$
&emsp;$\sqrt{b^2-4ac}$
&emsp;$\sqrt{5^2-4ac}$

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
