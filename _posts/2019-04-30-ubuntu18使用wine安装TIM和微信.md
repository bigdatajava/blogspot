---
layout:     post
title:      "ubuntu18使用wine安装TIM和微信"
date:       2016-08-15
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - Ubuntu
---

> “Ubuntu-问题解决”



# ubuntu18使用wine安装TIM和微信

```
理解懂以下知识和流程：
1，wine：相当于容器（提供了软件安装运行的特定环境），可以利用wine容器安装运行软件

2，deepin-wine-ubuntu：是wine的Ubuntu深度开发版
	（项目开源在https://github.com/wszqkzqk/deepin-wine-ubuntu）

3，安装好wine后，下载安装deepin（Ubuntu属于deepin系统）下发布的最新版容器安装包（例如TIM，微信等）
```



#### 1. 下载安装deepin-wine-ubuntu

deepin-wine-ubuntu（可登陆项目官网查看详细教程）`https://github.com/wszqkzqk/deepin-wine-ubuntu` 

下载安装：

```
1，git clone https://gitee.com/wszqkzqk/deepin-wine-for-ubuntu.git

2，解压后切换到解压文件目录，在终端中运行（授予可执行权限后）：./install.sh

KDE或其他按照普通安装方式安装后运行出现X错误的桌面环境执行 ./KDE-install.sh
```

至此，wine容器安装完成，下一步安装在容器中需要运行的软件

#### 2. 下载安装所需软件（TIM,微信&）

登陆 https://github.com/wszqkzqk/deepin-wine-ubuntu 这个网址里面附有所需要的软件，下载后：在终端下使用dpkg -i安装容器，否则容易误报依赖错误

```
dpkg -i TIM/微信等软件
```

完&


#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接         