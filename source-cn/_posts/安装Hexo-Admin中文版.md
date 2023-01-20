---
title: 安装Hexo Admin中文版
author: SCH
tags: [教程, Hexo, Hexo-Admin, 插件, 汉化]
categories: [教程, Hexo, 汉化插件安装]
abbrlink: 50519
date: 2023-01-20 14:46:21
excerpt: Hexo Admin是一个非常方便的Hexo博客管理插件，可以在编写文章的同时预览文章效果，但是官方提供的Hexo Admin是英文版的，很多人可能看不习惯，于是我个人制作了汉化版并提交到了npm中，今天教大家如何安装中文版Hexo Admin
lang: cn
---
{% note info %}
提示
该文章同时提供：[English](/en/article/25391)
{% endnote %}
# 简介
`Hexo Admin`是一个非常方便的`Hexo`博客管理插件，可以在编写文章的同时预览文章效果，但是官方提供的`Hexo Admin`是英文版的，很多人可能看不习惯，于是我个人制作了汉化版并提交到了`npm`中，今天教大家如何安装中文版`Hexo Admin`
# 部署博客
如果你已经部署好了博客那么可以跳过这一步，没有部署博客的根据下方指令进行部署
``` bash
npm install hexo -g
hexo init blog
cd blog
npm install
```
如果没有报错就说明部署成功了
![部署完成](/img/50519/1.jpg)
# 安装Hexo Admin中文版
## 检查是否安装hexo-admin
如果你已经安装了原版再安装中文版将会出现一些问题，所以建议先将原版卸载，先通过下方这个指令判断是否安装了`hexo-admin`
``` bash
npm list hexo-admin
```
如果输出的内容是这样的，就说明安装了`hexo-admin`，那么就需要卸载
![hexo-admin已安装](/img/50519/2.jpg)
如果输出的内容是这样的，就说明没有安装`hexo-admin`，可以跳过卸载步骤
![hexo-admin未安装](/img/50519/3.jpg)
## 卸载原版hexo-admin
``` bash
npm remove hexo-admin
```
这样就卸载完成了
![hexo-admin卸载完成](/img/50519/4.jpg)
## 安装hexo-admin中文版
``` bash
npm install hexo-admin-sch --save
```
# 运行
安装完成后，就可以启动hexo服务器看看效果了
``` bash
hexo s
```
![hexo服务器启动](/img/50519/5.jpg)
启动后访问`IP:端口/admin`就可以看到效果了
![使用体验](/img/50519/6.jpg)
# 注意事项
{% note warning no-icon %}
安装完成后强烈建议设置一个登录验证，在页面中点击`设置>设置身份验证`，并根据提示进行配置，设置登陆验证后会相对安全很多
{% endnote %}
# 结尾
这篇教程到这里就结束了，感谢您耐心阅读，如果有疑问可以在下方评论区留言