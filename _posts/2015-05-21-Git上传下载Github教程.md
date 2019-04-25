---
layout:     post
title:      "我的第一篇博客"
subtitle:   " \"Hello World, Hello Blog\""
date:       2019-04-25 12:00:00
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - 生活
---

> “Yeah It's on. ”


### Git使用教程

## 一、安装Git

官网下载后直接默认安装就可以

## 二、本地使用Git上传项目到GitHub

cd 到上传项目的根目录下，鼠标右键 -> Git Bash Here  进入到Git黑窗口执行下面命令。

1.初始化本地仓库

```
git init
```
2.添加当前工作目录文件到Git，添加管理
```
git add .(记得有个点哦，并且和add之间有空格)
```
3.查看一下当前目录是否 被git管理的文件 以及被git管理并且被修改但是还没有提交的文件，
```
git status（若出现了很多红色文件，那么就需要再次进行2的步骤，git add .直到没有问题。）
```
4.提交文件，把本地仓库暂存区的文件提交到本地仓库。
```
git commit -m "message"  （其中message就是你提交文件时候的备注。以便知道本次提交是什么作用）
```
5.关联远程仓库，其中origin后跟的是，远程仓库的别名。
```
git remote add origin https://github.com/bendan321/nihao.git
```
6.push文件。
```
git push -u origin master。
```

## 三、Idea使用Git上传项目到GitHub

1.电脑已经安装git，Idea需要配置下git基础配置
```
settings -> GitHub -> host:github.com; Login:GitHub用户名; Password:GitHub用户密码 ->test (可以点test测试下是否能够连通)

settings -> Git -> Path to Git executable ->电脑Git安装路径/bin/git.exe ->test（看是否能够连通）
```

2. 类似于命令 git init 
```
   VCS -> import into version control -> Create Git Repository ->选中项目OK
```

3.类似于命令 git add .
```
选中Idea中项目右键  Git->add
```
4.类似于命令 git commit
```
选中Idea中项目右键  Git->commit -> 填写commit信息备注，（注意：次时将用不到的项目文件可以勾选去了，只保留src和pom.xml即可）
```
4.类似于命令 git remote
```
选中Idea中项目右键 Git -> Repository -> remote ->店家“+”,将GitHub上的仓库地址写在此处(例如：https://github.com/bigdatajava/springboot.git)
```

5.类似于命令 git push
```
选中Idea中项目右键 Git ->Repository -> push
```

至此项目成功上传到GitHub

## 四、使用git下载github上的文件

```
git clone GitHub链接地址
```




#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接


