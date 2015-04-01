---
layout: post
title: "UIControl的几种事件"
date: 2015-04-01 19:24:37 +0800
comments: true
categories: memo
---

1. `UIControlEventTouchDown`

	仅按下的动作。

2. `UIControlEventTouchDownRepeat`

	连续多次按下

	UIControlEventTouchDown -> UIControlEventTouchUpInside -> UIControlEventTouchDown -> UIControlEventTouchDownRepeat -> UIControlEventTouchUpInside -> UIControlEventTouchDown -> UIControlEventTouchDownRepeat -> UIControlEventTouchUpInside

	除第一次按下之外，以后的每次都是一个UIControlEventTouchDown后跟一个UIControlEventTouchDownRepeat事件。

3. `UIControlEventTouchDragInside`

	按下，并在控件范围内拖动。

4. `UIControlEventTouchDragOutside`

	按下，并拖动至控件之外

	UIControlEventTouchDown -> UIControlEventTouchDragInside -> UIControlEventTouchDragExit -> UIControlEventTouchDragOutside

5. `UIControlEventTouchDragEnter`

	拖动时，从控件边界由外到内时的事件

6. `UIControlEventTouchDragExit`

	拖动时，从控件边界由内到外时的事件

7. `UIControlEventTouchUpInside`

	按下，并在控件范围内抬起。

8. `UIControlEventTouchUpOutside`

	按下，拖到控件外，再抬起

	UIControlEventTouchDown -> UIControlEventTouchDragInside *n -> UIControlEventTouchDragExit -> UIControlEventTouchUpOutside -> UIControlEventTouchUpOutside

@end

<br />

<br />

***

您所查看的内容为本博客的 [**Memo**](http://darknighten.github.io/blog/categories/memo/) 分类，更多内容可以浏览其他分类：

[**Note**](http://darknighten.github.io/blog/categories/note/): _主要是分享一些技术笔记,标签< Note >_

[**Memo**](http://darknighten.github.io/blog/categories/memo): _主要记录了开发一些常用的东西，方便备查，标签< Memo >_

[**Insight**](http://darknighten.github.io/blog/categories/insight/): _记录了开发中一些个人感悟，标签< Insight >_
