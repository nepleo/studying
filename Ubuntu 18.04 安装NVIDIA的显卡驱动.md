# Ubuntu 18.04 安装NVIDIA的显卡驱动

​	之前一段时间利用老师实验室闲置的两个NVIDIA GTX1080TI的显卡学习深度学习，在系统的安装上费了不少功夫。注意：<u>cuda 无法与nvidia-driver-418</u>  共存。在安装cuda的过程中会删除显卡驱动的相关依赖。所以后面无法执行 `nvidia-smi -l`  查看显卡的状态。

​	解决方案：下载anaconda，在anaconda中创建一个虚拟环境，执行 `conda install cudatoolkits=9.0`  在此虚拟环境中运行即可。

- ## 卸载cuda

  `sudo apt remove cuda`  移除cuda相关的组件， `sudo apt autoremove`  移除相关的组件，以免后面的依赖相冲突。

- ## 添加NVIDIA的第三方软件仓库 

  - 添加 PPA 软件仓库：`sudo add-apt-repository ppa:graphics-drivers/ppa`，需要输入用户密码，按照提示还需要按下 Enter 键。

  - 更新软件索引：`sudo apt update`



- ## 查看显卡驱动

  - 在终端输入：`ubuntu-deivers devices`
  - 推荐安装 `sudo ubuntu-drivers autoinstall`
  - 若想自行安装 `sudo apt install xxx`  即可

  

  

  

  



  