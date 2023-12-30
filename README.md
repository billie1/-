# -2023年计算机体系结构大作业论文复现

## 环境
+ ubantu 18.04

## 数据集
2012 memory scheduling championship (MSC). 每个工作负载包含 5 亿条代表性指令，这些指令是从 PARSEC 和商业基准中选出的，其方法类似于 Simpoint。整个数据集可以在这个页面下载 [this page](https://www.cs.utah.edu/~rajeev/jwac12/results_table.html).
由于数据集太大，传不上来，所以可以在这个网站上下载，下载的压缩包名为`jwac_msc_workloads_first18_workloads.tar`，解压到`input`文件夹即可

## 设置模拟指令
模拟指令在文件“run_GreenORAM”中设置。在每条指令中，您需要指定内存通道大小、输入文件和输出文件。您可以按如下方式编写指令：
```sh
bin/usimm input/1channel.cfg input/black > output/black_GreenORAM
```

## make and run
完成上述准备工作后，您可以使用以下命令编译项目并运行模拟：
```sh
cd src
make clean
make
cd ..
./run_GreenORAM
```
