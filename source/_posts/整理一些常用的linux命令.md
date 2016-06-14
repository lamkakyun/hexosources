---
title: 整理一些常用的linux命令
date: 2016-06-14 23:57:48
tags:
  - linux
categories: linux
---

## 因为打算使用ubuntu作为自己以后一直使用的操作系统
##### 因而一些对一些常用的linux命令，进行记录

### convert 图像处理命令
    sudo apt install ImageMagick
    convert avatar.jpg avatar.png
    convert avatar.jpg -resize 80 avatar.gif
### last 显示近期用户或终端的登录情况
### du -lh 查看文件大小
### file 查看文件类型
    file avatar.jpg
### stat 查看文件的状态 (如权限)
### iwconfig 查看wifi信息
    iwconfig # 查看哪一个接口支持无线连接
    sudo ip link set wlan0 up|down # 开启/关闭 网卡服务
    sudo iw dev wlan0 scan | less # 扫描无线网络 （可以加上grep ssid）
    sudo iw dev wlan0 connect [网络 SSID] # 连接的网络是没有加密的
    sudo iw dev wlan0 connect [网络 SSID] key 0:[WEP 密钥]
### free 查看内存和交换区使用量
### swapon -s 查看所有交换分区  
### fdisk -l  查看所有分区
### df -h 查看已挂载的硬盘信息
