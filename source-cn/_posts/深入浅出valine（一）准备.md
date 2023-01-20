---
title: 深入浅出valine（一）准备
abbrlink: 46933
tags:
  - 教程
  - valine
  - Leancloud
  - 数据分析
categories:
  - - 教程
    - valine
    - 数据分析
  - - 教程
    - Leancloud
    - 数据分析
customNextPre:
  next:
    title: 深入浅出valine（二）配置SDK
    path: https://xcgzs.cn/cn/article/34079/
date: 2023-01-14 16:13:20
excerpt: 有一个非常有名的评论功能，叫做valine，在这篇文章底部使用的评论系统就是valine，他的功能非常强大，可以记录IP，分析设备类型，根据昵称显示对应头像（gravatar）等，这个功能的数据存储在Leancloud中，那么这篇文章将讲解对这个Leancloud平台的数据库操作并操作valine的评论，这篇内容可能比较长，希望你能耐心看完，有问题可以在下方评论区中留言。
lang: cn
---
# 介绍
有一个非常有名的评论功能，叫做`valine`，在这篇文章底部使用的评论系统就是`valine`，他的功能非常强大，可以记录IP，分析设备类型，根据昵称显示对应头像（`gravatar`）等，这个功能的数据存储在`Leancloud`中，那么这篇文章将讲解对这个`Leancloud`平台的数据库操作并操作`valine`的评论，这篇内容可能比较长，希望你能耐心看完，有问题可以在下方评论区中留言。
![评论区截图](/img/46933/1.jpg)
# 登录Leancloud平台
如果你也是`hexo`使用者并且也使用`valine`这个评论系统，那么你一定已经注册了`Leancloud`账号
## 注册账号
如果你还没有注册账号，那么可以点击这个注册链接：[https://console.leancloud.cn/register](https://console.leancloud.cn/register)去注册，注册需要使用`邮箱`和`手机号`，注册完成之后就可以去登录了。
![注册页面](/img/46933/2.jpg)
## 登录账号
点击这个链接：[https://console.leancloud.cn/login](https://console.leancloud.cn/login)去登录，登录之后就会进入控制台。
![登录页面](/img/46933/3.jpg)
{% note info no-icon %}
如果你是第一次使用这个平台，那么登录之后会提示你需要实名认证，这个实名认证一定要完成，不然后续无法继续操作。
{% endnote %}
# 进行相关设置并获取信息
## 创建应用
点击导航栏中的logo，进入控制台，然后点击`创建应用`按钮，输入应用名称，这里以`Hexo`为例。
![创建应用](/img/46933/4.jpg)
创建完成后，就可以看到创建好的`Hexo`应用，然后点击设置按钮
![创建完成](/img/46933/5.jpg)
## 查看应用凭证
选择左侧的`应用凭证`，然后可以看到`AppID`和`AppKey`两个信息，建议先将两个值保存好，后面需要用到，并且确保这两个信息不被泄露，因为有这两个信息就可以直接操作你的数据。
![应用凭证](/img/46933/6.jpg)
# 结尾
到这里，今天的内容就讲完了，感谢您的耐心阅读，下一篇将讲解如何配置SDK，如果这篇文章内容你有疑问可以在评论区留言。
