# `Python`环境

- 使用`Anaconda`的`Python`发行版
    - https://www.anaconda.com/distribution/
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
- 更多说明参见：
    - https://www.jianshu.com/p/042fd657e2d4
    - https://mirror.tuna.tsinghua.edu.cn/help/anaconda/

## 基本的`Anaconda`使用

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
- 更多说明参见：
    - [Anaconda介绍、安装及使用教程](https://zhuanlan.zhihu.com/p/32925500)
    - [用 Anaconda 完美解决 Python2 和 python3 共存问题](https://foofish.net/compatible-py2-and-py3.html)
    - [Updating from older versions — Anaconda documentation](https://docs.anaconda.com/anaconda/install/update-version/)
    - [Keeping Anaconda Up To Date - Anaconda](https://www.anaconda.com/keeping-anaconda-date/)

