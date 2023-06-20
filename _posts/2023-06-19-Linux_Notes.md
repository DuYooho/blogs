---
title: Linux 一些常见命令总结
author: Yooho
date: 2023-06-19
category: Jekyll
layout: post
---

## Linux打包、压缩、解压

首先区分一下打包和解压两个概念：

* 打包：指将一大堆小文件打包汇总成一个总的大文件
* 压缩：指将一个大文件通过压缩算法变成一个较小的文件


### tar命令

#### 打包/压缩

（1）仅打包:

```bash
tar -cvf foo.tar f1 f2 ...
```
其中，```fxxx``` 为要打包的文件/文件夹，```foo.tar``` 为打包之后的文件名，习惯 ```.tar``` 作为后缀


（2）打包并压缩
```bash
tar -zcvf foo.tar.gz f1 f2 ...
```
```-z``` 参数表示以 ```tar.gz``` 或者 ```.tgz``` 为后缀（经过gzip）压缩过的包

```bash
tar -jcvf foo.tar.bz2 f1 f2 ...
```
```-j``` 参数表示以```.tar.bz2``` 为后缀的压缩包


#### 解压

（1）在当前目录下直接解压
```bash
tar -zxvf foo.tar.gz
```
注意，如果这个目录下有同名的文件，不会询问，直接覆盖

（2）解压至指定文件夹
```bash
tar -zxvf foo.tar.gz -C <dir name>
```


### gzip 命令




### zip命令
