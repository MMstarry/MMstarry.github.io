---
layout: post
title: "Springboot配置SSL"
date: 2017-09-25 
description: "starry"
tag: html 
---   

# Springboot配置SSL
### 1. 申请SSL证书(阿里云)
下载对应的Web容器的证书

### 2. 工程添加配置(application.yml)
```
server:
  port: 8889
  ssl:
    key-store: classpath:3423025_www.xxx.cn.pfx
    key-store-password: VWPwlIvL
```
> resources目录下添加下载SSL文件中的.pfx文件，并配置aplication.yml,配置明细如上。

### 3. 服务器配置
> 只需将SSL下载文件中的.pfx文件，添加到跟jar同级目录即可

至此完成了SpringBoot工程的SSL配置。