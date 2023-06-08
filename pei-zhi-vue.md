# 配置Vue

#### 1、安装node

apt install npm

npm install -g n

更新到最新版：n latest

查看版本：node -v&#x20;

\*使用该命令可默认下载最新版nodejs

#### 2、第一个Vue页面

App文件是自动创建的第一个页面，点击获得的网址即页面网址，其中import引用了Hello文件和Welcome文件。

Hello文件和Welcome文件是App中的左右两部分子内容（分块设计，再将各个块包含到总页面中）。

Vue页面包含了HTML、JavaScript、CSS三种语言的集合：

\<style>中为css；

\<template>中为html；

\<script>中为JavaScript；

```vue
<style scoped>防止其他语言对气其干扰
```



