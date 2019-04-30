---
layout:     post
title:      "使用npm命令安装库时,遇到 npm ERR! fetch failed https://registry.npmjs.org/xxx的问题"
date:       2016-11-23
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - npm


---

> “学而不思则**忘** ”



# 使用npm命令安装库时,遇到 npm ERR! fetch failed https://registry.npmjs.org/xxx的问题

## 最好的解决方式–使用淘宝源

镜像使用方法（三种办法任意一种都能解决问题，建议使用第三种，将配置写死，下次用的时候配置还在）:

1.通过config命令

```
$ npm config set registry https://registry.npm.taobao.org 
$ npm info underscore （如果上面配置正确这个命令会有字符串response）12
```

2.命令行指定

```
$ npm --registry https://registry.npm.taobao.org info underscore 1
```

3.编辑 ~/.npmrc 加入下面内容

```
$ registry = https://registry.npm.taobao.org1
```

搜索镜像: [https://npm.taobao.org](https://npm.taobao.org/)

建立或使用镜像,参考: <https://github.com/cnpm/cnpmjs.org>



#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接

