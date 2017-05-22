title: Mac上使用latex浙大论文模版

date: 2016-03-14 21:22:40
dfsdf
tags:
---

###1.编译选项 
首先是简单问题，就是指定下用xelatex编译，不然会用pdflatex

在main.tex第一行添加

```latex
%!TEX program = xelatex
```

###2.字体问题
接下来主要问题还是字体问题，在csbachelor.cls中修改。
首先在58行左右设置全局字体的地方，将这一段改为

```latex
\RequirePackage[slantfont,boldfont]{xeCJK}
\setCJKmainfont[BoldFont=STHeiti,ItalicFont=STKaiti]{STSong}
\setCJKsansfont[BoldFont=STHeiti]{STXihei}
\setCJKmonofont{STFangsong}
\punctstyle{kaiming}
```

在114行左右设置一些family的地方，改为

```latex
\setCJKfamilyfont{FangSong}{STFangSong}
\setCJKfamilyfont{HeiTi}{STXihei}
\setCJKfamilyfont{KaiShu}{AR PL KaitiM GB}
\setCJKfamilyfont{LiShu}{LiSu}
\setCJKfamilyfont{SongTi}{STSong}
\setCJKfamilyfont{YouYuan}{YouYuan}
\setCJKfamilyfont{STFangsong}{STFangsong}
\setCJKfamilyfont{STXingkai}{STKaiti}
```
mac下好像没有xingkai的字体，也用楷体代替了，有的话可以补充告诉我。

 
