# `Anaconda`的使用

-----------------------------

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [1. 常见的`Anaconda`使用](#1-%E5%B8%B8%E8%A7%81%E7%9A%84anaconda%E4%BD%BF%E7%94%A8)
- [2. 环境维护](#2-%E7%8E%AF%E5%A2%83%E7%BB%B4%E6%8A%A4)
    - [2.0 环境维护的基本原则/最佳实践](#20-%E7%8E%AF%E5%A2%83%E7%BB%B4%E6%8A%A4%E7%9A%84%E5%9F%BA%E6%9C%AC%E5%8E%9F%E5%88%99%E6%9C%80%E4%BD%B3%E5%AE%9E%E8%B7%B5)
    - [2.1 典型的环境](#21-%E5%85%B8%E5%9E%8B%E7%9A%84%E7%8E%AF%E5%A2%83)
        - [data science python 3.7](#data-science-python-37)
        - [data science python 3.7 with R](#data-science-python-37-with-r)
        - [data science python 2.7 with R](#data-science-python-27-with-r)
    - [2.2 用于学习的环境](#22-%E7%94%A8%E4%BA%8E%E5%AD%A6%E4%B9%A0%E7%9A%84%E7%8E%AF%E5%A2%83)
        - [书《深入浅出数据科学》学习环境](#%E4%B9%A6%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BA%E6%95%B0%E6%8D%AE%E7%A7%91%E5%AD%A6%E5%AD%A6%E4%B9%A0%E7%8E%AF%E5%A2%83)
    - [2.3 用于安装`Python`工具的环境](#23-%E7%94%A8%E4%BA%8E%E5%AE%89%E8%A3%85python%E5%B7%A5%E5%85%B7%E7%9A%84%E7%8E%AF%E5%A2%83)
        - [`Daily Tools`](#daily-tools)
- [3. 更多说明参见](#3-%E6%9B%B4%E5%A4%9A%E8%AF%B4%E6%98%8E%E5%8F%82%E8%A7%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

-----------------------------

# 1. 常见的`Anaconda`使用

- 管理环境
    - 创建新环境：`conda create --name <env_name> <package_names>`
        - 安装`Python 2`：`conda create --name foo_env_name python=2.7`
        - 安装`Python 3`：`conda create --name bar_env_name python=3.7`
    - 切换环境：`source activate <env_name>`
    - 退出环境：`conda deactivate` / `source deactivate`
    - 显示已创建环境：`conda info --envs` / `conda env list`
    - 复制环境：`conda create --name <new_env_name> --clone <copied_env_name>`
    - 删除环境：`conda remove --name <env_name> --all`
- 管理包
    - 查找可供安装的包版本
        - `conda search <text>`
        - `conda search --full-name <package_full_name>`
    - 获取当前环境中已安装的包信息：`conda list`
    - 安装包：
        - 在当前环境中安装包：`conda install <package_name>`
        - 在指定环境中安装包：`conda install --name <env_name> <package_name>`
        - 当使用`conda install`无法进行安装时，可以使用`pip`进行安装。
            - `pip install <package_name>`
    - 更新包：
        - 更新所有包：`conda update --all` / `conda upgrade --all`
        - 更新指定包：`conda update <package_name>` / `conda upgrade <package_name>`
    - 卸载包：
        - `conda remove <package_name>`
        - `conda remove --name <env_name> <package_name>`
- 更新`Anaconda`自身：
    - `conda update conda`
    - `conda update anaconda`

# 2. 环境维护

## 2.0 环境维护的基本原则/最佳实践

- `Base`环境完全不动。
    - 不要搞坏`Anaconda`本身 😂
- 提供典型的环境。
    - 比如 `Python 3`、`Python 2`的数据科学环境。
- 如果 一个开发工程 或 一个学习主题（如学习一本书）有典型环境不满足的需求（比如要安装一个特有的包），则为它创建一个独立的环境。
    - 不要搞坏典型的环境 😂
- 日常工具的环境。

相关资料：

- https://stackoverflow.com/questions/24405561/how-to-install-2-anacondas-python-2-and-3-on-mac-os

## 2.1 典型的环境

### data science python 3.7

```sh
conda create --name ds python=3.7.4 anaconda gensim tensorflow pymc3 &&
source activate ds
```

### data science python 3.7 with R

```sh
conda create --name dsr python=3.7.4 anaconda gensim tensorflow pymc3 r-base=3.6.1 r-essentials r-rbokeh &&
source activate dsr
```

- 安装上了`R`的运行环境
- 同时在`Jupyter Notebook`也支持上了`R` 😻

### data science python 2.7 with R

```sh
conda create --name ds2r python=2.7.17 anaconda gensim tensorflow pymc r-base=3.6.1 r-essentials r-rbokeh &&
source activate ds2r
```

## 2.2 用于学习的环境

### 书《深入浅出数据科学》学习环境

```sh
conda create -n Principles-of-Data-Science python=2.7 anaconda &&
source activate Principles-of-Data-Science
```

- 《深入浅出数据科学》的豆瓣链接：https://book.douban.com/subject/30338984/
- 代码库： https://github.com/PacktPublishing/Principles-of-Data-Science

## 2.3 用于安装`Python`工具的环境

### `Daily Tools`

用于日常工具的环境。

```sh
conda create --name daily-tools python=3.7 &&
source activate daily-tools &&
pip install git-up
```

# 3. 更多说明参见

- [Anaconda介绍、安装及使用教程](https://zhuanlan.zhihu.com/p/32925500)
- [用 Anaconda 完美解决 Python2 和 python3 共存问题](https://foofish.net/compatible-py2-and-py3.html)
- [Updating from older versions — Anaconda documentation](https://docs.anaconda.com/anaconda/install/update-version/)
- [Keeping Anaconda Up To Date - Anaconda](https://www.anaconda.com/keeping-anaconda-date/)
- [Using R language with Anaconda — Anaconda documentation](https://docs.anaconda.com/anaconda/user-guide/tasks/using-r-language/)
