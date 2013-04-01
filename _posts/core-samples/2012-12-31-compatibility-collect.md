---
layout: post
title : 	项目中浏览器兼容性解决方法收集
description : 整理项目中碰到的浏览器兼容性问题，并提供相关解决办法。希望自己不再被浏览器兼容性问题所苦恼，也希望自己处理浏览器兼容问题时不再重复和头痛...
category : 兼容性
tags : [兼容性, CSS, IE6]
---
{% include JB/setup %}

整理项目中碰到的浏览器兼容性问题，并提供相关解决办法。希望自己不再被浏览器兼容性问题所苦恼，也希望自己处理浏览器兼容问题时不再重复和头痛。

###1、 个人中心首页小发布框点击弹出发布框，在ie6下导致下面的Tabs上移，就是出现错位，点击旁边的Tabs切换就正常

问题回顾：

![IE下JS交互产生的定位重叠](http://huixisheng.github.com/images/article/ie6-jsclick-bug.jpg)

该问题出现当时完全想不到是为何，难道js交互也会导致CSS出现问题？为何切换了却是正常的。这个问题困恼了我好久。后来在张鑫旭大牛的博客看到一文[利用重绘解决IE下JS交互产生的定位重叠等棘手bug](http://www.zhangxinxu.com/wordpress/2013/01/js-paint-ie6-relative-ie8-inline-block-bug-fix/),受了启发，终于改了这个bug。

###2、 IE6 inline-block使line-height失效

该问题很常见，解决的办法也很多。主要出现在左边是icon的图片，右边是文字，文字图片垂直居中。ie6解决办法：icon的margin-top  margin-bottom取（外侧容器的高度-icon的高度）/2  其他浏览器：`vertical-align:middle; margin-top:-3px` 


###3、 IE6 z-index失效

问题回顾：

![IE6 z-index失效](http://huixisheng.github.com/images/article/ie67-z-index-disable.png)

出现了好几次，印象最深的是做网站导航的统一的时候。消息的下拉框被设置了pr的下面的元素挡住了。解决办法和原因请参考[IE6下z-index犯癫不起作用bug的初步研究](http://www.zhangxinxu.com/wordpress/2009/12/ie6%E4%B8%8Bz-index%E7%8A%AF%E7%99%AB%E4%B8%8D%E8%B5%B7%E4%BD%9C%E7%94%A8bug%E7%9A%84%E5%88%9D%E6%AD%A5%E7%A0%94%E7%A9%B6/)

###4、 IE6下弹出框被Select穿透

解决办法：1、弹出框添加iframe 2、select用js模拟

###5、 IE6不支持最大高度最小高度最大宽度最小宽度

解决办法：1、CSS表达式 2、js控制

##继续更新中
