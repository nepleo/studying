# Ubuntu 日常指令及问题处理

## 日常指令

- `wget -c`  获取网站上的安装包

- `sudo modprobe -r psmouse`  关闭鼠标

- `sudo modprobe psmouse`   打开鼠标

- `df -h `  列出磁盘目录

- `lsblk`  列出电脑上所有的磁盘结构

- `chmod +x`  赋予文件权限

- `ls -hl`  列出此目录下 文件的详细信息

- `tar -zxvf`  解压缩 压缩包

- `dpkg -i `  Ubuntu 下安装包 一般安装在 `/opt`  文件夹下

- `nake -j8`  用八个核对文件 编译

- `make clean`  清楚 之前make 的结果

- `find / -name`  查找根目录下 的文件

- `ifconfig`  输出网络信息 ，例如IP地址

- `g++ -g -o a.out xxx.cpp`     `./a.out`   vscode  调试时的命令

- `sudo add-apt-repository ppa:user/ppa-name` 添加软件源 

- `sudo add-apt-repository -r ppa:user/ppa-name`  删除软件源  进入 `/etc/apt/sources.list.d `目录，将相应 ppa 源的保存文件删除

- `ubuntu-drivers devices`   Ubuntu 的驱动， 安装推荐驱动 `sudo ubuntu-drivers autoinstall`   否者 apt 安装。

- `sudo apt purge xxx*`  完全 卸载

- `nohup python -u main.py --dataset selfie2anime > log.txt 2>&1 &`   进程后台执行并将输出写入日志，最后结束时 需要  使用 <u>`exit`</u>  退出 ， 注意  -u  的指令。

- `ps -aux`  显示所有的进程

- `top`  显示 CPU的运行情况

- `nvidia-smi -l`   每秒显示NVIDIA 的显卡状态

- `cat`  查看文件状态  

  

 





## 问题处理

1. 更改python默认版本

   - `update-alternatives --install /usr/bin/python python /usr/bin/python3`

   - `update-alternatives --config python`

     

     