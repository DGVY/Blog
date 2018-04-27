---
title: Ubuntu-终止由Ctrl+Z挂起在后台的python程序
date: 2018-01-24 14:40:17
tags:
- Ubuntu
- Linux
- python
categories:
- Linux
- Ubuntu
---

## Ctrl+C与Ctrl+Z的区别

* Ctrl+C: 终止当前程序

* Ctrl+Z: 将当前程序挂起到后台，输入`fg`命令可返回上一个被挂起的程序。

## 杀进程

1. 输入`ps -ef | grep python`查看python进程
2. 找到要杀死的进程，输入`kill -9 编号`，结束进程

{% asset_img 运行结果.png %}
