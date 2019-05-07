---
layout:     post
title:      "zkui-zookeeper图像化界面工具使用教程"
date:       2019-05-07
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
	- zkui
	- zookeeper

---

> “Yeah It's on. ”



# zkui-zookeeper图像化界面工具

## 1. 官方教程

地址：

```
https://github.com/DeemOpen/zkui
```

github上的开发者文档说明很nice，看官网教程基本上都能会的

## 2. 安装使用流程

### 2.1 将项目从github上拉下来，打成能够运行的jar

zkui本质上是一个java写的客户端web工具

```
1. git clone https://github.com/DeemOpen/zkui.git

2. 编译zkui，生成jar
	cd zkui
	mvn clean install	
(生成两个jar包：
zkui-2.0-SNAPSHOT.jar（用不到）和zkui-2.0-SNAPSHOT-jar-with-dependencies.jar，用的是第二个)

3. 将第一步下载的zkui文件夹根目录下的config.cfg复制到，与zkui-2.0-SNAPSHOT-jar-with-dependencies.jar同级目录下

修改配置文件config.cfg：
scmRepo=192.168.3.10:2181,192.168.3.12:2181,192.168.3.13:2181
# 若报KeeperErrorCode = ConnectionLoss for / 错误，增大zkSessionTimeout
zkSessionTimeout=20

4. 启动zkui
java -jar target/zkui-2.0-SNAPSHOT-jar-with-dependencies.jar

5. 浏览器上查看web界面
http://127.0.0.1:9090 
账号-admin
密码-manager
```

### 2.2 备注说明

关于zkui端口等详细配置，都在config.cfg里面配置



#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接

