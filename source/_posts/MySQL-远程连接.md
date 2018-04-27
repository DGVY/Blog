---
title: MySQL-远程连接
date: 2018-01-13 18:51:27
tags:
- MySQL
- 数据库
- ubuntu
categories:
- 数据库
- MySQL
---

# 现象

MySQL默认是只允许本地服务器访问，所以在远程访问MySQL时，会出现连接被拒的情况。

# 解决方案

1. 使用grant语句添加新用户，并设置用户权限
    ```sql
        -- 添加一个用户admin并授权可从任何其它主机发起的访问（通配符％）,访问密码为"something"
        grant all privileges on *.* to admin@"%" identified by 'password' with grant option;
    ```
2. 刷新权限
    ```sql
        flush privileges; 
    ```

3. 查看用户是否添加成功
    ```sql
        select user,host from mysql.user
    ```
    如果有刚才添加的用户名，则证明添加成功。

4. 修改绑定ip的默认配置
    * 注释mysql配置文件中`bind-address`一项或是配置成为某ip（一旦配置了，就只能该ip主机才能访问mysql服务器）， 很多文章介绍这个配置在 `/etc/mysql/my.cnf` 里（可能是mysql版本问题）但是我在该文件下并没有发现有`bind-address`配置，以至于走了很多弯路，后来发现这个配置在 `/etc/mysql/mysql.conf.d/mysql.cnf`里。
    * 修改`bind-address = 127.0.0.1`为`bind-address = 0.0.0.0`