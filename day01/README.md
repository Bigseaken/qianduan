### HTML基础
先了解html的基本结构
```
<!DOCTYPE html>
<html >
<head>
<meta charset="UTF-8"> <!-- 直接使用charset指定字符集 -->
<title>指定页面的标题</title>
</head>
<body>
布局内容
</body>
</html>
```
清楚html的结构后，我们来了解html的标签
<body> 标签

- 块级标签和内联标签

 - 块级标签：`<p><h1><table><ol><ul><form><div>`
 - 内联标签：`<a><input><img><textarea><span>`

#### block（块）元素的特点:

1. 总是在新行上开始；
2. 高度，行高以及外边距和内边距都可控制；
3. 宽度缺省是它的容器的100%，除非设定一个宽度。
4.  它可以容纳内联元素和其他块元素

####  inline（内联、行内）元素的特点:

1. 和其他元素都在一行上；
2. 高，行高及外边距和内边距不可改变；
3. 宽度就是它的文字或图片的宽度，不可改变
4. 内联元素只能容纳文本或者其他内联元素

####  对行内元素，需要注意如下

1. 设置宽度width 无效。
2. 设置高度height 无效，可以通过line-height来设置。
3. 设置margin 只有左右margin有效，上下无效。
4. 设置padding 只有左右padding有效，上下则无效。注意元素范围是增大了，但是对元素周围的内容是没影响的。

---
- 基本标签
```
<h1>~<h6> 标题标签.
<p>: 段落标签. 包裹的内容被换行.并且也上下内容之间有一行空白.
style="text-indent: 2em"可以设置样式为首行缩进两个字符。
<b> <strong>: 加粗标签.
<strike>: 为文字加上一条中线.
<u>: 文字下方加下划线.
<em> <i>: 文字变成斜体.
<sup>和<sub>: 上角标 和 下角标.
<br>:换行.
<hr>:水平线.
<div>
<span>
```
###块级标签。块级标签常用于布局，行级标签常用语显示内容。
###div的大小是由内容来决定的，默认情况下，高度由内容的高度决定，宽度适应屏幕。
###可以容纳其他元素，是一个容器。

----

- 特殊符号
```
> >
< <
空格
" 引号
© 版权符号
特殊符号 符号码
" &quot ;
& &amp ;
< &lt ;
> &gt ;
© &copy ;
® &reg ;
± &plusmn ;
× &times ;
§ &sect ;
¢ &cent ;
¥ &yen ;
· &middot ;
&euro ;
£ &pound ;
™ &trade ;
```
---

- `<a>` 超链接标签(锚标签)

###重要属性有三个：href、target、name
- href 超链接地址：可以是Web上任意资源，包括图片，网页，样式，脚本文件等。href="#"时，表示被链接页面就是当前页面。
- target 文档打开时要显示的目标位置，属性值一般有：_blank（新窗口中打开）、_self（默认，在超链接所在的容器中打开）、_parent（在超链接的父容器中打开）、_top（整个容器中打开）、name（框架名称）。

- name 锚记名称。作用：跳转到文档的某个地方。返回首页。
```
# 跳转网页
<a href="http://www.w3school.com.cn/tags/tag_a.asp" target="_blank">w3school a标签教学</a>
```
---

- `<img>` 图形标签
行级标签，用来显示图片。
重要属性有：src、title、alt、width、height、align。
 - src 图片地址。
 - title 鼠标悬浮在图片上的文字。
 - alt 图片找不到时要替换的文字。如果图片资源使用的是外网资源，则不会显示要替换的文字。如果使用的是本网站的资源（相对路径给出），则找不到图片时会显示替换的文字，并保留图片设置的宽高结构。
 - align 图片周围文字的垂直对齐情况。常用的属性值有：top（与图片的顶部对齐）、middle（与图片的中部对齐）、bottom（默认，与图片的底部对齐）。
 - width 图片的宽
 - height 图片的高 (宽高两个属性只用一个会自动等比缩放.)
```
<img src="http://images.cnblogs.com/cnblogs_com/suoning/845162/o_ns.png" alt="图片加载失败。。。" title="The knife girl, kiss"/>
```
---
- 列表标签

`<ul>` :无序列表标签
`<li>`:列表中的每一项.
`<ol>` :有序列表标签
`<li>`:列表中的每一项.
`<li>`主要的属性有：type、value两个:

 - type指明项目的类型，属性值有：A，a，I，i，1，disc（实心圆），square（实心正方形），circle（空心圆）。
 - value表示序号值从几开始。
`<dl>` 定义列表
`<dt>` 列表标题
`<dd>` 列表项
```
<ur>
<li type="circle">A</li>
<li type="1">B</li>
<li type="1">C</li>
</ur>
<ol>
<li value="3">3</li>
<li>4</li>
</ol>
<dl>
<dt><i>标题</i></dt>
<dd>第一项</dd>
<dd>第二项</dd>
<dd>第三项</dd>
</dl>
```
- `<table>` 表格标签
```
<table border="1">
<thead>
<tr>
<th>序号</th>
<th>姓名</th>
</tr>
</thead>
<tbody>
<tr>
<th>1.</th>
<td>nick</td>
</tr>
<tr>
<th>2.</th>
<td>jenny</td>
</tr>
</tbody>
</table>
```
`<table>` 表格标签

- border:（表格边框）
- align（水平对齐方式）
- bgcolor（背景颜色）
- cellpadding（内边距，单元格与内容之间的距离）
- cellspacing（外边距，单元格的间距，设置为0时，表格变为实线表格）
- width（表格的宽度，可以用%或者像素，最好通过css来设置长宽）
`<caption>` 表格的标题
`<tr>` 表格的数据行，table row
`<th>` 表格的表头名称，与<td>不同在于文字采用加粗居中的形式显示，table head cell
`<td>` 单元格，用来显示表格内容，table data cell
`<thead>` 表格头部，使结构更加分明
`<tbody>` 表格主体部分，使结构更加分明
rowspan 单元格竖跨多少行，作用在th或者td上
colspan 单元格横跨多少列（即合并单元格），作用在th或者td上
`<table>`
```
<caption>xxxxxxxxxx</caption>

<thead>

<tr>

<th>序号</th>

<th>姓名</th>

<th>年龄</th>

<th>女神</th>

</tr>

</thead>

<tbody>

<tr>

<th>1.</th>

<td>nick</td>

<td>18</td>

<td>可可西</td>

</tr>

<tr>

<th>2.</th>

<td>jenny</td>

<td>21</td>

<td>nick!!!</td>

</tr>

</tbody>

</table>
```
- `<form>`表单标签

#### 表单属性

HTML 表单用于接收不同类型的用户输入，用户提交表单时向服务器传输数据，从而实现用户与Web服务器的交互。表单标签, 要提交的所有内容都应该在该标签中。
属性：action、method、enctype

 - action 表单要提交的地址，用于处理表单的内容（一般是提交字典到后台的一个接口，这个接口是java写成的，提交到这个接口后后台就知道如何处理这些数据了）。

  - method 提交的方法，默认是get方式提交。

  - get: 1.提交的键值对.放在地址栏中url后面. 2.安全性相对较差. 3.对提交内容的长度有限制.

  - post:1.提交的键值对不在地址栏. 2.安全性相对较高. 3.对提交内容的长度理论上无限制.

`<input>`标签为文本输入框

