# 长沙理工大学硕博学位论文 LaTeX 模板

```
@author: Kang Xiatao (kangxiatao@gmail.com)
```

本项目是长沙理工大学硕博学位论文 LaTeX 模板，按照《[附件6：长沙理工大学研究生学位论文撰写规范(2020年版).doc](https://www.csust.edu.cn/yjsy/info/1167/10313.htm)》的要求编写。由于个人水平有限，对tex用法并不熟练，虽然现在的这个版本基本上满足了学校的要求，但难免存在不足之处，希望有大佬能一同完善此模板，让更多同学受益。

本项目基于 [HNUthesis_master](https://github.com/ljmdzyx1985/HNUthesis_master)。感谢！！

## 说明

- 注意默认为专硕论文封面

  学硕和博士封面请对应修改```preface/cover.tex``` 和 ```setup/format.tex``` 中的变量

- 用pdflatex编译。推荐使用[VsCode配置LaTeX环境](https://kangxiatao.github.io/2021/06/30/23/clgj6ojjj000fssik11imeehb/)。或者[overleaf在线](https://cn.overleaf.com/)。

- 编写注意

  - 为了中英文更好的混排，请在中英文切换时添加```~```符号（好想改成xelatex啊）
  - 图片和表格要注意格式。规范文档中未给出图表和文字的间距，可手动调节到合适的位置。表格上下两根线为 1.5 磅，中间线为 0.75 磅。
  - \ref 引用公式要添加()
  - \item 要加括号。模板没有写自己的的list，所以特意说明一下。
  ```
	\begin{enumerate}[label={(\arabic*)}, itemindent=1.6cm]  % 24pt
	\item xxx
	\item xxx
  ```
  - 参考文献的标题要统一，大小写不能乱来。文献信息尽量全，页面、doi等。
  - 图片标题上不要添加引用，图片也尽量用自己的图，哪怕对着画一个。存在争议，但是听老师的，老师说版权问题。

- 目前存在的问题

  - 行间距问题

    latex中一倍行间距默认为1.2，而word中为1.3，行距倍数乘1.3即可，实际上有些许误差。

    目录行间距要求固定为20pt，受全文影响不好设置，暂时通过调节行距倍数至20pt左右。

  - 页眉问题

    \leftmark莫名有编号，只能在对应章节里手动修改页眉，具体请看注释和第一章的写法

    论文撰写规范中页眉位置不明确，我从文字到顶部的距离算15mm。[latex geometry 页面设置](https://www.jianshu.com/p/0719795278eb/)

  - 黑体再加粗问题

    \bf 只能加粗到黑体系列字体属性，如果\bf再加黑体就没有加粗效果，可能要从字体下手，暂时没找到解决方案。在附录7中“学位论文原创性声明与版权使用授权书”的标题是黑体加粗，不过影响不大。

  - 参考文献问题

    直接用```gbt7714-numerical.bst```（cite和natbib宏包冲突问题），会议论文已把```\\```改为```.```（规范文档里示例为```.```），暂时没发现其他格式问题。 非常感谢：[GB/T 7714—2015 BibTeX Style](https://github.com/zepinglee/gbt7714-bibtex-style)
	
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

## 其他暂时懒得写了
