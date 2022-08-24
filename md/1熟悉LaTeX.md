TeX  面向作者

LaTeX

高德纳教授 Donald Ervin Knuth

## 1.1 让LaTeX跑起来
### 1.1.1 LaTeX的发行版及其安装
#### 1.1.1.1 CTeX套装
[CTeX](http://www.ctex.org/HomePage)

#### 1.1.1.2 TeX Live
[TeX Live](https://tug.org/texlive/)
可以通过[清华源](https://mirrors.tuna.tsinghua.edu.cn/CTAN/)下载安装

### 1.1.2 编辑器与周边工具
#### 1.1.2.1 编辑器举例-TeXworks 
我用VSCode，利用LaTeXWorkShop

- 正反向查找
- 代码补全

文字编码
- ASCII
- ISO
- GB
- GBK
- Unicode

#### 1.1.2.2 PDF阅读器
PS格式和PDF格式

- Adobe Reader

#### 1.1.2.3 命令行工具
一、 命令行
了解简单的目录切换、文件管理等命令

二、GhostScript

GhostScript是PostScript的一个解释器

ps2pdf、pdf2ps等

三、ImageMagick
图像格式转换工具

> 通过命令行获取帮助文档

### 1.1.3 “Happy TeXing”与“特可爱排版”
英文
```latex
\documentclass{article}

\begin{document}
This is my first document.

Happy \TeX ing!
\end{document}
```

中文
```latex
\documentclass[UTF8]{ctex}

\begin{document}
\section{文字}
特可爱排版。
\section{数学}
\[
	a ^ 2 + b ^ 2 = c ^ 2
\]

\end{document}
```

DVI 文件格式

编译程序  
pdfTeX、LuaTeX、XeTeX

## 从一个例子说起
### 1.2.1 确定目标
> 万事开头难？

### 1.2.2 从提纲开始
- 文档的结构
- 基本的设置
- 填写内容

注释  `%`

> 注释的艺术？

文档类 编码方式

参考文献格式

导言区

环境

根据内容所用的命令会有不同编译次数

### 1.2.3 填写正文
空行分段

LaTeX 自动控制缩进

空格的使用
通常汉字后面空格会被忽略，其他不会

### 1.2.4 命令与环境
脚注 `\footnote`

表示强调 `\emph`

命令都以 `\` 开始，后接参数，部分包括可选参数

引用  `quote` 环境

环境使用 `\begin` 和 `\end` 命令来标识起止

分组
声明

摘要 `abstract` 环境

定理环境的定义
```latex
\newtheorem{thm}{定理}

\begin{thm}[some text]
some text
\end{thm}
```

en dash `--`

### 1.2.5 遭遇数学公式

正文公式或行内公式 `$公式内容$`

显示公式或列表公式 `equation` 环境

键盘上没有的，可以用命令
`\angle`  `\pi`  `\circ`

数学结构：上下标、分式、根式等

### 1.2.6 使用图表
1. 插入事先准备好的图像
2. 使用LaTeX代码画图

插图使用 `graphicx` 宏包

宏包在导言区使用 `\usepackage` 命令导入

`\includegraphics`

单独环境插图

```latex
\begin{figure}[ht]
	\centering
	\includegraphics[scale=0.6]{picture.pdf}
	\caption{some text}
	\label{fig:picture}
\end{figure}
```

浮动体
`float` 宏包

标签 `\label`

表格 `tabular` 环境
```latex
\begin{tabular}{|rrr|}
\hline
$a$ & $b$ & $c$ \\
\hline
3 & 4 & 5 \\
5 & 12 & 13 \\
\hline
\end{tabular}
```

```latex
\begin{table}[H]

\begin{tabular}{|rrr|}
\hline
$a$ & $b$ & $c$ \\
\hline
3 & 4 & 5 \\
5 & 12 & 13 \\
\hline
\end{tabular}%

\qquad
($a ^ 2 + b ^ 2 = c ^ 2$)

\end{table}
```

`\qquad` 产生空格

利用注释取消行尾换行产生的空格

### 1.2.7 自动化工具
BibTex  参考文献数据库 文件后缀：`.bib`

引用

`\cite`
`\nocite` 不直接引用

目录 页码
`\tableofcontents`

交叉引用
`\ref`

`amsmath`
`\eqref`

### 1.2.8 设计文章格式
设计页面尺寸 `geometry` 宏包
```latex
\usepackage{geometry}
\geometry{a6paper,centering,scale=0.8}
```

图表标题格式 `caption` 宏包
```latex
\usepackage[format=hang,font=small,textfont=it]{caption}
```

目录 `tocbibind` 宏包
```latex
\usepackage[nottoc]{tocbibind}
```

定义新环境 `\newenviroment`
```latex
\newenvironment{myquote}
	{\begin{quote}\kaishu\zhihao{-5}}
	{\end{quote}}
```

定义新命令 `\newcommand`
```latex
\newcommand\degree{^\circ}
```

> 格式与内容分离  
> 模块化