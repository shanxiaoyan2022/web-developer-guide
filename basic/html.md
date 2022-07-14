# html 基础

作业：将 [word示例](./res/example.docx) 转化为网页



## 目标：

1.   了解 html 基础逻辑 https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics

2. 了解 html 标签，熟练记忆常用标签的语义及属性 https://www.w3school.com.cn/tags/index.asp

3.   理解「表现」与「结构」分离 http://www.w3cn.org/article/tips/2004/43.html

4.   能熟练写出合理的「结构」

     

## html 文件结构

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>测试页面</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="测试图片">
  </body>
</html>
```

第 1 行固定声明[文档类型](https://developer.mozilla.org/zh-CN/docs/Glossary/Doctype)，直接使用即可，暂不解释

第 2 行文档开始，对应第 10 行文件结束

第 3 行为头部开始，对应第 6 行结束，头部会引用资源，声明编码及 meta 等，后续单独解释，连续阶段只使用 title 即可

第 7 行为内容区开始，对应 第 9 行结束，html 代码需要写入 body 之间




## 讲解

HTML 不是一门编程语言，而是一种用于定义内容结构的标记语言。HTML 由一系列的元素（elements）组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。一对标签（ tags）可以为一段文字或者一张图片添加超链接等。

```
<div class="content" contenteditable="true">
	<h1>大标题</h1>
	<h2>子标题</h2>
	<div class="digest">
		<p>匠人制造工具，直至被后人用于惶惶战争，以武器之名为世所知。</p>
		<p>一个人有两个我，一个在黑暗里醒着，一个在光明中睡着。我是烈火，我也是枯枝，一部分的我消耗了另一部分的我。</p>
	</div>
</div>
```

这是一段纯内展示 html 示例，

`<div></div>` 是标签，标签之间的代码属于标签内容，可以是一段 html，比如 `div.content`，也可以是纯文字 h1；

`<div class="content` contenteditable="true"> 之间的键值对是标签 div 的属性，不同标签具有不同的属性，不同属性有不同的取值方式；

`div.content` 包含 3 个标签，一般说有 3 个子节点，分别为 `h1`、`h2` 与 `div.digest`，在写代码时，每深入一个层级，就通过一个 tab 键缩进，通过视觉可以非常方便的了解结构。以此类推，`div.digest` 拥有两个子节点，均为 p 标签。



## 什么表现、结构分离？

网页都是以某种风格展示，展示某些信息、提供某些操作。我们上网时就是通过鼠标键盘不断操作不断阅读。经常访问的网站时不时还会变个样子。

我们访问网页时要阅读获取的信息就是内容，为了提高阅读的体验，会把内容按照一定的结构处理，比如文章一般分为标题、摘要、发布时间、封面图、摘要、作者、正文、评论区等，不同结构对应不同的标签，按照某类内容设计好结构后，就可以分离出来变成模板，用来处理更多同类的信息。

这是一个体验的年代，光有结构还不够好，标题该多大？居左居右还是居中？是否加粗？什么颜色？段落首行缩进还是首字悬浮？段落间距多大？行距多少？封面图是否加边框？诸如此类的问题还需要专业设计进行排版处理。这些都属于表现层，web 前端约定表现层统一写入 css。

**这么做的好处**是把复杂文档（想想写 word，边写边排版）分离成两个较为简单的构成，分工为两个角色各自专业工作，效率高且能适应快速变化。内容生产者可以专注于内容本身，设计师可以专注于 UI，调整设计时直接更新 css 文件，两者各自独立互不影响。



**容易混淆的表现与结构**：

1.   logo图标：属于表现，对应的结构是公司名称
2.   所有边框类：图片边框、表格边框、按钮边框、输入框边框等
3.   纯图标按钮：图标属于表现，结构为按钮 + 文字，只是后期通过 css 把文字隐藏、显示了图标
4.   斜体、粗体、下划线、删除线等
5.   回行



## 撰写 html 代码的思路

1.   要了解清楚所有，至少是常见标签的语义，在使用时才知道有哪些可选项，比如 h1 一级标题、table 表格、ul 无序列表、ol 有序列表、dl 定义列表等等
2.   不明确语义的大结构使用 div，不明确语义的少量文字用 span
3.   标签语义较弱，又只能选用，经常无法完美表达本意，可通过 class 做补充，比如讲解中的 `div.digest` ，class 是自定义的，可以完全按照数据结构逻辑描述
4.   理解文档或设计稿的结构，分离出纯粹的内容结构，撰写 html




**推荐阅读：**

1.   LaTex 的内容与样式分离 https://liam.page/2019/03/18/separation-of-content-and-presentation/
1.   MVC https://zhuanlan.zhihu.com/p/35680070
1.   MVC https://www.runoob.com/design-pattern/mvc-pattern.html
