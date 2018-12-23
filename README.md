# object4d 时空对象存储管理服务

## 快速部署
+ 安装minio
+ docker 运行object4d
```
docker run -v mylocalconfig.json:/GOPATH/bin/config.json light4d/object4d
```

## 底层架构

![](doc/design.png)

<!-- ## 读 -->

<!-- (1991/12/22 23:23:12,114.234235235,34.235123213) -->
<!-- 读时空对象的部分字节 -->
<!-- (1991/12/22 23:23:12,114.234235235,34.235123213)[123:1224235] -->
<!-- ## 写 -->
<!-- 写整个时空对象 -->
<!-- (1991/12/22 23:23:12,114.234235235,34.235123213) -->
<!-- 写时空对象的部分字节 -->
<!-- (1991/12/22 23:23:12,114.234235235,34.235123213)[123:1224235] -->

## 本地搭建开发流程

+ 安装docker
+ 安装postman，导入本项目的doc/postman配置.json
+ 安装谷歌浏览器draw.io插件，打开本项目的doc/design.xml 设计文件

+ 配置好mysql
+ 利用bin/minio.sh 运行minio
+ 把minio的配置，手动写入数据库miniocon表

+ 启动本程序
```
go run app.go bin/config.json
```