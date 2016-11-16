---
title: HTML DOM学习
date: 2016-11-08 15:04:14
tags:
---
#### 查找HTML元素
##### 通过id查找HTML元素
``` bash
var x=document.getElementById("intro");
```
#### 通过标签名查找HTML元素
查找id="main"的元素，然后查找"main"中的所有`<p>`元素：
``` bash
var x=docoment.getElementById("main");
var y=x.getElementByTagName("p");
```
<b>根据类名查找HTML元素在IE5,6,7,8中无效</b>
******
#### 改变HTML内容
通过使用innerHTML属性
``` bash
document.getElementById("p1").innerHTML="New texe";
```
#### 改变HTML元素的属性
``` bush
document.getElementById("Image").src="landscape.jpg";
```
#### 改变HTML样式
``` bush
document.getElementById("p2").style.color="blue";
```
#### HTML事件属性
* onclick   单击响应
* onload    用户进入页面时触发
* onunload  用户离开页面时触发
* onchange  常结合对输入字段的验证来使用。
``` bush
<input type="text" id="fname" onchange="upperCase()">
```
* onmouseover 鼠标移至HTML元素上方
* onmouseout  鼠标移出HTML元素
* onmousedown 鼠标在HTML元素上按下
* onmouseup   鼠标在HTML元素上释放
* onfocus     输入字段获得焦点时，改变其背景色