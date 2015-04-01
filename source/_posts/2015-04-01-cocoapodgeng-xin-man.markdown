---
layout: post
title: "Cocoapods更新慢"
date: 2015-04-01 19:19:40 +0800
comments: true
categories: memo
---
`pod install`和`pod update`都卡在`Analyzing dependencies`很久没有响应

解决方案：为了避免以上命令触发cocoapods升级仓库，故添加以下参数来调用，速度大大提升

	pod install --verbose --no-repo-update
	
	或
	
	pod update --verbose --no-repo-update
<br />
	
@end

<br />

<br />

***

您所查看的内容为本博客的 [**Memo**](http://darknighten.github.io/blog/categories/memo/) 分类，更多内容可以浏览其他分类：

[**Note**](http://darknighten.github.io/blog/categories/note/): _主要是分享一些技术笔记,标签< Note >_

[**Memo**](http://darknighten.github.io/blog/categories/memo): _主要记录了开发一些常用的东西，方便备查，标签< Memo >_

[**Insight**](http://darknighten.github.io/blog/categories/insight/): _记录了开发中一些个人感悟，标签< Insight >_
