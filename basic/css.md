# css 基础

作业：按照设计稿美化之前的 html



## 目标：

1.   css 基础 https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/CSS_basics
2.   掌握常用的 css 选择器用法  https://www.w3school.com.cn/css/index.asp
3.   掌握布局方法  https://www.runoob.com/css/css-website-layout.html
4.   能制作简单的平移、缩放、旋转等动画  https://www.runoob.com/css3/css3-animations.html



## 讲解：

准备工作：在之前 html 文件的 head 之间贴入代码 `<link rel="stylesheet" href="***.css">`，根据实际位置写入文件路径，在 css 文件中写样式。

```
.digest {
	border: 1px solid #ccc;
	padding: 10px;
	color: #333;
}
```



`.digest` 叫选择器，指的是 css 选择页面中的节点，对应页面中的 `class="digest"`，与具体标签无关

`{}` 为固定语法，`{}` 之间写入 css 规则，建议每行一个，格式为 `css rule: value`，必须 `;` 结尾



### css 规则解释

👇🏻作用域

```
.a .b {} 	// 注意 .a 与 .b 之间有半角空格

<div class="a">
	<span class="b"></span>
</div> 	
//生效

<div class="a">
	<div class="a-child">
		<span class="b"></span>
	</div>
</div> 
//生效

<div class="a"></div> 
<span class="b"></span>
//不生效
```





👇🏻锁定标签，**不推荐使用**


```
div.a{}

<div class="a">		//生效
<span class="a">  //不生效
```





👇🏻双 class 锁定，**不推荐使用**

```
.a.b{}	// 注意 .a 与 .b 紧贴，没有半角空格


<span class="a b">  //生效

<div class="a">
	<span class="b"></span>
</div> 	
//不生效
```

   



👇🏻css 合并及覆盖

```
.a { 
	color: #ccc; 
	font-size:12px; 
}
.a { 
	border: 1px solid #cd0000; 
	font-size:14px; 
}

//等效
.a {
	color: #ccc; 
	border: 1px solid #cd0000;  // .a 同名合并
	font-size: 14px;  //后面覆盖前面
}
```





👇🏻深度优先，选择器定义的深度具有优先级，也就是说，选择器越精准，越具有优先权

```
.c { 
	font-size: 12px; 
}
.a .c { 
	font-size: 14px; 
}

<div class="a">
	<span class="c">这里文字最终显示为 14px</span>
</div>
```





👇🏻多选择器同时定义

```
.a,
.b {
	font-size: 14px;
}

//等同于
.a {
	font-size: 14px;
}
.b {
	font-size: 14px;
}

<div class="a">这里文字最终显示为 14px</div>
<span class="b">这里文字也是 14px</span>
```



**注意事项：**

1.  推荐只使用 class，**class 不得以数字或特殊字符开头**
2.  不使用 id，因为 id 在页面需要保持唯一，id 定义的 css 难以复用
3.  命名方式推荐 bem 规则 https://juejin.cn/post/6844903672162304013
4.  css 代码都分离成独立的文件引用
