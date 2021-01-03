**Step1: 用conda创建虚拟环境**

```bash
conda create -n venv-chopchop python=2.7
source activate venv-chopchop
```

**Step2: 安装虚拟依赖包**

```
conda install -n venv-chopchop biopython
conda install -n venv-chopchop pandas
conda install -n venv-chopchop numpy
conda install -n venv-chopchop pickle
conda install -n venv-chopchop scipy
conda install -n venv-chopchop argparse
conda install -n venv-chopchop scikit-learn==0.18.1
conda install -n venv-chopchop keras
conda install -n venv-chopchop bowtie==1.0.0
conda install -n venv-chopchop ucsc-twobittofa
```

**Step3: 运行测试代码**

```
./chopchop.py --targets chrXVI:701832-702235 -J -T 1 -M NGG --maxMismatches 3 -g 20 --scoringMethod DOENCH_2016 -f NN -G sacCer3 -t CODING -n N -R 4 -o sacCer3_temp/ > sacCer3_temp/results.txt 2> sacCer3_temp/python.err
```

**注：conda的`.condarc`文件内容如下**

```
ssl_verify: True
channels:
  - conda-forge
  - bioconda
  - defaults
```


**Installation commands for Win10 x64**

```
conda install -c msft-sqlserver-example scikit-learn
conda install -n venv-chopchop bowtie-py
```

说明：

* [bowtie2 is only available for Linux and OSX.](https://anaconda.org/bioconda/bowtie2)

**在Windows WSL-Ubuntu中安装bowtie和twobittofa**

```bash
sudo apt update
sudo apt install bowtie
```

```
# WSL-Ubuntu bash
cd /bin
wget http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/twoBitToFa
sudo chmod 755 twoBitToFa

# 由于需要区别大小写才能正常运行twoBitToFa
# 所以设置别名更方便

```

## WSL-UBUNTU-20.04

**[Windows和WSL互操作](https://docs.microsoft.com/zh-cn/windows/wsl/interop)：**

WSL-Ubuntu的`bin`目录：`C:\Users\Lenovo\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu20.04onWindows_79rhkp1fndgsc\LocalState\rootfs\usr\bin`

**WSL中安装Anaconda**

* [install Anaconda on WSL-Ubuntu 20.04](https://linuxize.com/post/how-to-install-anaconda-on-ubuntu-20-04/)

**WSL中conda虚拟环境**

* environment location: `/tmp/ENTER/envs/venv-chopchop`

* [Manage channels](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-channels.html)

**其他设置：**

* [Ubuntu中bash自动补全忽略大小写](https://blog.csdn.net/guyue35/article/details/52994766)


