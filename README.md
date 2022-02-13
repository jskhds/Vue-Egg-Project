# Vue-Egg-Project

#### 1.简介

**前后端分离的内容管理系统 **

```
1.技术栈：  
  前  端：Vue + Element UI   
  后  端：Egg + Nunjucks  + MySQL + Sequlize  
```



	 2.技术要点：    
	  前端：  
	  ·使用 Element UI 实现页面快速布局  
	  ·使用Vue-router实现路由配置，重写vueRouter.prototype.push避免路由报错  
	  后端：  
	  ·使用Sequlize 操作 MySQL 数据库  
	  ·通过 egg 框架进行统一开发，提升效率  

#### 2.配置

```bash
// server目录 
npm install
npm run dev
// 在client目录
npm install
npm run serve
```

在 server 启动前，还需要通过 mysql 创建数据库并在 server/app/config 目录下的32到41行配置 database 名，用户名以及密码进行连接数据库

```mysql
-- 使用下面语句创建数据库
create database databaseName default character set utf8mb4 collate utf8mb4_unicode_ci;
-- 启动egg项目后，所有数据表会自动创建，然后使用下面语句创建管理员用户。
insert into users (
    username,
    password,
    created_at,
    updated_at
) values (
    "admin",
    "e10adc3949ba59abbe56e057f20f883e",
    "2020-10-01",
    "2020-10-01"
);
-- 管理员用户名为admin，密码使用md5加密，所以初始值设置为‘123456’的加密字符串。
```

#### 3.页面

1. 登录页面

<img src="/image/登录页面.png" style="zoom:33%;" />

2.内容管理页面

<img src="/image/内容管理页面.png" style="zoom:33%;" />

3.首页

<img src="/image/首页.png" style="zoom:33%;" />
