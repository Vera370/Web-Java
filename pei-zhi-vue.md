# 配置Vue

#### 1、安装node

Ubuntu换源：清华源镜像--使用帮助--Ubuntu--按使用帮助修改文件（vim，注释原有内容，添加新内容）

apt install npm

npm install -g n

更新到最新版：n latest

查看版本：node -v&#x20;

\*使用该命令（下载npm和n）可默认下载最新版nodejs

#### 2、第一个Vue页面

App文件是自动创建的第一个页面，点击获得的网址即页面网址，其中import引用了Hello文件和Welcome文件。

Hello文件和Welcome文件是App中的左右两部分子内容（分块设计，再将各个块包含到总页面中）。

Vue页面包含了HTML、JavaScript、CSS三种语言的集合：

\<style>中为css，描述网页布局；

\<template>中为html，定义网页内容；

\<script>中为JavaScript，控制网页行为；

```vue
<style scoped>防止其他语言对气其干扰
```

#### 3、安装Element Plus

Vue相当于网页的整体框架，使用Element为其添加组件

安装：

```
npm install element-plus --save
```

导入：在main.ts文件中插入以下代码中缺少的部分

```
// main.ts
import { createApp } from 'vue'
import ElementPlus from 'element-plus'
import 'element-plus/dist/index.css'
import App from './App.vue'

const app = createApp(App)

app.use(ElementPlus)
app.mount('#app')
```

至此，便可在App页面中添加组件

#### 4、运行

进入项目所在目录：cd 目录

运行项目：npm run dev

#### 5、latest(3.3.2)版本的vue存在的问题

设计页面默认水平尺垂直居中对齐，使用Element plus的layout布局时左侧存在留白无法消除

改用3.2.47版本

配置文件：\
package.json文件

```
{
  "name": "qhubl",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "dev": "vite --host=0.0.0.0 --port=5173",
    "build": "run-p type-check build-only",
    "preview": "vite preview",
    "build-only": "vite build",
    "type-check": "vue-tsc --noEmit"
  },
  "dependencies": {
    "@element-plus/icons-vue": "^2.1.0",
    "@popperjs/core": "^2.11.7",
    "@types/echarts": "^4.9.17",
    "axios": "^1.4.0",
    "bootstrap": "^5.2.3",
    "echarts": "^5.4.2",
    "element-plus": "^2.3.1",
    "vue": "^3.2.47",
    "vue-echarts": "^6.5.5",
    "vue-router": "^4.1.6"
  },
  "devDependencies": {
    "@types/node": "^18.14.2",
    "@vitejs/plugin-vue": "^4.0.0",
    "@vue/tsconfig": "^0.1.3",
    "npm-run-all": "^4.1.5",
    "typescript": "~4.8.4",
    "vite": "^4.1.4",
    "vue-tsc": "^1.2.0"
  }
}
```

src/main.ts文件

```
import { createApp } from 'vue'
import App from './App.vue'
// import router from './router'

import ElementPlus from 'element-plus'
import 'element-plus/dist/index.css'
// import * as ElementPlusIconsVue from '@element-plus/icons-vue'

import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap"

const app = createApp(App)

// for (const [key, component] of Object.entries(ElementPlusIconsVue)) {
//     app.component(key, component)
//   }
// app.use(router)
app.use(ElementPlus)

app.mount('#app')
```

npm install

npm run dev
