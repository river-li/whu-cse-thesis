# 武汉大学毕业论文 LaTeX 模板

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Last Commit](https://img.shields.io/github/last-commit/river-li/whu-thesis.svg)](https://github.com/river-li/whu-thesis/commits/)

本项目为针对国家网络安全学院硕士要求修改后的硕士毕业模板，fork自[whu-thesis](https://github.com/whutug/whu-thesis)

原本的模板虽然大部分地方也是符合学校论文印制规定的，但是实际过程中有一些不成文的规矩之类的...

仅针对硕士模板进行了修改

有问题可见原始上游项目[README](https://github.com/whutug/whu-thesis)，本项目不做后续支持!

本项目主要修改内容包括以下几点

1. 增加了英文封面信息；
2. 调整了引用网络文献时的条目顺序；
3. 增加了硕士的成果简介页；


## 如何使用

可参考[上游项目](https://github.com/whutug/whu-thesis)

针对计算机相关专业常见的需求————在论文中写算法/代码，可以使用以下两类方法

修改的模板增加了脚本的编号，不过是放在代码上面的（和表格类似）

### 脚本代码

```latex
\lstset{
  backgroundcolor = \color{yellow!10},% 背景色：淡黄
  basicstyle = \small\cour,           % 基本样式 + 小号字体
  rulesepcolor= \color{gray},         % 代码块边框颜色
  numberstyle = \small,               % 行号字体
  numbers=none,
  keywordstyle = \color{blue},        % 关键字颜色
  commentstyle =\color{green!100},    % 注释颜色
  stringstyle = \color{red!100},      % 字符串颜色
  frame = shadowbox,                  % 用（带影子效果）方框框住代码块
  showspaces = false,                 % 不显示空格
  columns = fixed,                    % 字间距固定
  %escapeinside={<@}{@>}              % 特殊自定分隔符：<@可以自己加颜色@>
  morekeywords = {as},                % 自加新的关键字（必须前后都是空格）
  deletendkeywords = {compile}        % 删除内定关键字；删除错误标记的关键字用deletekeywords删！
}

\begin{lstlisting}[float,caption={Caption of your Script},breaklines=false]
 int main(){
     printf("Hello World\n");
     return 0;
 }
\end{lstlisting}
```

### 算法

可以用`algorithmic`包 （当然也有很多其他的可以参考[Overleaf上的一个说明](https://www.overleaf.com/learn/latex/Algorithms#The_algpseudocode_and_algorithm_packages)）


```latex
\begin{algorithmic}
\STATE $i\gets 10$
\IF {$i\geq 5$} 
  \STATE $i\gets i-1$
\ELSE
  \IF {$i\leq 3$}
    \STATE $i\gets i+2$
  \ENDIF
\ENDIF 
\end{algorithmic}
```
