---
layout: post
title : 	让css书写不在重复
description : 项目开发中处理ie浏览器的兼容性需要各种奇淫技巧，有很多css在项目中总是不断的重复，有时候我们选择了ctrl+c ctrl+v，但是有时不知哪里去ctrl+c，只好谷歌，百度。这是一个多么让人纠结的过程呢。
category : css
tags : [css]
---
{% include JB/setup %}

项目开发中处理ie浏览器的兼容性需要各种奇淫技巧，有很多css在项目中总是不断的重复，有时候我们选择了ctrl+c ctrl+v，但是有时不知哪里去ctrl+c，只好谷歌，百度。这是一个多么让人纠结的过程呢。

我用的是Sublime Text2，强烈推荐使用。自然想到了代码自动补全，输入简短的几个字母就能输出很长的css兼容性代码，那该是多么美好的事情。算是总结自己的代码片段，希望这个可以提高开发的效率。将[SublimeUser.rar](http://huixisheng.github.com/Tools/SublimeUser.rar)解压后的文件放到Sublime Text2的Packages\User\ 目录下。

输入`clearfix`
选择clearfix 回车
	.clearfix:before,.clearfix:after {content:"";display:table}
	.clearfix:after {clear:both;}
	.clearfix {zoom:1; clear:both}

具体的输入规则请看下图：
![css-no-repeat](http://huixisheng.github.com/images/article/css-no-repeat.jpg)

 