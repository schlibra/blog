---
title: JetBrains全家桶激活教程
abbrlink: 28544
excerpt: >-
  在很多年前，我无意间听说了Jetbrains这家公司，发现他们的IDE各个都是宝藏，功能非常强大，但是美中不足的是大部分软件都收费，于是今天这篇文章就要来讲讲如何正确使用(白嫖)Jetbrains全家桶。
date: 2023-01-16 23:36:49
tags:
lang: cn
---
# 前言
在很多年前，我无意间听说了`Jetbrains`这家公司，发现他们的IDE各个都是宝藏，功能非常强大，但是美中不足的是大部分软件都收费，于是今天这篇文章就要来讲讲如何轻松激活(~~白嫖~~)Jetbrains全家桶。
# 下载安装
## 下载
首先我们需要从jetbrains官网下载一个IDE的安装包，这次我以`PHPStorm`为例，因为~~PHP是世界上最好的语言~~，别的IDE操作基本一致，除了部分特殊的IDE可能无法激活，常用的IDE基本都可以正常激活。
![Jetbrains官网顶部截图](/img/28544/1.jpg)
打开官网：https://www.jetbrains.com/ ，选择顶上的`Developer Tools`，在弹出菜单里选择需要的IDE，然后点击`Download Now`，部分IDE有提供`Community版`(社区版)，例如Idea，社区版是免费的，但是功能相对较少，我们需要选择`Ultimate`，即旗舰版。
![Idea下载页面](/img/28544/2.jpg)
## 安装
下载完成后，双击安装包进行安装
![下载完成截图](/img/28544/3.jpg)
点击Next，可以选择更改安装位置，再次点击Next，出现一些选项
![安装选项](/img/28544/4.jpg)
其中第一项是软件在桌面上的快捷方式，右边的是将bin添加到环境变量中，用于使用指令启动IDE，第三项是将IDE快捷打开选项加入右键菜单项，这项建议**不要勾选**，下方的是文件关联，勾选后在打开指定文件时将会打开这个IDE，这个根据自己的情况选择就行，再次点击Next，在开始菜单中创建目录，这里不用更改，点击Install
![安装中](/img/28544/5.jpg)
这时候就开始安装了，这个过程耗时比较长，和硬盘读写速度有关，需要耐心等待。
![安装完成](/img/28544/6.jpg)
这个时候就安装完成了，取消勾选`run XXX`，然后点击finish
# 下载激活补丁
激活补丁需要从http://jetbra.in/s 这个网站下载，考虑到大家可能不愿意自己下载，我把下载链接放在下方
{% note success no-icon %}
### 激活补丁下载链接
清北网盘下载：https://pan.tsinbei.com/s/bNuz
蓝奏云下载：https://schlibra.lanzouo.com/i8rms0l88o5c
123云盘下载：https://www.123pan.com/s/xE9lVv-AJSKd
提取码：2854
{% endnote %}
下载完成后解压压缩包，将里面的文件夹放到一个你熟悉的位置，我将它放在C盘根目录，进入scripts目录，执行`install-all-users.vbs`，如果你是Linux用户，那么就执行`install.sh`
![执行脚本](/img/28544/7.jpg)
在第一次弹窗后点击`Ok`，然后等待一段时间，会弹窗提示`Done`这个时候就生成好配置文件了
![执行结果](/img/28544/8.jpg)
返回上级目录，进入`vmoptions`目录，同时打开一个新窗口，进入IDE的安装目录
![目录](/img/28544/9.jpg)
将安装目录中的`phpstorm64.exe.vmoptions`文件备份（不建议直接删除），然后将`vmoptions`目录中的`phpstorm.vmoptions`复制到安装目录中，并重命名为`phpstorm64.exe.vmoptions`，注意不同的IDE文件名会有所不同，请自行变通。
{% note info no-icon %}
注意：如果你是Linux用户，那么这个文件名就是`phpstorm64.vmoptions`而不是`phpstorm64.exe.vmoptions`，也就是没有`.exe`，操作相同，另外的IDE类似
{% endnote %}
# 激活IDE
在复制完配置文件后，整个激活就完成了一大半了，现在需要启动IDE，将会弹出激活窗口，选择`Activation code`，在输入框中粘贴激活码，点击`Active`
![激活成功](/img/28544/10.jpg)
什么？你还没有激活码，那么我把激活码放在下方，只需要解压就可以看到各个IDE的激活码啦
{% note success no-icon %}
### 激活码下载链接
清北网盘下载：https://pan.tsinbei.com/s/WofL
蓝奏云下载：https://schlibra.lanzouo.com/ickYP0l8cp8f
123云盘下载：https://www.123pan.com/s/xE9lVv-9JSKd
提取码：2854
{% endnote %}
# 注意事项
{% note info no-icon %}
激活补丁中的脚本只需要执行一次即可，执行后安装了新的IDE可以直接复制配置文件，然后输入激活码就可以用了
激活补丁的目录**千万不要删除**，删除将会导致IDE无法启动
{% endnote %}
# 结尾
这篇文章到这里就结束了，如果你有疑问可以在下方评论区中留言