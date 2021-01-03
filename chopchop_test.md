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
