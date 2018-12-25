### css基础篇
1. 每一个html标签就是一个盒子。
当对一个文档进行布局(laying out)的时候，浏览器渲染引擎会根据CSS-Box模型（CSS Basic Box model）将所有元素表示为一个矩形盒子（box)。CSS决定这些盒子的大小，位置以及属性（颜色，背景，边框尺寸...).
在CSS中，使用标准盒模型描述这些矩形盒子中的每一个。这个模型描述了元素所占空间的内容。每个盒子有四个边：外边距边, 边框边, 内填充边 与 内容边。 

<img src="http://www.runoob.com/images/box-model.gif" width="400" height="400"/>
```
<div style="margin:50px;padding:50px;background:green;color:white"></div
显示一个绿色的长方形 中间的文字是白色的

下面的样式将会是怎么样的呢
  <div style="margin:50px;padding:50px;background:green;color:white">
      <div style="background: white;padding: 10px;margin: 9px;color: black;">我是div -- content内容<div>
  </div>
```

2. 层叠
 CSS 是 Cascading Style Sheets 的缩写，这暗示层叠（cascade）的概念是很重要的。在最基本的层面上，它表明CSS规则的顺序很重要，但它比那更复杂。什么选择器在层叠中胜出取决于三个因素（这些都是按重量级顺序排列的——前面的的一种会否决后一种）：
- 重要性（Importance）
- 专用性（Specificity）
- 源代码次序（Source order）

#### 重要性
在CSS中，有一个特别的语法可以让一条规则总是优先于其他规则：!important。把它加在属性值的后面可以使这条声明有无比强大的力量。
让我们看一下这个例子:
```
<p class="better">This is a paragraph.</p>
<p class="better" id="winning">One selector to rule them all!</p>
#winning {
  background-color: red;
  border: 1px solid black;
}

.better {
  background-color: gray;
  border: none !important; //优先级是最高的
}

p {
  background-color: blue;
  color: white;
  padding: 5px;
}
```

#### 专用性
```
专用性指的样式优先级
以下例子显示
<div id="outer" class="container">
  <div id="inner" class="container">
    <ul>
      <li class="nav"><a href="#">One</a></li>
      <li class="nav"><a href="#">Two</a></li>
    </ul>
  </div>
</div>

/* id为outer下的所有a标签 背景颜色为红色 */
#outer a { 
  background-color: red;
}

/* id为outer下的id为inner的所有a标签 背景颜色为蓝色 
  描述的仔细程度比上面样式强 所以a标签 背景颜色为蓝色
*/
#outer #inner a {
  background-color: blue;
}

/* specificity: 0104 */
#outer div ul li a {
  color: yellow;
}

/* specificity: 0113 */
#outer div ul .nav a {
  color: white;
}

/* specificity: 0024 */
div div li:nth-child(2) a:hover {
  border: 10px solid black;
}

/* specificity: 0023 */
div li:nth-child(2) a:hover {
  border: 10px dashed black;
}

/* specificity: 0033 */
div div .nav:nth-child(2) a:hover {
  border: 10px double black;
}
/*
 * a标签的样式 
 */
a {
  display: inline-block;
  line-height: 40px;
  font-size: 20px;
  text-decoration: none;
  text-align: center;
  width: 200px;
  margin-bottom: 10px;
}

ul {
  padding: 0;
}

li {
  list-style-type: none;
}
```

