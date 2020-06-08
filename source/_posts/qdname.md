---
title: qdname
date: 2020-06-08 18:45:16
tags:
---
使用 Hexo+GitHub 搭建个人免费博客教程

本文就详细介绍下如何使用 Hexo + GitHub 搭建免费个人博客网站的教程

简介：GitHub Pages 和 Hexo & 原理

1、环境搭建

Hexo 基于 Node.js，搭建过程中还需要使用 npm（Node.js 已带） 和 git，因此先搭建本地操作环境，安装 Node.js 和 Git。

1.1node

Node.js：https://nodejs.org/zh-cn
1.2git

Git：https://git-scm.com/downloads
1.3安装git前建议先安装brew，终端执行命令：

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
1.4 安装git，终端执行命令：

brew install git
1.5安装完成后检查结果

cmd进入并打开，一次执行node -v、npm -v 和 git --version
展示版本号，说明安装成功

2、Github账户创建并创建仓库

2.1创建github账户链接

https://github.com/
完成注册后，并通过邮箱验证

2.2设置用户名和邮箱

git config --global user.name "GitHub 用户名"
git config --global user.email "GitHub 邮箱"
2.3创建ssh密钥：

ssh-keygen -t rsa -C "GitHub 邮箱"
2.4添加密钥：

1、进入 [C:\Users\用户名.ssh]目录（要勾选显示“隐藏的项目”），用记事本打开公钥 id_rsa.pub *文件并复制里面的内容。
2、 登陆 GitHub ，进入 Settings 页面，选择左边栏的 SSH and GPG keys，点击 New SSH key。
3、Title 随便取个名字，粘贴复制的 id_rsa.pub 内容到 Key 中，点击 Add SSH key 完成添加
4、验证链接：打开 Git Bash，输入 ssh -T git@github.com 出现 “Are you sure……”，输入 yes 回车确认 显示“Hi xxx! You've successfully……” 即连接成功