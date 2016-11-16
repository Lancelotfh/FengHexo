---
title: jQuery DOM应用
date: 2016-11-16 18:28:07
tags:
---
### DOM应用
<b>添加元素</b>
``` bush
var $li_1=$("<li title='香蕉'>香蕉</li>");
var $li_2=$("<li title='雪梨'>雪梨</li>");
$("ul").append($li_1)
.append($li_2);
```
<b>其他插入节点方法</b>
`append()`向每个匹配的元素内部追加内容  
`appendTo()`将所有匹配的元素追加到指定的元素中  
`prepend()`向每个匹配的元素内部前置内容  
`prependTo()`将所有匹配的元素前置到指定的元素中  
`after()`再每个匹配的元素之后插入内容  
`insertAfter()`将所有匹配的元素插入到指定元素之后的后面  
******
<b>不仅能将新创建的DOM元素插入到文档中，也能对原有的DOM元素进行移动</b>  
``` bush
var $one_li=$("ul li:eq(1)");
var $two_li=$("ul li:eq(2)");
$two_li.insertBefore($one_li);
```
<b>删除节点</b>
* remove()方法  
``` bush
$("ul li:eq(1)").remove();
```
节点用`remove()`方法删除后，该节点的所有子节点同时被删除。返回值是一个指向已被删除节点的引用，因此以后可以再使用这些元素。  
<b>有选择性的删除节点</b>
``` bush
$(ul li).remove("li[title!=菠萝]");
```
* detach()方法  
不会把匹配的元素从jQuery对象中删除，不同的是，所有的绑定的事件、附加的数据等都会保留下来。  
* empty()方法  
清空节点，清空元素中的所有后代节点。保留元素标签  
<b>复制节点</b>
* clone()方法  
复制节点，新复制的节点不具有任何行为。  
如果需要新复制的节点具有以前节点的行为，使用`clone(true)`  
<b>替换节点</b>  
* replaceWith方法()  
``` bush
$("p").replaceWith("<strong>你最不喜欢的水果是?</strong>");
```
* replaceAll方法()  
``` bush
$("<strong>你最不喜欢的水果是?</strong>").replaceAll("p");
```
<b>包裹节点</b>  
* wrap()方法  
可以在文档中插入额外的结构化标记  
``` bush
$("strong").wrap("<b></b>");//用<b>标签把<strong>元素包裹起来
```
得到的结果：  
``` bush
<b><strong title="选择你最喜欢的水果.">你最喜欢的水果是？</strong></b>
```
* warpInner()方法  
将每一个匹配的元素的子内容（包含文本节点）用其他结构化的标记包裹起来。
