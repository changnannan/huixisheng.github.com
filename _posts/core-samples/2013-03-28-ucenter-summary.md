---
layout: post
title : 个人中心项目总结
description : 这是进公司接手的第一个项目。项目中各种心酸。在此留个纪念，聊表心情。也算是自己对项目的回顾。希望接下来做项目时踩过的坑可以不会再踩。
category : 项目总结
tags : [项目总结]
---
{% include JB/setup %}

这是进公司接手的第一个项目。项目中各种心酸。在此留个纪念，聊表心情。也算是自己对项目的回顾。希望接下来做项目时踩过的坑可以不会再踩。在公司前端小组的例会上也做过分享。

在公司前端小组的例会上也做过分享，总结主要分为6个方面。

	1. 项目背景		
	2. 前端“架构”	
	3. 前端文件“自动化”发布		
	4. 不足之处		
	5. 各种神伤		
	6. 不变应万变		


从接手到现在为止的项目中间大大小小对项目进行了2次调整。最初的项目还是叫sns，公司应该是要打造股民的微博吧。当时是边开发边调整，之前遗留下来很多问题，特别是IE浏览器的兼容性问题。对前端文件的组织结构进行了调整。删除了很多没用的文件，制定了一些前端的规范。当时前端有2人，另一个主要是写js的。我主要负责切图和一点点js。后面由于项目的关系，该项目没有上线。可以说是废弃。重新改版叫[个人中心](http://t.10jqka.com.cn/127750329)。算是一个新的项目重新开始开发，功能跟之前的sns差不多，但是项目的人员变动很大，后台有好几个离职，写js的涛爷也走了，所以js的活全部都到了我手上。先前的sns项目积累了经验，前端的“架构”融入了自己的思想，但是前期的设计应对产品经理各种变来变去的需求还是很吃力的。期间也不停地进行调整，最悲剧的就是项目在ie神器下面的前端性能很差，改了好长的时间，性能稍微有了提升。项目上线后页面经常有调整同时需要发布。每次的发布都需要将js、css、images分别压缩成zip的文件上线到公司的静态资源服务器。每次要这样我都觉得好麻烦。后面用nodejs写了个可以自动压缩zip文件的“自动化”脚本，省去了中间很多没有必要的重复性的劳动，大大地节省时间。


以下零碎的总结算是项目中收获吧：

	* 布局多考虑自适应	
	* html结构考虑可扩展性，应对很多无厘头的需求变化	
	* UI组件提取，复用其他项目	
	* 公用的js代码分离
	* js代码必须添加注释
	* 代码使用OOP原则	
	* 降低代码的耦合性	
	* 提高代码的重用率	
	* 同后台协商一些约定	
	* 项目必须要有规范
	* 该用a标签的地方请用a标签，按需加_blank
	* CSS添加必要的注释
	* 按钮方面多考虑渐进增强
	* 对低版本IE浏览器可以优雅降级
	* OOCSS原则
	* 减少后台的判断，使用负编辑减少多余的右边距和下边距等
	* 异常数据的处理（长英文，长用户名，一连串很长的英文等）
	* 小图标拼Spirit图，必须备份拼好的PSD
	* 测试的图片放在images/test 下，不要上传资源服务器
	* Copy他人结构和css的时候按需copy
	* 先测兼容性再给后台开发
	* 多做总结，多看他人优秀的代码和开源的前端框架
	* 待补充

