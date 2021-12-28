LaTeX

TeX

高德纳教授

## 1.1 让LaTeX跑起来

### 1.1.1 LaTeX的发行版及其安装
CTeX

TeX Live

#### 1.1.1.1 CTeX套装
[CTeX](http://www.ctex.org/HomePage)

#### 1.1.1.2 TeX Live
[TeX Live](https://tug.org/texlive/)

### 1.1.2 编辑器与周边工具
#### 1.1.2.1 编辑器举例-TeXworks 
我用VSCode，利用LaTeXWorkShop

#### 1.1.2.2 PDF阅读器

PS格式和PDF格式

#### 1.1.2.3 命令行工具
一、 命令行

二、GhostScript

GhostScript是PostScript的一个解释器

ps2pdf、pdf2ps等

三、ImageMagick

### 1.1.3 “Happy TeXing”与“特可爱排版”

编译程序

DVI文件格式

pdfTeX、LuaTeX、XeTeX

## 从一个例子说起
### 1.2.1 确定目标
### 1.2.2 从提纲开始
注释 %

文档类 编码方式

导言区

环境

根据内容所用命令会有不同编译次数

### 1.2.3 填写正文
空行分段

LaTeX自动控制缩进

通常汉字后面空格会被忽略，其他不会

### 1.2.4 命令与环境
命令都以\开始，后接参数

声明

en dash

### 1.2.5 遭遇数学公式

正文公式或行内公式 \$公式内容\$

显示公式或列表公式 equation环境

键盘上没有的，可以用命令

数学结构：上下标、分式、根式等

### 1.2.6 使用图表
1. 插入事先准备好的图像
2. 使用LaTeX代码画图

插图使用graphicx宏包

宏包在导言区使用\usepackage命令导入

单独环境插图

浮动体

标签 \label

表格 tabular环境

\qquad 产生空格

### 1.2.7 自动化工具
BibTex  参考文献数据库 文件后缀：.bib

引用

目录 页码

交叉引用

### 1.2.8 设计文章格式

设计页面尺寸 geometry宏包

图表标题格式 caption宏包

目录 tocbibind宏包

定义新环境 \newenviroment

定义新命令 \newcommand




