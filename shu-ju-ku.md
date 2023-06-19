# 数据库

1、容器中下载mysql

2、将原容器打包为镜像

基于创建的一个镜像，创建新的容器&#x20;

docker run --network=host --name mynginx -it  -d nginx:latest

&#x20;\--network=host参数设置主机和容器共用同一个IP



### 连接数据库

容器中运行数据库

```
service mysql start
```

查看数据库状态

```
service mysql status
```

连接到数据库，输入命令和密码

```
mysql -u sqlname -p
```

vscode中设置端口3306，打开可视化工具nacitat即可连接到数据库
