# 创建容器并连接VScode

#### 1、创建容器

```bash
docker run --name -it mynginx -d nginx:latest
```

创建容器并自动进入系统

#### 2、列出容器

```
docker ps -a
```

#### 3、开启容器

```
docker start containname
```

#### 4、在运行的容器中执行命令

```
docker exec -i -t containname /bin/bash
```

进入容器伪终端，执行命令对容器进行从操作

#### 5、容器连接vscode

<div align="left">

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

点击左下角图标，连接到正在运行的容器即可使用vscode连接容器编写程序

#### 6、初次进入系统更新、升级软件包

apt updata

\*sudo命令用于在非root用户下执行root命令

apt upgrade

#### 7、安装Ubuntu基本软件包

which name :查看某个软件包是否存在

apt install name:安装软件包

基本软件包：文本编辑器vim
