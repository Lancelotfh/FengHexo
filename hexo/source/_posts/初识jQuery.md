---
title: 初识jQuery
date: 2016-11-10 13:34:20
tags:
---
jQuery 是一个 JavaScript 函数库。
* HTML 元素选取
* HTML 元素操作
* CSS 操作
* HTML 事件函数
* JavaScript 特效和动画
* HTML DOM 遍历和修改
* AJAX
* Utilities
#### 页面中添加jQuery库
``` bush
<head>
<script type="text/javascript" src="jquery.js"></script>
</head>
```
##### CDN地址
<b>标准版</b>
```bush
<script src="//cdn.bootcss.com/jquery/3.1.1/jquery.js"></script>
```
<b>迷你版</b>
``` bush
<script src="//cdn.bootcss.com/jquery/3.1.1/jquery.min.js"></script>
```
### 语法
####基础语法：
<b><code>$(selector).action()</code></b>
* 美元符号定义jQuery
* 选择符(selector)"查询"和"查找"HTML元素
* jQuery的action()执行对元素的操作
例如：
* <code>$(this).hide()</code>
* <code>$("p").hide()</code>  
<b>TIP:</b>jQuery使用的语法是XPath与CSS选择器语法的组合。  
所有的jQuery函数应位于一个document ready函数中:
``` bush
$(document).ready(function(){
//jQuery functions go here
});
```
这样做是为了防止在<b>文档没有完全加载前</b>就运行函数:
* 试图隐藏一个不存在的元素
* 获得未完全加载的图像的大小