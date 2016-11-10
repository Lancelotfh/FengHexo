---
title: jQuery 选择器
date: 2016-11-10 14:46:25
tags:
---
#### jQuery元素选择器
jQuery使用<b>CSS</b>选择器来选取HTML元素。
例如:  
* <code>$("p")选取`<p>`元素。</code>
* <code>$("p.intro")选取所有class="intro"的`<p>`元素。</code>
* <code>$("p#demo")选取所有id="demo"的`<p>`元素。</code>
#### jQuery属性选择器
jQuery使用XPath表达式来选择带有给定属性的元素。
* <code>$("[href]")选取所有带有href属性的元素。</code>
* <code>$("[href='#']")选取所有带有href值等于"#"的元素。</code>
* <code>$("[href!='#']")选取所有带有href值不等于"#"的元素。</code>
* <code>$("[href&='.jpg']")选取所有href值以".jpg"结尾的元素。</code>
#### jQuery CSS选择器
jQuery CSS选择器可用于改变HTML元素的CSS属性。  
下面的例子把所有p元素的背景颜色更改为红色：  
<b>实例</b>  
``` bush
$("p").css("background-color=","red");
```