+++
title = 'Hugo stack 主题配合 Github 搭建个人博客'
date = 2024-10-15T09:08:41+08:00
draft = false
categories = ["Hugo"]
tags = ["Hugo"]
+++


hugo 搭建博客记录

—环境搭建
官网：https://gohugo.io/
中文官网：https://www.gohugo.org/
https://gohugo.io/installation/
选择自己操作系统的hugo安装
查看hugo版本：hugo version
有输出代表安装成功

—初始建站
hugo new site [name]
cd theme
下载主题
https://themes.gohugo.io/

—配置文件修改
theme = 'hugo-theme-stack'

—创建文章
hugo new post/first-post.md

—启动hugo
hugo server
访问 localhost:1313


—部署到github
新建仓库 nonoroazoro25.github.io

博客根目录下 输入命令：hugo   生成public文件夹

cd public
git init
git remote add origin https://github.com/Github 用户名/Github 用户名.github.io.git # 将本地目录链接到远程服务器的代码仓库
 【git remote add origin https://github.com/nonoroazoro25/nonoroazoro25.github.io.git】
git add .
git commit -m "[介绍，随便写点什么，比如日期]"
git push -u origin master
【记得修改配置文件：baseURL = 'http://nonoroazoro25.github.io/'】

—每次修改后提交命令
在blog目录下输入 hugo
cd public
git add .
git commit -m “”
git push -u origin master


—hugo相关命令


其他：
安装hugo,go

hugo new site ssha_blog
cd ssha_blog
git init
 # 添加主题作为子模块
git submodule add https://github.com/nonoroazoro25/hugo-theme-stack.git themes/stack
# 初始化子模块
git submodule init
git submodule update
# 复制主题的示例配置
cp themes/stack/exampleSite/config.yaml ./

hugo new about.md
hugo new posts/my-first-post.md
# 启动本地服务器
hugo server -D
# 访问 http://localhost:1313 查看效果







