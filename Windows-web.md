# 将windows主机作为web应用的服务器

## 配置

* [Git for windows](http://blog.csdn.net/woodcorpse/article/details/79313846)

  + [解决Git Bah中文乱码的问题](https://blog.csdn.net/jfsufeng/article/details/79219673)

* [Xshell](https://www.filehorse.com/download-xshell-free/download/)

* [Apache](https://www.apachehaus.com/cgi-bin/download.plx)

* [Java]

* [Java JDK 15.0.1]()

* [MySQL 5.7]()

## MySQL


## Install Centos7 on windows

准备：

* 空的U盘（至少8G）

* 通过[磁盘管理](https://zhuanlan.zhihu.com/p/52141844)，分出cento7所需要的的空间，不要格式化！

  + win10-磁盘管理-压缩卷
  
  + 点击压缩卷后显示压缩后的磁盘是`未分配`的状态，`未分配`的磁盘，是无法显示的。

* [Cento7 镜像](https://www.centos.org/download/)

  + `DVD ISO`附带了安装图形用户界面和其他服务的附加选项，或者您可以选择没有GUI和附加功能的`Minimal ISO`。

* [Rufus](https://rufus.ie/): 实用程序的副本来创建可启动的USB驱动器

* 因为我们要使用USB复刻在电脑上安装Cento7系统，但是由于BIOS默认是从硬盘启动，因此首先需要设置开机启动项为从U盘启动。

**启动：**

windows开机时，点击F12，进入BIOS选择界面，选择Centos7启动

### 如何在Windows和Centos7系统之间切换？


