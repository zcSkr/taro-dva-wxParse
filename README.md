### 项目简介

为了学习Taro 本人利用官方提供的 知乎小程序demo[github地址](https://github.com/jimczj/taro_zhihu)。
借鉴作者 zuoge85 的 ![整合dva 和 taro 的仿知乎例子](https://github.com/zuoge85/taro-dva)

解决了该例子process.env.TARO_ENV获取不到的问题,并整合了wxParse，实现并测试了了h5端和微信小程序端的富文本显示问题


### 安装
安装 Taro 开发工具 @tarojs/cli

使用 npm 或者 yarn 全局安装

```
npm install -g @tarojs/cli
// 或
yarn global add @tarojs/cli
```
下载代码
```
git clone https://github.com/jimczj/taro_zhihu
# 安装依赖
cd taro_zhihu
npm i
```

### 使用

文件目录如下：
```
├── dist                   编译结果目录
├── config                 配置目录
|   ├── dev.js             开发时配置
|   ├── index.js           默认配置
|   └── prod.js            打包时配置
├── src                    源码目录
|   ├── pages              页面文件目录
|   |   ├── index          index页面目录
|   |   |   ├── index.js   index页面逻辑
|   |   |   └── index.css  index页面样式
|   ├── app.css            项目总通用样式
|   └── app.js             项目入口文件
└── package.json
```
进入项目目录开始开发，可以选择小程序预览模式，或者h5预览模式，若使用微信小程序预览模式，则需要自行下载并打开[微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)，选择预览项目根目录。

**微信小程序编译预览模式:**


```
# npm script
npm run dev:weapp
# 或 仅限全局安装
taro build --type weapp --watch
```

**H5编译预览模式:**
```
# npm script
npm run dev:h5
# 或 仅限全局安装
taro build --type h5 --watch
```
### 页面展示

![](https://user-gold-cdn.xitu.io/2018/6/15/16402e6037be17b7?w=648&h=1142&f=jpeg&s=189658)
![](https://user-gold-cdn.xitu.io/2018/6/15/16402e624c0690f7?w=696&h=1154&f=jpeg&s=223080)
![](https://user-gold-cdn.xitu.io/2018/6/15/16402e640f51f37d?w=656&h=1146&f=jpeg&s=147204)
![](https://user-gold-cdn.xitu.io/2018/6/15/16402e65960247b6?w=656&h=1146&f=jpeg&s=147204)
![](https://user-gold-cdn.xitu.io/2018/6/15/16402e6774a05521?w=656&h=1138&f=jpeg&s=200522)
![](https://user-gold-cdn.xitu.io/2018/6/15/16402e68a9ca8235?w=660&h=1150&f=jpeg&s=80253)


### 开发前注意
若使用 微信小程序预览模式 ，则需下载并使用[微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)添加项目进行预览，此时需要注意微信开发者工具的项目设置
* 需要设置关闭ES6转ES5功能，开启可能报错
* 需要设置关闭上传代码时样式自动补全，开启可能报错
* 需要设置关闭代码压缩上传，开启可能报错


![项目设置](https://user-gold-cdn.xitu.io/2018/6/14/163fe817af30c48e?w=2170&h=1080&f=jpeg&s=198269)
