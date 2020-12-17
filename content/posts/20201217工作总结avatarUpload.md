---
title: "20201217工作总结avatarUpload"
date: 2020-12-17T21:22:03+08:00
draft: false
toc: false
images:
tags: 
  - 工作所得
---
#### 2020.17.17

##### 关键词

gin、xorm、gRPC、华为OBS

#### gin

ctx.FormFIle() 直接获取到文件流的柄

ctx.GetHeader（header 字段名）

ctx.Query(query Json)

#### xorm

xorm使用go中Struct内部的字段来和数据库进行同步，不需要写麻烦的Sql语句

gRPC

protobuffe语言的用法

1. message

2. enum

3. reverse 

```shell
protoc --go-grpc_out=. *.proto
```
#### 华为OBS
匿名访问方式 https://桶名.obs服务器名/文件名

