---
title: hexo的应用
date: 2023-02-08 13:43:07
categories: hexo 
summary: 只有做傻事的人才是傻子
tags: hexo
---

## 1.切换主题

以下图主题为例,在hexo官网选择自己喜爱的主题点击进去

![](hexoY1.png)

找到该主题的github链接

![](hexoY2.png)

复制地址

![](hexoY3.png)

选择博客根目录下的themes

输入指令：git clone 地址

该目录下就会出现一个主题名的文件夹

![](hexoY5.png)

打开博客根目录_config.yml文件，修改themes: 主题名

![](hexoY4.png)

## 2插入图片

ps:个人觉得这是最方便的

用 npm install hexo-renderer-marked下载图片插件

或者用 npm install https://github.com/CodeFalling/hexo-asset-image --save

安装之后在`config.yaml`中更改配置如下：

![](1.png)

在本地博客目录下的source/_posts里会多出一个跟文章名一样的文件夹

把文章里需要用到的图片放进里面

文章图片引用直接 `![](图片名.图片格式)`