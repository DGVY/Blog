---
title: 搭建OpenGL-freeglut开发环境
date: 2017-11-29 22:24:18
tags:
- OSG
- OpenGL
- freeglut

categories:
- 图形学
- OSG
---

# 下载地址

* http://freeglut.sourceforge.net/index.php#download

# Window10环境

## 编译源码
* 使用CMkae打开`./freeglut-x.x.x`路径下的`CMakeLists.txt`
* 生成VS2017工程
* 打开工程，编译`ALL_BUILD`的Debug版本和Release版本

## 放置编译文件

* 编译完成后，需要使用的文件有三处
    1. 源码文件夹中`./freeglut-x.x.x/include/GL/`路径下的四个头文件
    2. 工程目录中`./bin/`目录下的`freeglut.dll`和`freeglutd.dll`
    3. 工程目录中`./lib/`目录下的`freeglut.lib`和`freeglutd.lib`
* 将其分别移动到OSG环境路径下的相应文件夹中。

## 工程配置

* 在VS工程属性`连接器`->`输入`中添加`freeglutd.lib`或`freeglut.lib`