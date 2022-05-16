
# 项目相关
## 简介
开源 vue2
## git地址
https://github.com/ly525/luban-h5.git
## 安装依赖
```zsh
./luban-h5.sh init
```
用yarn安装（issue里有人用npm安装会报错）
## 一键启动
```zsh
./luban-h5.sh start
```
启动完成后访问http://localhost:1337<br>
后台访问地址http://localhost:1337/admin/

## 项目结构
### 前端 /front-end/h5

### 后端 /back-end/h5-api
管理后端使用了nodejs开发，使用了strapi.js框架。<br>
### 数据库用的sqlite

## 支持的业务场景
1.产品宣传、活动简介等宣传页。

## 使用成本、改造成本
1.把项目部署到服务器。需要搞明白前端是怎么运行的，后端是怎么运行的，数据库怎么存储数据的？如何部署？项目克隆完成后文档只给了一键启动的方式，内部运行原理类似黑盒子，需要花时间理解，不然无法获取创建的数据，更不用提如何改造以便贴合现有的业务场景。<br>
2.鲁班H5现在是一个半成品，好多功能没实现，比如表单功能。
3.鲁班H5只打了个壳子，目前支持的组件比较少，如果做比较复杂的功能，需要自己开发一些组件。
# 学习笔记
#### 1.前端项目建议移除 node-sass 依赖，替换为 dart-sass；node-sass是古老的东西了，sass 官方都不用了
```bash
yarn add sass # 安装 dart-sass，dart-sass 现在是 sass 的主要实现。没有 binary 依赖
```
#### 2.文档的代码目录说明里有个解释用jsx的原因
1.作者的个人习惯<br>
2.jsx 语法相对要灵活一些，对变量的复用也会更好，可以避免很多重复计算（阅读vue-easytable 的体会）<br>
3.以后扩充成react版本，大部分代码可以直接复用<br>
#### 3.作者用的UI库 ant-design-vue element-ui