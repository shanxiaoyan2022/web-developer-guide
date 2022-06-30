# 基础课程

代码与文档是分别由计算机语言和人类语言的写作，都是用来沟通，首先要写出让别人看明白的代码，这个别人也可能是不久后的自己。



## 1. 通用注意事项

1. 文件名不能使用中文、空格或特殊字符，推荐使用数字、字母（全小写）及 -(或 _ )
2. 排序方式，如果是两位数，应该是 01/02………………99，才能保证正常顺序
2. 开始写代码多写注释，可通过注释提供文档链接
2. 文档和注释主要用来补充代码无法表达的背景及设计思想等，与代码同等重要，要养成先写文档注释再写代码的习惯
2. 每天结束时提交保存当天代码，避免丢失



**推荐阅读：**

1.   少数派写作指南 https://sspai.com/post/37815
2.   中文排版 https://github.com/mzlogin/chinese-copywriting-guidelines
3.   中英文混排的 “Social Distancing” https://blog.imfing.com/2020/05/chinese-typesetting-space/
4.   Sun MicroSystems 公司 Java语言规范 https://waylau.com/java-code-conventions/page01.html



## 2. 概要

在浏览器中，主要通过 html、css 与 javascript 控制页面所能看到和操作的一切，大概的分工说明：

1.   html 负责结构化数据输出
2.   css 负责描述 html 长什么样子，如果没有 css，浏览器会采用内置的规则决定 html 最终的样子
3.   javascript 可以访问页面所处环境，可以捕获键盘、鼠标等外设，并且可以修改 html 及 css 内容，因此页面可以根据各种操作作出交互效果



## 3. html 基础

**目标：**

1.   了解 html 标签，熟练记忆常用标签的语义及属性
2.   了解页面结构
3.   理解「表现」与「结构」分类的概念，以及这么做的用意
4.   能熟练写出合理的「结构」
5.   熟练写出表单结构



作业：将 [word示例](./res/example.docx) 转化为网页



**推荐阅读：**

1.   循序渐进上手 http://www.w3cn.org/article/step/index.html

2.   html 基础 https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics

3.   构建 html https://developer.mozilla.org/zh-CN/docs/Learn/HTML

4.   html 标签大全 https://www.w3school.com.cn/tags/index.asp

     

## 4. css 基础

**目标：**

1.   掌握常用的 css 选择器用法
2.   掌握布局方法
3.   能制作简单的平移、缩放、旋转等动画



**注意事项：**

1.  不使用 id 定义，使用 class，class 不得以数字或特殊字符开头
2.  推荐 bem 规则 https://juejin.cn/post/6844903672162304013
3.  css 代码都分离成独立的文件引用



**推荐阅读：**

1.   https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/CSS_basics
1.   css 命令 https://www.w3school.com.cn/css/index.asp
1.   css 布局 https://www.runoob.com/css/css-website-layout.html
1.   css3 动画 https://www.runoob.com/css3/css3-animations.html



## 5. javascript 基础

**目标：**

1.   了解事件及监听
2.   掌握变量定义、作用域及函数定义
3.   掌握点击弹出、鼠标经过变色等常见交互的开发



**推荐阅读：**

1.   函数及传参 https://www.runoob.com/js/js-functions.html
2.   事件 https://www.runoob.com/js/js-events.html
3.   作用域 https://www.runoob.com/js/js-scope.html
4.   dom https://www.runoob.com/js/js-htmldom-html.html
5.   dom css https://www.runoob.com/js/js-htmldom-css.html