---
title: hexo搭建本地博客
date: 2023-02-03 11:15:51
author: alin
img: https://i.postimg.cc/YqY7MdNb/hexo1.jpg
top: true
cover: true
summary: 一个不欣赏自己的人，是难以快乐的
categories: hexo 
tags: hexo,git,node,博客
keywords: node,hexo,git
---

## 1.准备阶段

### 1.1安装git

windows 

32位链接：https://pan.baidu.com/s/15ksAYNVYyCKBAHH4VuvR4g?pwd=a425 
提取码：a425

64位链接：https://pan.baidu.com/s/1xtjDVoZ_qGv3PY8quDugFA?pwd=3rtd 
提取码：3rtd

或者直接去官网下,需科学上网条件[Git - Downloading Package (git-scm.com)](https://git-scm.com/download/win)

安装过程一直next就行

### 1.2安装nodejs及其配置环境

#### 1.2.1安装

64位链接：https://pan.baidu.com/s/1sJ54VKd5TtwNb6YX2WIpSQ?pwd=i7t2 
提取码：i7t2

下载下来解压即可

打开git或者cmd,检查安装是否成功

![](node1.png)

#### 1.2.2配置环境

配置前准备

在解压缩的文件夹中新建这两个文件夹，我这边是放D盘了，且名字改为了nodejs,以下截图都是这个路径为参考

![](node2.png)

再次打开cmd 输入

npm config set prefix “D:\nodejs\node_global”

npm config set prefix “D:\nodejs\node_cache”//路径填写自己的

**设置环境变量**

打开设置搜索环境变量

![](node3.png)

![](node4.png)

**编辑用户变量**

![](node5.png)

找到尾号为npm的配置，点击编辑，替换成解压缩文件夹中的npm路径

![](node6.png)

**编辑系统变量**

![](node7.png)

![](node8.png)

新建%NODE_PATH%

![](node9.png)

**最后输入npm install express -g**

## 2.安装hexo

//如果遇到问题，报错443的话，删除C盘与.ssh文件夹同目录下的.npmrc文件

ps:一定要有权限，要是实在不会用cmd管理员身份打开 cd 到指定的文件夹开始后面流程即可

1.使用npm安装Hexo，在cmd命令行中输入npm install -g hexo-cli

2.自己可以指定一个文件夹，然后右键点击打开git 输入hexo init

3.完毕后再次输入npm install

## 3.hexo的开启

执行指令：hexo s即可

ps:每次改动后，打开前执行指令:hexo cl,hexo g,最后再执行hexo s



