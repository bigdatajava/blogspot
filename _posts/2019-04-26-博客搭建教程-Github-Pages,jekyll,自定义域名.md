---
layout:     post
title:      "博客搭建教程-Github Pages,jekyll,自定义域名"
subtitle:   " \"博客搭建\""
date:       2019-04-26
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - 博客搭建


---

> “网上教程太乱了-所以总结了此篇文档 ”

# 基于GitHub Pages，jekyll，自定义域名-博客搭建



## 1. 前提

要有GitHub账号，理解GitHub Pages原理）

安装jekyll（便于后期在本地实时查看博客修改效果）

要有域名（目前国内：对于类似GitHub主机在外国的，域名可以不用备案）

## 2. 将jekyll网站模板放到自己的Github仓库中

**http://jekyllthemes.org/** 此网站提供有可以直接使用的模板，直接下载后解压放到Github仓库里

## 3. 修改配置文件，实现网站特效

关于配置文件各参数介绍，可以去jekyll官网查看（**<https://www.jekyll.com.cn/docs/>**）

下面介绍主要的配置文件：



**_config.yml **主要配置参数说明：

```
# 用于自定义域名
url: https://www.liuwc.xyz/            # 这里写你自己的域名（要是使用GitHub提供的默然域名，可不填写）
baseurl: /         # for example, '/blog' if your blog hosted on 'host/blog'（这里如果写错，会导致后期网站样式加载不出来，因为路径错误）

#其它配置参数，根据不同模板书写
```



**CNAME** 文档内容如下

```
www.liuwc.xyz # 写入自己的域名
```



## 4. 配置GitHub Pages

如图

![https://github.com/bigdatajava/blogspot/raw/master/img/%E9%80%89%E5%8C%BA_001.png](https://github.com/bigdatajava/blogspot/raw/master/img/选区_001.png)



## 5. 访问自己的域名试试呗



#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接



