---
title: 功能模块设计
description: ''
position: 2111
category: '经验篇-项目'
---

实现 `注册、登录、注销、密码找回` 的需求。

用户可以通过手机号进行登录和密码找回。

## 系统结构图

示例：

![Image](/experience/project/sys.png)

## 功能模块

### 注册

流程图，示例：

![Image](/experience/project/flow.png)

涉及参数：

* 用户名
* 密码
* 手机号
* 短信验证码

约束条件：

* 短信验证码发送频率限制 90s
* 注册频率限制每30分钟只能注册 1次

（示例，根据实际需求和业务进行约束）

### 登录

涉及参数：

* 用户名或手机号
* 密码

约束条件：

* 30分钟内 连续出错 3次 限制登录

### 找回密码

涉及参数：

* 手机号
* 短信验证码
* 新密码
