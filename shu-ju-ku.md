# 数据库

1、容器中下载mysql

2、将原容器打包为镜像

基于创建的一个镜像，创建新的容器&#x20;

docker run --network=host --name mynginx -it  -d nginx:latest

&#x20;\--network=host参数设置主机和容器共用同一个IP
