---
title: 用github访问hexo博客
date: 2023-02-03 16:39:33
tags: github,hexo
summary: 昨日种种，皆成今我
categories: hexo 
---

## 1.绑定用户

### 1.1生成信息

cmd或者git输入 

git config --global user.name "name"

git config --global user.email"email"

### 1.2生成ssh key

cmd或者git输入 

ssh-keygen -t rsa -C “email” 

一直回车键，生成后，在C盘找到id_rsa.pub文件打开，复制粘贴到github ssh上

## 2.建立本地仓库

找到你本地博客的根目录

cmd或者git输入  git init 会生成一个隐藏文件夹.git

接着，将所有文件添加到仓库中

执行指令：`git add .` (注意空格后有.)

然后，把文件提交到仓库，双引号内是提交注释。

执行指令：`git commit -m "提交文件"`

## 3.关联github仓库

复制github仓库ssh地址（建立的仓库名一定要是 用户名.github.io）

执行指令：git remote add origin git@github.com:用户名/用户名.github.io.git

## 4.上传本地仓库

打开博客所在文件夹中的_config.yml

![](github1.png)

输入下面三个指令：hexo cl,hexo g,hexo d

ps:hexo d部署到github仓库，如果出现问题，删掉博客根目录下的.deploy_git文件夹，再重复那三个指令即可

## 5.通过github访问博客

输入网址：github用户名.github.io即可访问到上传到github仓库中的博客

ps:github用户名.github.io这个也是你放博客的仓库名









