---
title: 使用hexo和github-pages创建博客
date: 2016-06-14 00:46:38
tags:
---

## install hexo
	npm install hexo-cli -g

## usage
	hexo init
	npm install
	hexo generate
	hexo server

## upload to github

#### update _config.yml file
	deploy:
	  type: git
	  # repository: https://github.com/lamkakyun/lamkakyun.github.io.git
	  repository: git@github.com:lamkakyun/lamkakyun.github.io.git
	  branch: master

#### generate static file
	npm install hexo-deployer-git --save
	hexo clean
	hexo generate
	hexo deploy

## add rss feed and sitemap
	npm install hexo-generator-feed --save
	npm install hexo-generator-sitemap --save

	# update _config.yml
	plugins:
	- hexo-generator-feed
	- hexo-generator-sitemap


## 发现一个问题
> 就是我想在其他PC上写博客，出现麻烦了，因为hexo源码并没有push到github，所以离开了原来的PC，就写不了，所以我将在github另外建立一个repository，将源码放在这个repository里面


## 一直没有评论系统，所以决定，安装一个评论插件，让大家可以相互交流
> 加入多说评论十分简单，这里就不详细写了
