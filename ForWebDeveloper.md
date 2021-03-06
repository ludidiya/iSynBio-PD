针对生物网站开发，如果涉及到基因组的展示，建议后端开发人员先学习了解以下基础知识：

* 基因的DNA双螺旋结构
* 碱基反向互补原则
* 中心法则
* 学习基因信息的存储方式以及格式的区别......

对于前端页面设计者，最有挑战的是设计灵活、符合项目需求的DNA可视化界面。此处的灵活可能包括的功能有：

* 像文本工具一样的选择、复制、粘贴、搜索、插入等功能；
* 定位查找；
* zoom in and out；
* 不同属性的部分展示不同的样式；
* 根据用户操作实时变化试图；



# 1. 常用数据库

[生信 / 数据库 / 分类整理](https://www.jianshu.com/p/5c4ecdf0534a)

[生信分析常用基因组数据库汇总](https://www.jianshu.com/p/29202d721ef4)

生物数据库众多，不同分类标准有对应不同的数据库，但是最常用的有：

* [NCBI](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.ncbi.nlm.nih.gov%2Fassembly%2F%3Fterm%3D)目前最常用的综合性基因组数据库;

* [Ensembl](https://links.jianshu.com/go?to=http%3A%2F%2Fasia.ensembl.org%2Findex.html)
* [UCSC](https://links.jianshu.com/go?to=http%3A%2F%2Fgenome-asia.ucsc.edu%2Fcgi-bin%2FhgGateway%3Fredirect%3Dmanual%26source%3Dgenome.ucsc.edu)
* [Swiss-Prot/Uniprot](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.uniprot.org%2F)
* [Pfam](https://links.jianshu.com/go?to=http%3A%2F%2Fpfam.xfam.org%2F)
* [PDB](https://links.jianshu.com/go?to=http%3A%2F%2Fwww.rcsb.org%2F)
* [Reactome](https://links.jianshu.com/go?to=https%3A%2F%2Freactome.org%2F)
* [KEGG](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.kegg.jp%2F)
* [Biomodels](https://links.jianshu.com/go?to=http%3A%2F%2Fbiomodels.caltech.edu%2F)

# 2. 数据格式

## 2.1 常见基因组文件格式

[UCSC上总结的所有基因组文件类型，以及对应的格式](https://genome.ucsc.edu/FAQ/FAQformat.html)

最常见的主要是以下几种：

* FASTA
* FASTQ
* GFF/GTF
* SAM
* BAM
* 其他

在有的情况下可能需要我们自己解析[GenBank格式的文件](https://www.ncbi.nlm.nih.gov/Sitemap/samplerecord.html), 而解析方法可以直接使用[biopython](https://biopython-cn.readthedocs.io/zh_CN/latest/index.html)

## 2.2 生物模型格式

* [SBML](http://sbml.org/Documents/Specifications#SBML_Level_3_Version_2_Core)
* [SBOL](https://sbolstandard.org/)

# 2. 常用软件工具

## 2.1 Bash scripts

* QC: [fastqc](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/), [multiqc](https://multiqc.info/)
* Reads to contigs: [velvet](https://www.ebi.ac.uk/~zerbino/velvet/), [SPAdes](https://cab.spbu.ru/software/spades/), [Cufflinks](http://cole-trapnell-lab.github.io/cufflinks/)...
* Align reads to reference sequence: [SHRiMP](http://compbio.cs.toronto.edu/shrimp/), [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml), [BWA](http://bio-bwa.sourceforge.net/), [tophat](http://ccb.jhu.edu/software/tophat/index.shtml)...
* Variant identification: [GATK](https://gatk.broadinstitute.org/hc/en-us)
*  [SAMTools](http://www.htslib.org/)
* [bedtools](https://bedtools.readthedocs.io/en/latest/index.html)
* Alignment:
  * BLAST
  * Clustal Omega
  * Clustalw2
  * Kalign
  * MAFFT
  * MUSCLE

## 2.2 Python

* [<u>***BioPython***</u>](https://biopython-cn.readthedocs.io/zh_CN/latest/index.html) ! ! ! ! !



# 3. Web Development/Visualization/Plugin

## 3.1 基因组浏览器

* [IGV官网（可下载桌面应用）](https://software.broadinstitute.org/software/igv/home)，[IGV.js浏览器插件](https://github.com/igvteam/igv.js)
* [Embed the UCSC genome browser graphic in your web page](https://genome.ucsc.edu/goldenPath/help/mirror.html#considerations-before-installing-a-genome-browser)
* [GIVE - Genomic Interaction Visualization Engine](https://zhonglab.gitbook.io/3dgenome/chap4-integrative-data-visualization-tools/4.1give)
* [NCBI Graphical Sequence Viewer Embedding API](https://www.ncbi.nlm.nih.gov/tools/sviewer/embedding-api/), [Using the Sequence Viewer Embedding API](https://www.ncbi.nlm.nih.gov/tools/sviewer/manual-api/)
* [JBrowse Configuration Guide](http://gmod.org/wiki/JBrowse_Configuration_Guide), [GitHub](https://github.com/GMOD/jbrowse/wiki/JBrowse_Configuration_Guide)
* [WebApollo Configuration](https://genomearchitect.readthedocs.io/en/1.0.4/Configure/)
* [Epigenome](http://epigenomegateway.wustl.edu/browser/)

还有些github开源项目：
* [Teselagen OpenVectorEditor](https://github.com/TeselaGen/openVectorEditor)
* [nebiolabs IGV-snapshot-automator](https://github.com/nebiolabs/IGV-snapshot-automator)



## 3.2 统计图表展示

* [Plotly.js](https://plot.ly/javascript/)
* [CanvasJS](https://canvasjs.com/)
* [TOAST UI Chart](https://ui.toast.com/tui-chart)
* [GoJS](https://gojs.net/latest/index.html) is a JavaScript diagramming library for interactive flowcharts, org charts, design tools, planning tools, visual languages.
* [C3.js](https://c3js.org/) is a D3-based reusable chart library.
* [dimple](http://dimplejs.org/) is an object-oriented API for business analytics powered by D3.
* [Charted](https://www.charted.co/), by Medium, is a tool that automatically visualizes data. You just give it a link to a data file. (You can read more about it [at Medium](https://medium.com/data-lab/introducing-charted-15161b2cd71e).)
* [Smoothie Charts](http://smoothiecharts.org/) can be helpful, if you are dealing with stream real-time data.
* [Chartkick.js](https://github.com/ankane/chartkick.js) is a library that allows you to create beautiful charts with one line of JavaScript.
* [Morris.js](http://morrisjs.github.io/morris.js/) is a powerful library with a clean interface. It allows you to create good-looking charts with ease. It’s based on jQuery and the Raphaël JavaScript library.

## 3.3 网络图

* [ESCHER](https://escher.github.io/#/)



# 生物信息相关知识-思维导图

![](https://raw.githubusercontent.com/jmzeng1314/bioinformatics123/master/bioinformatics.png)

made by [@jmzeng1314](https://github.com/jmzeng1314)
