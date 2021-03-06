# 将windows主机作为web应用的服务器

## 配置目录

* [Git for windows](http://blog.csdn.net/woodcorpse/article/details/79313846)

  + [解决Git Bah中文乱码的问题](https://blog.csdn.net/jfsufeng/article/details/79219673)
  
  + 管理员身份启动git Bash: git bash快捷方式上“右键”-->"属性"-->“兼容性”-->勾选“以管理员身份xxx”-->“确定”

* [Xshell](https://www.filehorse.com/download-xshell-free/download/)

* [Apache](https://www.apachehaus.com/cgi-bin/download.plx)

* [Java JDK 15.0.1]()

* [MySQL 5.7]()

* [WSL (Windows Subsystem for Linux) - Ubuntu 20.04](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

  + [Windows 和 WSL 互操作](https://docs.microsoft.com/zh-cn/windows/wsl/interop)
  
  + [install Anaconda on WSL-Ubuntu 20.04](https://linuxize.com/post/how-to-install-anaconda-on-ubuntu-20-04/)
  
  + [Manage conda channels](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-channels.html)
  
  + WSL-Ubuntu中使用conda创建虚拟环境的路径在: `/tmp/ENTER/envs/venv-name`

# 1. MySQL

* [下载地址](https://dev.mysql.com/downloads/installer/) (我安装的5.7)

* [安装指南](https://www.runoob.com/w3cnote/windows10-mysql-installer.html)
  + 安装过程中设置跟用户名和登陆密码
  + 添加环境变量
  + 从`gitbash`, `cmd`, `powershell`, 或者mysql专门的`MySQL Command Line Client`窗口都可进入mysql命令行界面

* 从`gitbash`登入mysql有bug

如果直接在`gitbash`中使用`mysql -uUser-name -pPassword`(注意参数后没空格)，即使登陆成果，终端中不会出现`mysql>`的标识提醒你已进入mysql命令行，并且不会展示出mysql语句运行的结果。

对于这个bug，只要把进入mysql的命令换成`winpty mysql -uUser-name -pPassword`即可。

[详见：Gitbash如何支持交互式命令？如何让gitbash的命令不乱码？winpty是什么？](https://www.cnblogs.com/saysmy/p/9970247.html)

# 2. WEB服务器

Apache和Nginx都安装了，装了多个web服务器要防止80端口被占用。

* [Apache VS. Nginx](https://yq.aliyun.com/articles/586791)

* [Nginx版本名区别](https://www.cnblogs.com/ppgs8903/p/4343259.html)

* [Win10 上安装Nginx](https://www.jianshu.com/p/d2f30962e8ce)

* 80端口被占用怎么修改；

* apache配置文件 中Listen 8080与ServerName localhost:8080区别是什么?

  + `listen 8080`是设置服务器监听端口
  + `ServerName localhost:8080`只是设置服务器的注册名称，无论你加不加8080, 实际你都要使用8080端口才能触发服务器

# 3. 安装SWL-Ubuntu20.04

* [WSL (Windows Subsystem for Linux) - Ubuntu 20.04](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

* [Windows 和 WSL 互操作](https://docs.microsoft.com/zh-cn/windows/wsl/interop)

  + WSL中运行Windows中的可执行文件要加上后缀`.exe`
  
  + WSL中可通过`/mnp`路径访问Windows系统中的文件
  
  + 可以通过在WSL中运行`ln -R /mnp/E/filePath`把想要操作的Windows文件创建一份软连接到WSL中
  
* [install Anaconda on WSL-Ubuntu 20.04](https://linuxize.com/post/how-to-install-anaconda-on-ubuntu-20-04/)
  
  + [Manage conda channels](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-channels.html)
  
  + WSL-Ubuntu中使用conda创建虚拟环境的路径在: `/tmp/ENTER/envs/venv-name`
  
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

## Anaconda

* [Windows 10 + Anaconda环境配置](https://blog.csdn.net/u013211009/article/details/78437098)

* [conda创建虚拟环境、安装chopchop运行依赖包](https://github.com/ludidiya/iSynBio-PD/blob/main/chopchop_test.md)


