---
layout:     post
title:      "MD文档添加Github图床图片"
subtitle:   " \"markdown,Github图床\""
date:       2017-02-25
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - Github图床
---

> “Yeah It's on. ”


### Markdow文档使用GitHub上的图片

#### 1.markdown文档图片插入方式

md文件插入图片是：

```
 ![](图片地址)
 
 PS：[] 里面可以写图片名或者其他备注信息，为的是让图像无法显示时可以看到备注内容
```

#### 2.Github和md文件关联的图片地址是有一定的格式

其格式如下：

```
https://github.com/用户名/repository仓库名/raw/分支名master/图片文件夹名称/`***`.png

PS:按照此格式github会自动解析这个语法，并把图片在md文件中正常显示出来
```



#### 3.总结

复制GitHub里的图片地址后，将blob改为raw就可以了



#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接

