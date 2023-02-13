---
title: github-hexo搭建博客
date: 2023-02-11 10:35:49
summary: 昨日种种，皆成今我
mathjax: true
top: true
cover: true
categories: 博客
tags: 
- github
- hexo
- node
- git
---

## 1.准备

### 1.1安装nodejs及配置其环境

windows 64位链接：https://pan.baidu.com/s/1sJ54VKd5TtwNb6YX2WIpSQ?pwd=i7t2 
提取码：i7t2

下载后选择盘解压缩即可

或者去官网下载https://nodejs.org/en/download/

![](1.1.1.png)

在解压缩的文件夹中新建这两个文件夹，我这边是放D盘了，且名字改为了nodejs,以下截图都是这个路径为参考

![](1.1.2.png)

打开cmd 输入指令：

`npm config set prefix “D:\nodejs\node_global”`

`npm config set prefix “D:\nodejs\node_cache”`//路径填写自己的

搜索编辑系统环境变量

![](1.1.3.png)

系统属性页面点击环境变量

![](1.1.4.png)

**用户变量**，选中Path点击编辑

![](1.1.5.png)

如果有node配置就改成下图，没有就新建

![](1.1.6.png)

**系统变量**，新建NODE_PATH变量

![](1.1.9.png)

选中Path点击编辑

![](1.1.7.png)

新建%NODE_PATH%

![](1.1.8.png)

最后输入`npm install express -g`

### 1.2安装git

windows 

32位链接：https://pan.baidu.com/s/15ksAYNVYyCKBAHH4VuvR4g?pwd=a425 
提取码：a425

64位链接：https://pan.baidu.com/s/1xtjDVoZ_qGv3PY8quDugFA?pwd=3rtd 
提取码：3rtd

或者直接去官网下,需科学上网条件[Git - Downloading Package (git-scm.com)](https://git-scm.com/download/win)

安装过程一直next就行

## 2.安装hexo

//如果遇到问题，报错443的话，删除C盘与.ssh文件夹同目录下的.npmrc文件

ps:一定要有权限，要是实在不会用cmd管理员身份打开 cd 到指定的文件夹开始后面流程即可

1.使用npm安装Hexo，在cmd命令行中输入指令

`npm install -g hexo-cli`

2.自己可以新建一个文件夹，然后右键点击打开git 输入指令

`hexo init`

3.完毕后再次输入指令

`npm install`

4.hexo 3连，即

`hexo cl`  清除了你之前生成的东西

`hexo g`  生成静态文章

`hexo d`  部署文章到github

在浏览器中输入 `localhost:4000` 就可以看到生成的博客页面了

## 3.绑定用户

### 3.1生成信息

注：name是你github用户名，email是你邮箱

git输入指令：

`git config --global user.name "name"`

`git config --global user.email"email"`

可以用以下两条，检查一下你有没有输对

`git config user.name`

`git config user.email`

### 3.2建立github仓库

创建一个和你用户名相同的仓库，后面加.github.io

我的用户名是darkchirps

所以仓库名是darkchirps.github.io

### 3.3生成ssh key

git输入指令：

`ssh-keygen -t rsa -C “email”` 

一直回车键，生成后，在C盘找到id_rsa.pub文件打开复制

打开git设置

![](3.2.1.png)

粘贴到github ssh上

![](3.2.2.png)

在 gitbash 中输入以下指令，查看是否 SSH 是否已绑定成功

`ssh -T git@github.com`

## 4.将hexo部署到github

找到你本地博客的根目录,打开_config.yml,找到deploy，修改

![](4.1.1.png)

修改完成保存

注：repo: git@github.com:用户名/用户名.github.io.git

安装deploy-git，输入指令：

`npm install hexo-deployer-git --save`

然后进行部署

`hexo cl`  清除了你之前生成的东西

`hexo g`  生成静态文章

`hexo d`  部署文章到github

注意：hexo d部署到github仓库，如果出现问题，删掉博客根目录下的.deploy_git文件夹，再重复那三个指令即可

## 5.通过github访问博客

输入：github用户名.github.io 即可访问到上传到github仓库中的博客