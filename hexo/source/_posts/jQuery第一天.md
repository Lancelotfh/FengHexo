---
title: jQuery第一天
date: 2016-11-11 18:27:13
tags:
---
<code>getElementsByTagName("p")</code>获取到的是所有p元素组成的数组  
后代元素、子元素的区别：  
父元素的下一代为子元素  
子元素只是后代元素的其中一代，后代元素还可以包含孙子元素、重孙子元素。  
### 层次选择器
<b>改变`<body>`内所有`<div>`的背景色</b>
``` bush
$("body div").css("background","#bbffaa");
```
<b>改变`<body>`内子`<div>`的背景色</b>
``` bush
$("body > div").css("background","#bbffaa");
```
<b>改变class为one的下一个`<div>`同辈元素的背景色</b>
``` bush
$(".one + div").css("background","#bbffaa");
等价于$(".one").next("div");
```
<b>改变id为two的元素后面所有的`<div>`的背景色</b>
``` bush
$("#two ~ div").css("background","#bbffaa");
等价于$("#two").nextAll("div");
```
*****
<b>过滤选择器</b>  
`:first`选取第1个元素  
`:last`选取最后1个元素  
`:not(selector)`去除与给定选择器相匹配的元素  
`:even`选取索引是偶数的所有元素，索引从0开始  
`:odd`选取索引是奇数的所有元素，索引从0开始  
`:eq(index)`选取索引等于index的元素，索引从0开始  
`:gt(index)`选取索引大于index的元素，索引从0开始  
`:lt(index)`选取索引小于index的元素，索引从0开始  
`:header`选取所有的标题元素  
`:animated`选取当前正在执行动画的所有元素  
`:focus`选取当前获取焦点的元素 
*****
*****
<b>内容过滤选择器</b>
`:contains(text)`选取含有文本内容为"text"的元素    
`:empty`选取不包含子元素或者文本的空元素      
`:has(selector)`选取含有选择器所匹配的元素的元素   
`:parent`选取含有子元素或者文本的元素   
*****
*****
<b>可见性过滤选择器</b>  
`:hidden`选取所有不可见的元素  
`:visible`选取所有可见的元素  
*****
*****
<b>属性滤波器</b>  
`[attribute]`选取拥有此属性的元素  
`[attribute=value]`选取属性的值为value的元素  
`[attribute!=value]`选取属性的值不为value的元素 
`[attribute^=value]`选取属性的值以value开始的元素   
`[attribute$=value]`选取属性的值以value结束的元素   
`[attribute*=value]`选取属性的值含有value元素   
`[attribute|=value]`选取属性的值等于给定字符串或以该字符串为前缀(该字符串后跟一个连字符"-")的元素  
`[attribute~=value]`选取属性用空格分隔的值中包含一个给定值的元素  
`[attribute1][attribute2][attribute3]`用属性选择器合并成一个复合属性选择器，满足多个条件。
****
<b>表单选择器</b>  
`:input`选取所有的`<input>、<textarea>、<select>和<button>`元素  
`:text`选取所有单行文本框  
`:password`选取所有密码框  
`:radio`选取所有单选框  
`:checkbox`选取所有多选框  
`:submit`选取所有提交按钮  
`:image`选取所有图像按钮  
`:reset`选取所有重置按钮  
`:button`选取按钮  
`:file`选取所有上传域  
