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
