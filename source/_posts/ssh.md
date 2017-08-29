---
title: ssh
date: 2017-08-29 13:36:44
tags: 计算机技术
---
#### 1.ssh登录
需要login另一台设备时，再命令行敲几个字母是不是很像黑客
<!-- more -->
> ssh pi@192.168.0.1

ssh 加上设备用户名@ip地址即可

#### 2.免密登录：
如果之前生成果私钥公钥，如配置github时，只需把本机公钥放到server端，
> ~/.ssh/authorized_keys
#### 3.配置别名：
在本机 ~/.ssh/config中添加ssh server 端的信息即可：
>     Host Data-service
>         HostName   120.132.*.*
>         Port       *
>         User       ubuntu
>         IdentityFile /Users/shuailong/.ssh/id_rsa

星号替换为自己要ssh的==server ip==以及端口

