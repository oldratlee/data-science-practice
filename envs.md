# 环境维护

环境维护的基本原则：

- `Base`环境完全不动。
- 为每个 学习主题（如书）或 工程开发 创建一个独立的环境。

相关资料：

- https://stackoverflow.com/questions/24405561/how-to-install-2-anacondas-python-2-and-3-on-mac-os

# 典型的环境

## data science python 3.7

```sh
conda create --name ds python=3.7.4 anaconda gensim tensorflow pymc3 &&
source activate ds
```

## data science python 3.7 with R

```sh
conda create --name dsr python=3.7.4 anaconda gensim tensorflow pymc3 r-base=3.6.1 r-essentials r-rbokeh &&
source activate dsr
```

## data science python 2.7 with R

```sh
conda create --name ds2r python=2.7.17 anaconda gensim tensorflow pymc r-base=3.6.1 r-essentials r-rbokeh &&
source activate ds2r
```

## 用于学习的环境

## `Principles-of-Data-Science`环境

用于学习书`Principles-of-Data-Science`的环境。

```sh
conda create -n Principles-of-Data-Science python=2.7 anaconda &&
source activate Principles-of-Data-Science
```

- https://github.com/PacktPublishing/Principles-of-Data-Science

# 用于安装`Python`工具的环境

## `Daily Tools`

用于日常工具的环境。

```sh
conda create --name daily-tools python=3.7 &&
source activate daily-tools &&
pip install git-up
```
