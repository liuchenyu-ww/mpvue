# map-vue进阶学习(个人练习)

> 美团开源小程序框架mpvue进阶学习

## 安装

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

```
## 打包
``` bash
# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

## 项目技术栈
``` bash
# 前端技术栈
mpvue + mpvue-weui

# 数据
easy mock 模拟数据
```

## 进度
``` bash
潮流前线前端静态，模拟数据两条，购物车，更多和我的未完成。
```
# Mpvue-WeUI相关文档 借鉴自 - Mpvue-WeUI作者
##### [原文档地址(Mpvue-WeUI Github地址)](https://github.com/MPComponent/mpvue-weui)
<p align="center" style="text-align: center">
  <a href="https://mpcomponent.github.io/mpvue-weui/">
    <img width="300" src="https://github.com/MPComponent/mpvue-weui/blob/master/docs/logo/logo.png" alt="mpvue-weui logo">
  </a>
  <p align="center" style="text-align: center">
   <a href="https://circleci.com/gh/MPComponent/mpvue-weui" target="_blank"><img src="https://img.shields.io/circleci/project/github/MPComponent/mpvue-weui/dev.svg"></a>
   <a href="https://www.npmjs.com/package/mpvue-weui" target="_blank"><img src="https://img.shields.io/npm/v/mpvue-weui.svg?style=flat" alt="npm"></a>
   <a href="https://www.npmjs.com/package/mpvue-weui" target="_blank"><img src="https://img.shields.io/npm/dt/mpvue-weui.svg?style=flat" alt="npm"></a>
 </p>
</p>

## Mpvue-WeUI

`Mpvue-WeUI`是基于 [mpvue](https://github.com/Meituan-Dianping/mpvue) 的一个小程序 UI 框架， 保留了 [weui](https://weui.io/) 的视觉规范，旨在提高小程序开发体验，同时让用户的使用感知更加统一。

## 文档

[mpvue-weui 文档](https://mpcomponent.github.io/mpvue-weui/)


## 扫码体验

<img src="https://user-images.githubusercontent.com/20694238/47097108-453cae00-d263-11e8-9cd6-5c7c41ad0678.jpg" width="200">


## 安装

``` bash
npm install mpvue-weui --save  # cnpm install mpvue-weui --save

```

## 使用
``` js
/* 全局引入 weui.css (在 `src/main.js` 中引入 weui.css) */
import 'mpvue-weui/src/style/weui.css';
```
``` vue
<template>
  <mp-button type="primary" size="large" btnClass="mb15">默认按钮</mp-button>
</template>
<script>
  import mpButton from 'mpvue-weui/src/button';
  export default {
    components: {
      mpButton,
    },
  }
</script>
```

* 目前由于 `mpvue` 暂不支持全局安装组件，因此只能通过页面单独引入。
* [更多组件](https://mpcomponent.github.io/mpvue-weui/)

## 开发预览

``` bash
1. git clone
git clone git@github.com:MPComponent/mpvue-weui.git

2. 安装依赖
npm install

3. 启动程序
npm run dev

4. 预览
打开微信开发者工具，新建项目，将目录指向 /dist 即可

```

