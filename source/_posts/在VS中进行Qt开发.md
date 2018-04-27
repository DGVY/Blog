---
title: 在VS中进行Qt开发
date: 2017-11-12 23:18:07
tags:
- VS2017
- Qt
categories:
- Qt
---

Qt可以使用QtCreator进行开发，也可以使用VisualStudio。
本人是VS的信仰粉，所以在网上查找了Qt在VS2017中的开发环境搭建，记录在此。

# Qt插件下载

* 插件下载地址：http://download.qt.io/development_releases/vsaddin/
* 下载完成后，直接进行安装

# 注意

* **若使用VS开发Qt，则在编译Qt时，应添加msvc版本。**

# 插件配置

1. 打开Qt5菜单，如图：

    {% asset_img 01_打开Qt5菜单.png %}

2. 选择Qt Options，如下图：

    {% asset_img 02_选择QtOptions.png %}

3. 点击图示的Add按钮，可以添加版本。如下图。在弹出的Add New Qt Version对话框里，填写Qt版本，然后选择Qt路径。

    {% asset_img 03_点击图示的Add按钮.png %}
    

4. 特别提示：VS2013中添加Qt版本时，找的是bin目录下的qmake，所以，应该选择类似"C:\Qt\Qt5.4.1\5.4\msvc2013_64" 这样的。如果不是酱紫的路径，就会报类似下面的错误：

    {% asset_img 04_bin.png %}

5. 配置了正确的Qt Version，点击OK按钮后，效果如下：

    {% asset_img 05_结果如下.png %}
