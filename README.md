# FastColl

[TOC]

本仓库源代码来自：http://www.win.tue.nl/hashclash/

本仓库主要贡献如下：
1. fastcoll初代代码版本过于久远，编译过程会报错
2. 提供适配新版g++和make的配置文件
3. 对fastcoll的功能进行总结与说明
4. 提供fastcoll编译教程


## 如何编译？

### 代码下载与编译

​	本项目代码已在github中开源。仓库地址为https://github.com/coronaPolvo/fastcoll。用户可以执行如下指令下载全部仓库：

```
git clone https://github.com/coronaPolvo/fastcoll.git
```

​	本项目需要在Linux下进行编译运行。在项目仓库中已提供好Makefile文件，用户可以通过以下命令编译运行：

```shell
make
```

### boost环境配置

​	在代码实现中使用了 C++ boost库因此需要配置boost的使用环境。配置步骤如下：

1. 在官网下载boost后解压
2. 进入到boost文件夹中以root权限运行./bootstrap.sh
3. 运行./b2 install

当然也可以直接使用系统源进行安装，比如ubuntu用户可以用如下命令进行安装：

```shell
sudo apt-get update
sudo apt-get install libboost-dev
```

我使用的boost版本是1.77.0

## 功能说明

你可以使用`./fastcoll -h`来查看可选的选项；

```
Allowed options:
  -h [ --help ]           Show options.
  -q [ --quiet ]          Be less verbose.
  -i [ --ihv ] arg        Use specified initial value. Default is MD5 initial 
                          value.
  -p [ --prefixfile ] arg Calculate initial value using given prefixfile. Also 
                          copies data to output files.
  -o [ --out ] arg        Set output filenames. This must be the last option 
                          and exactly 2 filenames must be specified. 
                          Default: -o msg1.bin msg2.bin
```



