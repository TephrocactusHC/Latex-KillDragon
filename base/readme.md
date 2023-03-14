# Latex Learning

来源，简单粗暴LATEX

主要记录每个功能该去找什么包

# 命令与环境

LATEX 中的命令通常是由一个反斜杠加上命令名称，再加上花括号内的参数 构成的（有的命令不带参数，例如：\TeX）．

```latex
\documentclass[a4paper]{ctexart}
```

备选项为 `方括号`

还有一种重要指令叫做环境．它被定义于控制命令`\begin{environment} `和`\end{environment}`间的内容．比如：
```latex
\begin{document} 
...内容... 
\end{document}
```

## 保留字符
它们的作用分别是： 
- #: 自定义命令时，用于标明参数序号． 
- $: 数学环境命令符． 
- %: 注释符．在其后的该行命令都会视为注释．如果在回车前输入这个命令， 可以防止行末 LATEX 插入一些奇怪的空白符． 
- ^: 数学环境中的上标命令符． 
- &: 表格环境中的跳列符． 
- \_: 数学环境中的下标命令符． 
- {与}: 花括号用于标记命令的必选参数，或者标记某一部分命令成为一个 整体．
- \\: 反斜杠用于开始各种 LATEX 命令． 以上除了反斜杠外，均能用前加反斜杠的形式输出．
## 导言区
```latex
\documentclass[options]{doc-class} 
\begin{document} 
... 
\end{document}
```
其中，在语句`\begin{document}`之前的内容称为导言区．导言区可以留空， 以可以进行一些文档的准备操作．你可以粗浅地理解为：导言区即模板定义．

`宏包`的加载工作
```latex
\usepackage{package}
```
# 分页
用`\newpage`命令开始新的一页．
用`\clearpage`命令清空浮动体队列5，并开始新的一页． 
用`\cleardoublepage`命令清空浮动体队列，并在偶数页上开始新的一页．
# 字族、字系与字形
这个挺有意思的。
# 颜色
`xcolor`宏包
# 引用与注释
## 标签和引用
使用`\label`命令插入标签（在 MS Word 中称为“题注”），然后在其他地方 用`\ref`或者`\pageref`命令进行引用，分别引用标签的序号、标签所在页的页码．

更常用的是 `hyperref `宏包
## 脚注、边注与尾注
```latex
\footnote{This is a footnote.}
```
# 正式排版：封面、大纲与目录
```latex
\title{Learning LaTeX}
\author{wklchris} 
\date{text}
```

**带星号的大纲插入目录**

## 目录
使用命令`\tableofcontents`即可插入目录．目 录在加载了 `hyperref` 宏包后，可以实现点击跳转的功能．你可以通过重定义命 令更改`\contentsname`，即“目录”的标题名

# 计数器与列表
用`\the` 接上计数器名称的方式来调用计数器
# 图文混排
可参考 `wrapfig` 宏包
# 表格
`longtable` ,` supertabular `,`tabu `等宏包．跨行的问题 只需要 `multirow` 宏包．

`array`,`makecell`,分割表头：`diagbox`
# 数学
一块特别巨大的内容，用时再查吧。。。
# 进阶
## 箱子
很有用
## tcolorbox 宏包
左边源码，右边效果
## GIF
`animate` 宏包（当然，`graphicx` 宏包也是需要的），可以将多张图片 以动态图的形式插入 PDF
