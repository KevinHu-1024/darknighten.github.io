---
layout: post
title: "用Octpress在Github写博客的几个步骤"
date: 2015-04-01 06:43:38 +0800
comments: true
categories: Memo
---


经过长时间的爬坑，现将自己的总结与网上搜索到的资料精简整合一下

__1、__建立新文章

	rake new_post["这里是文章名"]

	

__2、__文章生成位置在 `octopress/source/_posts` 下，使用Mou编辑保存（或任意一款支持Markdown编辑的软件），这个过程中建议开启

	rake watch
	
	

__3、__编辑完成后 `control+c` 停止 rake watch ，运行

	rake generate
	rake preview
	
	

在 <http://localhost:4000> 可见预览页面。

__4、__没有问题的话，运行

	rake deploy
	
	

程序会将生成好的静态页面上传至github的默认分支（默认为master分支）下，此时可以在浏览器输入你的网址进行浏览了。

如果要将source文件夹也同步进去，则接下来运行

	git check source
	git add -A (这里常用 git add .)
	git commit -m "写更新信息"
	git push origin source
	
	

@end





***

您所查看的内容为本博客的 [**Memo**](http://darknighten.github.io/blog/categories/Memo/) 分类，更多内容可以浏览其他分类：

[**Note**](http://darknighten.github.io/blog/categories/note/): _主要是分享一些技术笔记,标签< Note >_

[**Memo**](http://darknighten.github.io/blog/categories/memo): _主要记录了开发一些常用的东西，方便备查，标签< Memo >_

[**Insight**](http://darknighten.github.io/blog/categories/insight/): _记录了开发中一些个人感悟，标签< Insight >_
