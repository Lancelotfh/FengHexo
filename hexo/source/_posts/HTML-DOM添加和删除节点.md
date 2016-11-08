---
title: HTML DOM添加和删除节点
date: 2016-11-08 20:18:01
tags:
---
#### 创建新的HTML元素
先创建该元素（元素节点），然后再向一个已存在的元素追加该元素。
``` bush
<!DOCTYPE html>
<html>
<body>

<div id="div1">
<p id="p1">这是一个段落。</p>
<p id="p2">这是另一个段落。</p>
</div>

<script>
var para=document.createElement("p");
var node=document.createTextNode("这是新段落。");
para.appendChild(node);

var element=document.getElementById("div1");
element.appendChild(para);
</script>

</body>
</html>
```
******
#### 删除已有的HTML元素
必须首先获得该元素的父元素
``` bush
<!DOCTYPE html>
<html>
<body>

<div id="div1">
<p id="p1">这是一个段落。</p>
<p id="p2">这是另一个段落。</p>
</div>

<script>
var parent=document.getElementById("div1");
var child=document.getElementById("p1");
parent.removeChild(child);
</script>

</body>
</html>
```
<b>在不引用父元素的情况下删除某个元素 </b>  
常用解决方案：找到希望删除的子元素，然后使用parentNode属性来找到父元素：
``` bush
var child=document.getElementById("p1");
child.parentNode.removeChild(child);
```
来源：[w3school](www.w3school.com.cn)
