---
title: Install Hexo Admin Chinese
abbrlink: 25391
date: 2023-01-20 16:07:42
tags: [tutorial, Hexo, Hexo-Admin, plugin, Localization]
categories: [tutorial, Hexo, Localization plugin installation]
excerpt: Hexo Admin is a very convenient Hexo blog management plugin, you can preview the effect of the article while writing the article, but the official Hexo Admin is in English, many people may not be used to it, so I personally made a Chinese version and submitted it to npm, today teach you how to install the Chinese version of Hexo Admin
lang: en
---
{% note info %}
Note
The article is also available at: [简体中文](/cn/article/50519)
{% endnote %}
# Brief introduction
`Hexo Admin` is a very convenient `Hexo` blog management plugin, you can preview the effect of the article while writing the article, but the official `Hexo Admin` is in English, many people may not be used to it, so I personally made a Chinese version and submitted it to `npm`, today teach you how to install the Chinese version of `Hexo Admin`
# Deploy the blog
If you have already deployed a blog, you can skip this step and deploy it according to the instructions below if you have not deployed a blog
``` bash
npm install hexo -g
hexo init blog
cd blog
npm install
```
If no error is reported, the deployment is successful
![Deployment complete](/img/25391/1.jpg)
# Install Hexo Admin Chinese
## Check that hexo-admin is installed
If you have already installed the original version and then installed the Chinese version will have some problems, so it is recommended to uninstall the original version first, and first determine whether `hexo-admin` is installed through the following command
``` bash
npm list hexo-admin
```
If the output is like this, it means that `hexo-admin` is installed and needs to be uninstalled
![hexo-admin is installed](/img/25391/2.jpg)
If the output is like this, it means that `hexo-admin` is not installed and you can skip the uninstall step
![hexo-admin is not installed](/img/25391/3.jpg)
## Uninstall the original hexo-admin
``` bash
npm remove hexo-admin
```
This completes the uninstallation
![The hexo-admin uninstall is complete](/img/25391/4.jpg)
## Install the hexo-admin Chinese
``` bash
npm install hexo-admin-sch --save
```
# Run
After the installation is complete, you can start the HEXO server to see the effect
``` bash
hexo s
```
![The Hexo server starts](/img/25391/5.jpg)
After starting, you can see the effect by accessing `IP:port/admin`
![Usage experience](/img/25391/6.jpg)
# Notes
{% note warning no-icon %}
After installation, it is strongly recommended to set up a login authentication, click `Set > Set Authentication` on the page, and configure it according to the prompts, it will be relatively safe after setting up login verification
{% endnote %}
# End
This tutorial ends here, thank you for your patience in reading, if you have any questions, you can leave a message in the comment area below