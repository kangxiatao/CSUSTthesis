# 长沙理工大学硕博学位论文 LaTeX 模板

```
@author: Kang Xiatao (kangxiatao@gmail.com)
```

本项目是长沙理工大学硕博学位论文 LaTeX 模板，按照《[附件6：长沙理工大学研究生学位论文撰写规范(2020年版).doc](https://www.csust.edu.cn/yjsy/info/1167/10313.htm)》的要求编写。由于个人水平有限，对tex用法并不熟练，虽然现在的这个版本基本上满足了学校的要求，但难免存在不足之处，希望有大佬能一同完善此模板，让更多同学受益。

本项目基于 [HNUthesis_master](https://github.com/ljmdzyx1985/HNUthesis_master)。感谢！！

- 本模板的缺陷较多，强烈建议用xelatex重新设计模板，可参考 [湖工商latex模板](https://github.com/ethan-phu/hutb_master_thesis_latex)。期待@[hahally](https://github.com/hahally)大佬提供xelatex的模板😀。

- 最后一次更新，以后也不会维护了。之后学院可能会出自己的模板，如果有同学还需要使用这个模板，遇到什么问题可以提在issues，我尽量答复。

## 说明

- 注意默认为专硕论文封面

  学硕和博士封面请对应修改```preface/cover.tex``` 和 ```setup/format.tex``` 中的变量

- 用pdflatex编译（如果可以读档，我一定会用xelatex）。推荐使用[VsCode配置LaTeX环境](https://kangxiatao.github.io/2021/06/30/23/clgj6ojjj000fssik11imeehb/)。不推荐使用[overleaf在线](https://cn.overleaf.com/)（pdflatex编译找不到字体，很麻烦。另外个人认为overleaf很难用）。

- 编写注意

  - 为了中英文更好的混排，请在中英文切换时添加```~```符号。请注意手动控制标点符号，不要出现在首行。
  - 图片和表格要注意格式。规范文档中未给出图表和文字的间距，可手动调节到合适的位置。表格上下两根线为 1.5 磅，中间线为 0.75 磅。
  - \ref 引用公式要添加()
  - \item 要加括号。模板没有写自己的list，所以特意说明一下。
  ```
	\begin{enumerate}[label={(\arabic*)}, itemindent=1.6cm]
	\item xxx
	\item xxx
  ```
  - 参考文献
	- 参考文献的标题统一为小写，大写缩写请用```{}```包起来，```e.g. {Lottery tickets in {RL} and {NLP}}```。
	- 文献信息尽量全，页面、doi等。谷歌学术上很多会议论文给的是arXiv，信息不全。
	- arXiv的文献最好在arXiv的页面```Export BibTeX Citation```。也可以用[arXiv引文格式在线](https://arxiv2bibtex.org/?q=2001.09678&format=bibtex)。
  - 图片标题上不要添加引用，图片也尽量用自己的图，哪怕对着画一个。存在争议，但是听老师的，老师说版权问题。
  - 关于空白页。图书馆是不能有空白页的，但是学院需要插空白页（保证章节在奇数页），有点折磨人，打印要注意。

- 目前存在的问题

  - 行间距问题

    latex中一倍行间距默认为1.2，而word中为1.3，行距倍数乘1.3即可，实际上有些许误差。

    目录行间距要求固定为20pt，受全文影响不好设置，暂时通过调节行距倍数至20pt左右。

  - 页眉问题

    \leftmark莫名有编号，只能在对应章节里手动修改页眉，具体请看注释和第一章的写法

    论文撰写规范中页眉位置不明确，我从文字到顶部的距离算15mm。[latex geometry 页面设置](https://www.jianshu.com/p/0719795278eb/)

  - 外文黑体问题

    \textsf{}转换为英文无衬线体替代黑体。
	```
	关于\text**：
	\textrm{} 相当于默认字体，即中文宋体，英文罗马
	\textit{} 默认中文楷书，若前面定义过下文中文字体，则为定义字体，英文斜体
	\textsf{} 中文微软雅黑，英文无衬线体
	\texttt{} 中文仿宋，英文等宽字体
	\textbf{} 字体加粗通用
	```

  - 参考文献问题

    直接用```gbt7714-numerical.bst```（cite和natbib宏包冲突问题），暂时没发现其他格式问题。 非常感谢：[GB/T 7714—2015 BibTeX Style](https://github.com/zepinglee/gbt7714-bibtex-style)
	
	规范文档里会议论文示例为```.```，之前已把```\\```改为```.```（[修改方法](https://github.com/zepinglee/gbt7714-bibtex-style/issues/119)）。但考虑到以国标为准，析出文献应该用```\\```，已改回。
	
	计算机学科确实很多文章是上传到arXiv在线发表，关于arXiv上的文献国标没有特殊规定，很多人都认为可以分到```[A]```，arXiv的预印本属于科技档案，我也比较认同，所以arXiv的文献格式为```xxx[A]. 2023. arXiv: 2000.66888```。
	
  - 代码规范问题
	
	最开始的框架就很乱，后面又调整了很多东西，现在代码基本上成屎山了，个人没精力去整理，先这样吧。

## 文件

- 在模板```main.pdf```中做了具体说明（latex的一些用法、注意事项、文件结构等）
- ```main.tex``` 为主文件
- ```setup``` 和根目录下的部分文件为格式文件
- ```body``` 中放主要章节
- ```figures``` 放图片
- ```preface``` 为封面内容和摘要
- ```reference``` 放参考文献
- ```appendix``` 包含附录部分

## 祝大家顺利毕业！

![](https://s3.bmp.ovh/imgs/2023/06/01/8d3835c51e6bb816.png)
