---
title: Linux编译安装sqlite3
abbrlink: 26535
date: 2023-01-19 20:26:05
tags:
excerpt: sqlite3是一个比较常用的程序模块，在编译一些程序的时候会依赖这个模块，但是我测试过程中发现，这个模块没法直接使用apt安装，即时用apt安装了也无法在编译验证脚本中通过，所以需要手动安装。
lang: cn
---
# 介绍
`sqlite3`是一个比较常用的程序模块，在编译一些程序的时候会依赖这个模块，但是我测试过程中发现，这个模块没法直接使用apt安装，即时用apt安装了也无法在编译验证脚本中通过，所以需要手动安装。
# 下载源码
首先需要从`sqlite3`的官网下载源码，下载链接：https://www.sqlite.org/download.html
![sqlite3下载页面](/img/26535/1.jpg)
找到`source code`，复制其中的链接，建议选择`.tar.gz`格式，因为`.zip`是没有编译脚本的，需要自行编译，非常复杂。
## 获取源码
``` bash
wget https://www.sqlite.org/2022/sqlite-autoconf-3400100.tar.gz
```
## 解压源码包
``` bash
tar -zvxf sqlite-autoconf-3400100.tar.gz
```
# 开始编译
## 进入目录
``` bash
cd sqlite-autoconf-3400100
```
## 检测&生成编译脚本
``` bash
./configure
```
![配置完成截图](/img/26535/2.jpg)
当看到类似如图信息时，就说明编译脚本生成成功了，如果没有出现这个可以阅读错误信息并尝试解决。
## 编译源码
``` bash
make
```
## 安装
![编译完成截图](/img/26535/3.jpg)
编译完成后会出现输入行，如果输出信息中没有报错就说明编译成功，然后就可以安装了
``` bash 
make install
```
## 检测
![安装完成截图](/img/26535/4.jpg)
安装过程会输出非常多内容，等到输出停止后就安装完成，如果没有报错就是安装成功，最后再检测是否被识别到
``` bash
pkg-config --libs sqlite3
```
![检测截图](/img/26535/5.jpg)
# 结尾
这篇教程到这里就结束了，如果你在操作过程中遇到问题可以在下方评论区留言，感谢您的耐心阅读