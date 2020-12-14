---
title: "GRPC Install"
date: 2020-12-15T00:55:41+08:00
draft: false
toc: false
images:
tags: 
  - patch
---
### gRPC

#### 安装

1. 下载最新protobuf Release：[protubuf Release](https://github.com/grpc/grpc/releases)

2. 下载对应的zip或tar，然后解压

3. 执行以下，安装 protoc
   
   ```shell
   ./configure
   make
   make check
   make install   
   ```

4. 执行以下，安装对应gRPC生成插件
   
   ```shell
   go get -u google.golang.org/protobuf/cmd/protoc-gen-go
   go get -u google.golang.org/grpc/cmd/protoc-gen-go-grpc
   ```

5. 执行
   
   ```shell
   protoc --go-grpc_out=:. hello.proto
   ```

    验证能否生成 *grpc.pb.go

6. 如果能够生成，则安装完成，若失败，且*<u>proto-gen-go</u>*需要PATH 为加入环境变量，则将GOPATH加入环境变量。

7. 此为加入环境变量后依然无法运行的解决方法.**慎用**！
   
   ```shell
   sudo cp ~/go/bin/protoc-gen-go-grpc /usr/local/go/bin
   sudo cp ~/go/bin/protoc-gen-go /usr/local/go/bin
   ```




