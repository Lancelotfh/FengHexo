---
title: jQuery 显示精简/完整菜单
date: 2016-11-16 15:50:34
tags:
---
### 显示精简/完整菜单
<b>获取需要隐藏的li</b>
``` bush
var $hideobj = $("ul li:gt(5):not(:last)");
```
<b>根据内容添加高亮</b>  
使用链式结构
``` bush
$("ul li")
.filter(":contains('佳能'),:contains('尼康'),:contains('奥林巴斯')")
.addClass("promoted");
```
<b>用到的jQuery方法</b>
* <code>show();</code>显示隐藏的匹配元素
* <code>css(name,value)</code>给元素设置样式
* <code>text(string);</code>设置所有匹配元素的文本内容
* <code>filter(expr);</code>筛选出与指定表达式匹配的元素集合，其中expr可以是多个选择器的组合。find()会在元素内寻找匹配元素，而filter()是筛选元素。一个是对自己操作，一个是对自身集合元素进行筛选。
* <code>addClass(class);</code>为匹配的元素添加指定的类名