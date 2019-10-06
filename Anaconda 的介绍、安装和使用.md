# Anaconda 的介绍、安装和使用

## 一、anaconda介绍

- Anaconda 是一个用于科学计算的 Python 发行版，支持 Linux, Mac, Windows, 包含了众多流行的科学计算、数据分析的 Python 包。

- Anaconda 实际上是一个软件发行版，它附带了 conda、Python 和 150 多个科学包及其依赖项。应用程序 conda 是包和环境管理器。Anaconda 的下载文件比较大（约 500 MB），因为它附带了 Python 中最常用的数据科学包。如果只需要某些包，或者需要节省带宽或存储空间，也可以使用 Miniconda 这个较小的发行版（仅包含 conda 和 Python）。但你仍可以使用 conda 来安装任何可用的包，它只是自身没有附带这些包而已。	

## 二、anaconda的安装

- 这里可以使用清华大学的anaconda的源，可以查看清华大学的[Anaconda 镜像使用帮助](https://mirror.tuna.tsinghua.edu.cn/help/anaconda/)。
- `cd /Downloads`   进入Downloads 文件夹下。
- `wget https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-5.3.1-Linux-x86_64.sh  `   这里下载最新版的Anaconda。
- `bash Anaconda3-5.3.1-Linux-x86_64.sh  `  运行.sh文件。
- 进入注册页面信息，输入yes，后面一直确认就完成安装了。
- 打开终端并输入 `sudo gedit ~/.bashrc`   文件末尾添加路径`#export PATH=/home/xxx/anaconda3/bin:$PATH'`,执行 `source ~/.bashrc`  使其生效。(xxx 是你的用户名)



## 三、anaconda的配置

- 修改 用户目录下的`~/.condarc`  隐藏文件 `gedit ~/.condarc` 把里面的内容全部替换成如下，就可以使用TUNA的Anaconda仓库和第三方源。

  ```
  channels:
    - defaults
  show_channel_urls: true
  default_channels:
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  custom_channels:
    conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  ```



## 四、Anaconda的相关命令

- 查看conda版本： `conda --version`

- 安装 `conda install <包名>`        安装不同版本的包时 需要用 `=` 指明版本 例如：`conda install cudatoolkit=8.0`

- 移除 `conda remove <包名>`

- 更新 `conda update <包名>`

- 列出安装包： `conda list`

- 创建环境  `conda create -n name python=3.6`  name 为你要创建的环境名。

- 删除环境 `conda remove -n name --all`

- 激活环境 `source activate name`

- 退去环境 `source deactivate`

- 显示conda 的config 信息 `conda config --show`

- 显示源 `conda config --show channels`  

- 移除清华的源 `conda config --remove channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/`

- 添加清华的源 

  ```
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  conda config --set show_channel_urls yes
  ```

  



## 五、卸载Anaconda

- 删除整个anaconda目录：到包含整个anaconda目录的文件夹下，删除整个Anaconda目录

  `rm -rf anaconda3`

- 清理下.bashrc中的Anaconda路径: 

  - `sudo gedit ~/.bashrc`
  - 删除文件末尾的路径 `#export PATH=/home/xxx/anaconda3/bin:$PATH`	