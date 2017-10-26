---
title: Hexo多终端同步管理
date: 2017-10-26 15:34:20
categories:
- 前端
- Hexo
tags:
- Hexo
- 前端
- 博客
---

# 操作：
{% codeblock lang:powershell %}
git pull                    #同步更新 
hexo new post "新建文章"     #简写形式 hexo n "新建文章" 
hexo clean                  #清除旧的public文件夹 
hexo generate               #生成静态文件 简写形式 
hexo g hexo deploy          #发布到github上 简写形式 hexo d 
git add .                   #添加更改文件到缓存区 
git commit -m "更新说明"     #提交到本地仓库 
git push                    #推送到远程仓库进行备份
{% endcodeblock %}

-----
