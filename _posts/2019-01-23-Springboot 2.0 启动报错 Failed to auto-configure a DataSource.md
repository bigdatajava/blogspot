---
layout:     post
title:      "SpringBoot 2.0 启动报错 Failed to auto-configure a DataSource"
subtitle:   " \"SpringBoot\""
date:       2019-01-12
author:     "刘自超"
header-img: "img/post-bg-2015.jpg"
tags:
    - SpringBoot


---

> “学而不思则**忘** ”



## springboot 2.0 启动报错 Failed to auto-configure a DataSource

### 原因

在pom中添加了mybatis，mysql依赖后，如果application.properties中没有配置数据库连接方面的配置，则会报错：

```
这是因为添加了数据库组件，所以autoconfig会去读取数据源配置，而我新建的项目还没有配置数据源，所以会导致异常出现。
```



```
***************************
APPLICATION FAILED TO START
***************************
Description:
Failed to auto-configure a DataSource: 'spring.datasource.url' is not specified and no embedded datasource could be auto-configured.
Reason: Failed to determine a suitable driver class
Action:
Consider the following:
If you want an embedded database (H2, HSQL or Derby), please put it on the classpath.

If you have database settings to be loaded from a particular profile you may need to activate it (no profiles are currently active).
```

### 解决方法

#### 1.在启动类中加注解

```
在启动类的 @EnableAutoConfiguration 或 @SpringBootApplication 中添加
exclude = {DataSourceAutoConfiguration.class}，排除此类的autoconfig。启动以后就可以正常运行。
```

#### 2.在配置文件application.properties中添加数据源配置，或在pon.xml去除maven依赖





#### 著作权声明

本文首次发布于 [刘自超](https://bigdatajava.github.io/blogspot/)，转载请保留以上链接