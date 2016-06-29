---
title: 学习apue
date: 2016-06-16 22:05:41
tags:
  - linux
  - unix
---

## Unix高级环境编程是一本关于unix api的书籍
> 我买了这本书也有很久，但是一直高高挂着，因为始终觉得有点枯燥，但是了解unix api对学习C语言有巨大的助益，所以还是应该仔仔细细的讲这本书看一遍

### 使用APUE 库

``` bash
$ wget -c http://www.apuebook.com/src.3e.tar.gz
$ tar zxvf src.3e.tar.gz
$ sudo apt install libbsd-dev -y
$ make

$ sudo cp ./include/apue.h /usr/include/
$ sudo cp ./lib/libapue.a /usr/local/lib/
```

### 编写第一个程序

``` c
#include "apue.h"
#include <dirent.h>

int main(int argc, char **argv) {

    DIR *dp;
    struct dirent *dirp;

    if (argc != 2) {
        err_quit("usage: ls directory_name");
    }

    if ((dp = opendir(argv[1])) == NULL) {
        err_quit("can't not open %s", argv[1]);
    }

    while ((dirp == readdir(dp)) != NULL) {
        printf("%s ----- %s\n", dirp->d_name, dirp->d_type);
    }

    exit(0);
}
```

> 编译报错 undefined reference to `err_quit'

***

#### 解决方案

``` bash
$ sudo cp -f ./lib/error.c /usr/include
```

> 在文件添加一行 include "errro.c"
> 或编辑/usr/include/apue.h 在 #endif	/* _APUE_H */ 前面添加 #include "error.c"
