---
layout: post
title: "Springboot配置SSL"
date: 2020-02-22
description: "starry"
tag: html 
---   

# 
### 1. 申请SSL证书(阿里云)
下载对应的Web容器的证书
![](/images/posts/2020022201.png)
### 2. 工程添加配置(application.yml)
![](/images/posts/2020022202.png)
```
server:
  port: 8889
  ssl:
    key-store: classpath:3423025_www.xxx.cn.pfx
    key-store-password: VWPwlIvL
```
> resources目录下添加下载SSL文件中的.pfx文件，并配置aplication.yml,配置明细如上。

### 3. 服务器配置
![](/images/posts/2020022203.png)
> 只需将SSL下载文件中的.pfx文件，添加到跟jar同级目录即可