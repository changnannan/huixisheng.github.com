---
layout: post
title : 	项目中碰到的问题随笔
description : 很随便的记录项目中碰到的疑难杂症
category : 项目总结
tags : [项目总结, 整理]
---
{% include JB/setup %}

###ajax服务器端接收数据时"+"会丢失
jQuery的ajax通过get的方法传参数，如果参数含有`+、&`等，会导致内容丢失。		
"+"号：JavaScript解析为字符串连接符，所以服务器端接收数据时"+"会丢失。		
"&"：JavaScript解析为变量连接符，所以服务器端接收数据时&符号以后的数据都会丢失。	
解决办法：ajax的data改为Object。以下是网上的方法：在传到服务端之前先将参数中的"+"和"&"符号都编码一下
	function filter(str){
	    str = str.replace(/\+/g,"%2B");
	    str = str.replace(/\&/g,"%26");
	    return str;
	}


###JavaScript编码转换
常用的函数:使用 unescape() 对 escape() 编码的字符串进行解码、decodeURIComponent() 函数可对 encodeURIComponent() 函数编码的 URI 进行解码、decodeURI() 函数可对 encodeURI() 函数编码过的URI 进行解码。 encodeURIComponent会对/也进行十六进制转义，而encodeURI不会。

escape的一个应用就是将中文转成unicode编码
	escape("悔惜晟").replace(/%/g, '\\')


###CSS强制英文、中文换行与不换行
white-space:nowrap; 强制不换行，都起作用	
white-space:pre-wrap; 只对中文起作用，强制换行	
项目中用来打散成串的因为

###jQuery ajaxFileUpload.js 插件 ie9 下bug
    if(window.ActiveXObject) {
        if(jQuery.browser.version=="9.0"){
            var io = document.createElement('iframe');
            io.id = frameId;
            io.name = frameId;
        }else if(jQuery.browser.version=="6.0" || jQuery.browser.version=="7.0" || 
        		jQuery.browser.version=="8.0"){
             var io = document.createElement('<iframe id="' + frameId + '" name="' + frameId + '" />');
             if(typeof uri== 'boolean'){
                 io.src = 'javascript:false';
             }
             else if(typeof uri== 'string'){
                 io.src = uri;
             }
        }
    }

todo.. 整理

### 参考网址
[CSS强制英文、中文换行与不换行](http://zmingcx.com/css-compulsory-english-chinese-and-non-wrapping-line.html#)

 