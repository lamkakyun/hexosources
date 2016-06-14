---
title: 我的zsh配置文件
date: 2016-06-14 23:32:19
tags:
---

``` bash
alias edsh='vim ~/.zshrc'
alias srcsh='source ~/.zshrc'
alias c='clear'
alias vimrc='vim ~/.vimrc'
alias eh='sudo vim /etc/hosts'
alias vi='vim'
alias install='sudo apt install'
alias search='apt search'
alias update='sudo apt update'
alias autoremove='sudo apt autoremove'
alias ..='cd ..'
alias ping='ping -c 4'
alias rm='rm -i'
alias cp='cp -i'
alias mv='mv -i'
alias ali_ubs='ssh xxx@127.0.0.1 -p 22'
alias ali_sftp='sftp -oPort=22 jet@127.0.0.1'
alias awsub='ssh -i /home/jet/Downloads/AwsUbs.pem ubuntu@127.0.0.1'
alias sslocalon='nohup sslocal -s 127.0.0.1 -p 8839 -b 0.0.0.0 -l 1080 -k 1111111 -t 600 -m aes-256-cfb 1>/home/jet/.sslocal.log 2>&1 &'

alias edphp='sudo vim /usr/local/php/etc/php.ini'
alias edfpm='sudo vim /usr/local/php/etc/php-fpm.conf'
alias ednginx='sudo vim /usr/local/nginx/conf/jet.conf'

alias nginxon='sudo /usr/local/nginx/sbin/nginx'
alias nginxoff='sudo /usr/local/nginx/sbin/nginx -s stop'
# alias nginxrestart='sudo /usr/local/nginx/sbin/nginx -s reload'
alias nginxrestart='nginxoff && nginxon'

alias fpmon='sudo /usr/local/php/sbin/php-fpm'
alias fpmoff='sudo kill -INT `cat /usr/local/php/var/run/php-fpm.pid`'
alias fpmrestart='sudo kill -USR2 `cat /usr/local/php/var/run/php-fpm.pid`'
alias edfpm='sudo vim /usr/local/php/etc/php-fpm.conf'
alias localdb='mycli -h 127.0.0.1 -uroot -p 123'

alias file='nautilus'

# use taobao mirror instead of default npm sources
alias cnpm="sudo npm --registry=https://registry.npm.taobao.org \
--cache=$HOME/.npm/.cache/cnpm \
--disturl=https://npm.taobao.org/dist \
--userconfig=$HOME/.cnpmrc"

alias uploadblog='hexo clean && hexo generate && hexo deploy'
alias ub='git add -A && git commit -m "default comment" && git push origin master && hexo clean && hexo generate && hexo deploy'
alias runblog='hexo clean && hexo generate && hexo server -i 0.0.0.0 -p 8000'
```
