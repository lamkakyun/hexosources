---
title: symfony 初学习
date: 2016-06-22 15:30:57
tags:
---

## symfony 安装

``` bash
$ sudo curl -LsS https://symfony.com/installer -o /usr/local/bin/symfony
$ sudo chmod a+x /usr/local/bin/symfony
```
> 如果你觉得慢，请用proxychains

## 新建项目
	symfony new project_name 2.8

## 运行内置服务器
	app/console server:run 0.0.0.0:8080

