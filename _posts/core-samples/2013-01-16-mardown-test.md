---
layout: post
title : 	mardowm语法简单测试
description : 本文是学习markdown语法做的一些简单测试
category : markdown
tags : [markdown]
---
{% include JB/setup %}

本文是学习markdown语法做的一些简单测试。

一个回车或者大于等于2个空格是一个段落。

# 1个#号可以生成h1
## 2个#号可以生成h2
### 3个#号可以生成h3

下面以此类推到h6

一个Tab可以生成code BlockS

	<html>
	<head>
		<style>
			.clas{ font-size:12px;}
		</style>
	</head>
	<body>
		<div class="page">
		</div>
	</body>
	</html>

在一个段落前面加`>`可以生成一个 blockquotes
>我是用`>`生成的blockquote

数字`1. 2.`生成有序列表

1. 我是有序列表第1个`li`
2. 我是有序列表第2个`li`
3. 我是有序列表第3个`li`

***
##长的有序列表测试##

1. 工作中碰到的困难只是暂时的，不管是怎样的困难，	
2. 项目开始前，必须对项目的架构做可行性、	
3. 不要停下你学习脚步，不管你在现在在做的项目中有没有碰到困难，都要及时地给自己充电，拓宽自己的知识面和提高自己的技能	

字符`*、+、-`生成无序列表

* 我是无序列表第1个`li`
* 我是无序列表第2个`li`
* 我是无序列表第3个`li`

**PS:每个列表的末尾需要4个空格或者tab**

链接和图片生成的方法

	[链接名称](链接)
	![图片名称](链接)

[链接测试](https://github.com/huixisheng/huixisheng.github.com/generated_pages/new)

![测试图片](http://huixisheng.github.com/assets/themes/twitter/bootstrap/img/glyphicons-halflings.png)

我是code`code`,我是**加粗**，我是__斜体__

`***`可以生成hr

***

单纯的链接根式`<链接>`	
<http://huixisheng.github.com/>

特殊的字符需要转义， \_ \*

***


 