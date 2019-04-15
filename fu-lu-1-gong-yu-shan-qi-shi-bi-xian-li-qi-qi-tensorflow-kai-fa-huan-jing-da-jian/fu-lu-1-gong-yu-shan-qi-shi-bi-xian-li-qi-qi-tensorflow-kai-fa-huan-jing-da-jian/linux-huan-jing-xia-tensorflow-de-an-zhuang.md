---
description: Linux环境下TensorFlow的安装
---

# 1.2 Linux环境下TensorFlow的安装

## Linux环境（Ubuntu 18.04 发行版）下TensorFlow的搭建

贡献人：浙江大学城市学院 王傲然

### 1. 安装Anconda

Anaconda 是一个用于科学计算的 Python 发行版，支持 Linux, Mac, Windows, 包含了众多流行的科学计算、数据分析的 Python 包。

Anaconda 安装包可以到清华源 [https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/) 下载。

在该网站下找到[Anaconda3-5.2.0-Linux-x86\_64.sh](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-5.2.0-Linux-x86_64.sh)这个版本，如果你的电脑是32位的，选择Anaconda3-5.2.0-Linux-x86.sh。

\#在下载的目录中键入命令

`bash Anaconda3-5.2.0-Linux-x86_64.sh`

开始安装

![&#x56FE;1](../../.gitbook/assets/image%20%28307%29.png)

### 2. TensorFlow 开发环境搭建

使用Anaconda自带的Python包管理工具conda即可进行安装。

打开终端，命令如下：

`conda install tensorflow`

如需获取GPU支持则输入命令

`conda install tensorflow-gpu`

在使用GPU版本的Tensorflow之前，首先要确保计算机满足以下几个条件

* 计算机中带有NVIDIA®计算能力大于3.0的显卡
* 已经在Linux系统中安装好NVIDIA® GPU drivers，并且符合CUDA版本要求
* 安装CUDA® Toolkit
* （可选）CUDA® Deep Neural Network library（CUDNN）

详情可见Tensorflow官网对于GPU支持的说明：[https://www.tensorflow.org/install/gpu](https://www.tensorflow.org/install/gpu)

Conda会对当前环境进行自动配置,同时也会安装除显卡驱动以外的所需依赖，一般来说只要显卡驱动版本满足CUDA®的最低要求其他的Conda都会帮你搞定。

![&#x56FE;3](../../.gitbook/assets/image%20%28186%29.png)

最终显示下图则安装成功

![](../../.gitbook/assets/image%20%2857%29.png)

