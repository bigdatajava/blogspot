---
layout:     post
title:      "ubuntu显示windows盘挂载出错问题解决"
date:       2016-08-15
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - Ubuntu
---

> “Ubuntu-问题解决”



# ubuntu显示windows盘挂载出错问题解决

双系统中，Ubuntu挂载Windows盘出错解决：

```
• sudo ntfsfix /dev/sda8
```

注意：对于windows的系统盘C盘需要关闭：`快速启动项`。不然此命令不会成功




#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接         