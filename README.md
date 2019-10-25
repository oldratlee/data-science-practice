# 数据科学实践

**数据科学** 是指

1. **数学/统计学**
1. **计算机技术（编程）**
1. **业务领域**

三者的交叉应用学科。数据科学这个词近些年火起来，典型事件是2015年2月美国白宫宣布任命曾在多家硅谷科技公司任职的帕蒂尔（_DJ Patil_）为白宫首位首席数据科学家。

数据科学3者下的两两交叉应用，其实已经广为大家所知：

1. 数学/统计学 **`+`** 计算机技术（编程）   
    **`=>`** **机器学习**（Bang!）
1. 计算机技术（编程） **`+`** 业务领域  
    **`=>`** **业务软件开发**（平时说的软件工程师）  
1. 数学/统计学 **`+`** 业务领域  
    **`=>`** **传统研究**

在数据科学火起来之前，大家用的多是『数据分析』这个词。所以2个主题的书一起看，早些年典型的『数据分析』主题的书实际讲的是数据科学的内容。

❤️❤️
欢迎进入数据科学的世界！
❤️❤️

-----------------------------

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [0. 学习资料/书单](#0-%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99%E4%B9%A6%E5%8D%95)
- [1. 实践/开发环境搭建](#1-%E5%AE%9E%E8%B7%B5%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA)
    - [1.1 `Python`运行环境搭建](#11-python%E8%BF%90%E8%A1%8C%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA)
        - [1.1.1 安装`Anaconda`的`Python`发行版](#111-%E5%AE%89%E8%A3%85anaconda%E7%9A%84python%E5%8F%91%E8%A1%8C%E7%89%88)
        - [1.1.2 配置镜像源](#112-%E9%85%8D%E7%BD%AE%E9%95%9C%E5%83%8F%E6%BA%90)
        - [1.1.3 `Anaconda`的使用](#113-anaconda%E7%9A%84%E4%BD%BF%E7%94%A8)
    - [1.2 代码编写的环境](#12-%E4%BB%A3%E7%A0%81%E7%BC%96%E5%86%99%E7%9A%84%E7%8E%AF%E5%A2%83)
        - [1.2.1 `Jupyter Notebook`](#121-jupyter-notebook)
        - [1.2.2 `PyCharm`](#122-pycharm)
        - [1.2.3 `VS Code`](#123-vs-code)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

-----------------------------


# 0. 学习资料/书单

- [数据科学/Data Science](https://www.douban.com/doulist/119731263/)，个人推荐先看：
    - [深入浅出数据科学](https://book.douban.com/subject/30338984/)
    - [集体智慧编程](https://book.douban.com/subject/3288908/)
    - [Python数据科学手册](https://book.douban.com/subject/27667378/)
- [数据分析](https://www.douban.com/doulist/45963852/)，个人推荐先看：
    - [精益数据分析](https://book.douban.com/subject/26278639/)
    - [利用Python进行数据分析 原书第2版](https://book.douban.com/subject/30283996/)

可以看看了解

- [数据分析师和数据科学家有何区别？ - 知乎](https://www.zhihu.com/question/20935297)

# 1. 实践/开发环境搭建

`Python`已经成为数据科学/机器学习的首选实践/开发环境。  
\# 当然也可以使用`R` 或是 `Excel`，使用不同工具环境都可以实践数据科学。  
\# `Excel`，是的，没听错；`Excel`应该是使用人数最多的数据分析工具。

- `Python`繁荣与活跃生态 对 数据科学/机器学习 已经有了成熟的支持。
- `Python`作为通用编程语言，相对`R`、`Excel`而言，灵活性不可比拟。

## 1.1 `Python`运行环境搭建

**_`Anaconda`_**！

- 使用[`Anaconda`的`Python`发行版](https://www.anaconda.com/)已经成为数据科学/机器学习`Python`运行环境搭建的最佳实践！
- `Anaconda`快速提供了
    - 一个包含各种数据分析、机器学习的库的`Python`运行环境
    - 不同的`Python`版本/不同库的隔离环境
- 而无需在琐碎但没有价值的事情上浪费时间：
    - 各种库的安装过程
    - 不同库不同版本的兼容性问题

下面给下快速搭建数据科学/机器学习的`Python`运行环境的说明。

### 1.1.1 安装`Anaconda`的`Python`发行版

下载地址：

- https://www.anaconda.com/distribution/
- 照着网页上的说明，完成安装。

安装好了之后，执行

- `ipython` （加强`python`解释器）
- `jupyter-notebook` （基于`Web`浏览器里的一体化交互式环境）

命令，运行看看～ 🎉

如有问题，更多说明参见：https://www.jianshu.com/p/042fd657e2d4 ，或是搜索一下 :)

### 1.1.2 配置镜像源

在国内没有镜像可不行，包安装下载要等死。

- 配置`Anaconda`的镜像源
    - 使用清华的镜像：https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    - 通过命令行设置

            conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
            conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
            conda config --set show_channel_urls yes
    - 或是修改配置文件`~/.condarc`
- 配置`pip`的镜像源
    - 修改`~/.pip/pip.conf`：

            [global]
            trusted-host =  pypi.douban.com
            index-url = http://pypi.douban.com/simple

更多说明参见： https://mirror.tuna.tsinghua.edu.cn/help/anaconda/ 或是 搜索一下 :)

### 1.1.3 `Anaconda`的使用

下载安装后`Anaconda`的使用：

- 常见的`Anaconda`使用
- `Python`环境维护

👉 参见独立的文档：[`Anaconda`的使用](anaconda-usage.md)。

## 1.2 代码编写的环境

`Jupyter Notebook` | `PyCharm` | `VS Code`。

### 1.2.1 `Jupyter Notebook`

`Jupyter Notebook`已经在`Anaconda`的发行版本中有了。

提供基于`Web`浏览器里的一体化交互式环境，非常流行。试试用用，你会喜欢的。

### 1.2.2 `PyCharm`

`IDE`王者`JetBrains`提供`Python`开发的专业`IDE`。

- 强劲的代码编写提示支持
- 内置集成支持
    - 流行`Jupyter Notebook`的编写
    - `Anaconda`

如果你是`JetBrains`/`IntelliJ`的粉丝更会喜欢。

### 1.2.3 `VS Code`

无需多解释。

