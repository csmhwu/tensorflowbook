# 附录 1 工欲善其事必先利其器：TensorFlow开发环境搭建

#### &gt; 下载及安装Anaconda开发工具

Anaconda是Python的一个科学计算发行版，内置了上千个Python经常会用到的库，包括Scikit-learn、NumPy、SciPy、Pandas等。

它的官网是：[https://www.anaconda.com](https://www.anaconda.com/)

它支持Windows、macOS以及Linux。

我们只需要下载Python 3.6 version就可以了。

![&#x56FE;1-1](../.gitbook/assets/image%20%28183%29.png)

由于从官网上下载速度可能比较慢，所以建议从国内的镜像网站上下载。

我们可以通过清华映像站来下载Anaconda。

首先，我们打开这个网址：[https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/)

里面有许多Anaconda的版本，我们根据教学需要，选择Anaconda3-4.2.0的版本。大家可以根据自己的操作系统版本选择相应的安装包文件进行下载。

![&#x56FE;1-2](blob:https://minghuiwu.gitbook.io/e16f2fd9-9c68-4699-967c-afae66dfdd11)

这里以Anaconda3-4.2.0-Windows-x86\_64.exe为例来解释一下文件名的含义：3-是Python版本3.x，Windows-x86是32位系统，Windows-x86\_64是64位系统。



接下来我们进行Anaconda的安装。

我们以Windows10系统为例。下载完成后是一个大约400M的文件。

![&#x56FE;1-3](blob:https://minghuiwu.gitbook.io/02a64c53-4cb1-4333-a518-f45a70b0d357)

接下来只要选择Next和I Agree就可以了，整个安装过程大概五分钟左右。

![&#x56FE;1-4](blob:https://minghuiwu.gitbook.io/f29fbba7-2bac-4e81-9eb4-6f601cbc320b)

在安装好了以后，我们可以看到在目录中多了一个Anaconda3的文件夹。

![&#x56FE;1-5](blob:https://minghuiwu.gitbook.io/ae0cd2b5-c6c9-4676-a238-fe43e9cd5030)

这里有许多的程序，在之后我们会用到比较多的是Anaconda Prompt以及Jupyter Notebook。



#### &gt; 下载及安装TensorFlow

下一步，我们需要在Anaconda中安装TensorFlow。

不过在安装TensorFlow之前，我们最好先修改一下扩展包下载的位置，因为直接从国外的网站下载还是比较慢，所以我们先做一个修改国内镜像源的操作。

通过conda config命令生成配置文件，在这个配置文件里会指定从哪里去下载将要下载的扩展包。在这里呢，我们使用清华的镜像：[https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/](https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/)

首先，我们打开Anaconda Prompt窗口，执行命令：

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/

然后执行命令：

conda config --set show\_channel\_urls yes

![&#x56FE;1-6](blob:https://minghuiwu.gitbook.io/90a80a4b-be84-4dbc-8440-d91521ab2a03)

之后，我们到用户的目录底下找到.condarc文件。

![&#x56FE;1-7](blob:https://minghuiwu.gitbook.io/d55e3ed2-5871-44f7-8e1a-56a666bf80c9)

用编辑软件（记事本就可以）打开. condarc文件，删除第三行：– defaults，再保存文件即可（图1-8是原文件，图1-9是删除后的文件），镜像源就修改好了。

![&#x56FE;1-8](blob:https://minghuiwu.gitbook.io/a4bcd3ce-42a7-4bf4-a219-dba866bb7561)

![&#x56FE;1-9](blob:https://minghuiwu.gitbook.io/c1b1c9d5-1df8-467a-98e4-c729e1164079)



我们知道TensorFlow有支持GPU的版本，有条件的话，可以安装GPU版本。在教学过程中，我们安装普通CPU的版本即可。

安装普通版TensorFlow命令为：conda install tensorflow

安装GPU版TensorFlow命令为：conda install tensorflow-gpu

![&#x56FE;1-10](blob:https://minghuiwu.gitbook.io/2865ac7c-e110-4203-9ec2-af9d73ec8ae8)

接下来它会去相应的网站下载安装包，大约需要几分钟的时间。

TensorFlow的安装依赖于MSVCP140.DLL，如果安装过程中报相关错误信息，请确定是否已经有安装过Visual C++ 2015 redistributable（x64 version），并且在%PATH%里。

Visual C++ 2015 redistributable的下载网址如下：

[https://www.microsoft.com/en-us/download/details.aspx?id=53587](https://www.microsoft.com/en-us/download/details.aspx?id=53587)



安装完毕后，需要测试TensorFlow是否安装成功，我们会用到刚刚提到的Jupyter Notebook。

双击打开Jupyter Notebook。它实际上会先启动一个本地后台的服务器，然后通过浏览器的模式去做编辑和运行（浏览器会自动弹出）。

![&#x56FE;1-11](blob:https://minghuiwu.gitbook.io/512b5ae8-7e53-4399-80a9-e8aec893ee24)

![&#x56FE;1-12](blob:https://minghuiwu.gitbook.io/7b813c48-317b-4dd9-9c4c-28abbaa7de1e)

我们点开右上角的New，选择下图中红框所示的Python\[conda root\]

![&#x56FE;1-13](blob:https://minghuiwu.gitbook.io/dcb88693-ba75-4120-a415-6ac917505fce)

它会新建一个Untitled的文件。我们在第一行中输入：

import tensorflow as tf

tf.\_\_version\_\_

注意：第二行输入中的下划线是两个下划线

然后可以用快捷键Ctrl+Enter执行

![&#x56FE;1-14](blob:https://minghuiwu.gitbook.io/bb334cb0-066b-4bd9-b275-3c0111940b76)

可以看到输出的结果为1.2.1，说明TensorFlow的版本为1.2.1，这时我们的TensorFlow就已经安装成功了。

![&#x56FE;1-15](blob:https://minghuiwu.gitbook.io/90b1f847-b8e0-4004-b1fb-6a7d4dc779b2)

