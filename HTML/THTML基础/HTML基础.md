# HTML基础
 

### ⽂文档声明

一个基本的完整的HTML代码如下所示
 

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

`<!DOCTYPE html>`


-  HTML⽂文档声明，告诉浏览器器当前⻚页⾯面是HTML5⻚页⾯面，让浏览器器⽤用HTML5的标准去解析识别HTML⽂文档
- 必须放在HTML⽂文档的最前⾯面，不不能省略略，省略略了了会出现兼容性问题
- HTML5的⽂文档声明⽐比HTML 4.01、XHTML 1.0简洁⾮非常多


### html元素

- html元素是HTML⽂文档的根元素，⼀一个⽂文档中只能有⼀一个，其他所有元素都是它的后代元素
-  W3C标准建议为html元素增加⼀一个lang属性，作⽤用是
	- 帮助语⾳音合成⼯工具确定要使⽤用的发⾳音
	-  帮助翻译⼯工具确定要使⽤用的翻译规则
	- lang="en"告诉浏览器器:这个HTML⽂文档的语⾔言是英⽂文；lang="zh"表示这个HTML⽂文档的语⾔言是中⽂文
 


### head元素

- head元素⾥里里⾯面的内容是⼀一些“元数据”(元数据:描述数据的数据)
- 一般⽤用于描述⽹网⻚页的各种信息，⽐比如字符编码、⽹网⻚页标题、⽹网⻚页图标
	- title元素 网⻚页的标题
	- meta元素 可以⽤用于设置⽹网⻚页的字符编码，让浏览器器更更精准地显示每⼀一个⽂文字，不不设置或者设置错误会导致乱码，⼀般都使⽤用UTF-8编码，涵盖了了世界上⼏几乎所有的⽂文字



以下列出的元素大多数情况下都是在head元素内部使用
- meta 定义了HTML文档中的元数据
- title 定义了文档的标题
- style 定义了HTML文档的样式文件
- link 定义了一个文档和外部资源之间的关系
- base 定义了页面链接标签的默认链接地址
- script 定义了客户端的脚本文件
- noscritpt

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/HTML/THTML基础/head元素.png)



### body元素

body元素⾥里里⾯面的内容将是你在浏览器器窗⼝口中看到的东⻄西，也就是⽹网⻚页的具体内容和结构

网页中显示的任何元素都应该是它的后代元素



### HTML 标题

 标题（Heading）是通过 `<h1> - <h6>` 标签进行定义的。
 
 
h1~h6共规定了了6个等级的标题
- h元素有助于⽹网站的SEO(Search Engine Optimization)优化，可以促进关键词排名
- 建议在⽹网⻚页中最多只有1个h1元素
- 乱⽤用h元素不不仅不不会给⽹网站带来好的权重，同时也有可能被搜索引擎认为作弊，最后导致K站
 
### HTML 水平线

<hr> 标签在 HTML 页面中创建水平线。

hr 元素可用于分隔内容。

```
<p>这是一个段落。</p>
<hr>
<p>这是一个段落。</p>
<hr>
<p>这是一个段落。</p>
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/HTML/THTML基础/hr.png)




### HTML 段落

HTML 可以将文档分割为若干段落。

段落是通过 <p> 标签定义的。

```
<p>这是一个段落 </p>
<p>这是另一个段落</p>
```


**HTML 折行**

如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 <br> 标签：

```
<p>这个<br>段落<br>演示了分行的效果</p>
```

`<br />` 元素是一个空的 HTML 元素。由于关闭标签没有任何意义，因此它没有结束标签。

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/HTML/THTML基础/br.png)


### HTML 输出- 使用提醒

我们无法确定 HTML 被显示的确切效果。屏幕的大小，以及对窗口的调整都可能导致不同的结果。
对于 HTML，您无法通过在 HTML 代码中添加额外的空格或换行来改变输出的效果。
当显示页面时，`浏览器会移除源代码中多余的空格和空行`。`所有连续的空格或空行都会被算作一个空格`。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。

想打出几个空格就显示几个空格需要用`pre`元素


```
<p>
        我需要五个空格     已经打了5个空格
    </p>
    <pre>
    哈哈
        哈                      呵
        呵呵
    hhhhh
    </pre>
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/HTML/THTML基础/pre.png)


### HTML 文本格式化

HTML 使用标签  对输出的文本进行格式 

- <b> 定义粗体文本
- <em> 定义着重文字
- <i> 定义斜体字
- <small> 定义小号字
- <strong> 定义加重语气
- <sub> 定义下标字
- <sup> 定义上标字
- <ins> 定义插入字
- <del> 定义删除字





```
<b>这个文本是加粗的</b>

<br />

<strong>这个文本是加粗的</strong>

<br />

<big>这个文本字体放大</big>

<br />

<em>这个文本是斜体的</em>

<br />

<i>这个文本是斜体的</i>

<br />

<small>这个文本是缩小的</small>

<br />

这个文本包含
<sub>下标</sub>

<br />

这个文本包含
<sup>上标</sup>


```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/HTML/THTML基础/文本格式化.png)




### HTML链接

HTML使用标签 <a>来设置超文本链接。
超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。
当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手。
 
- <a>用来显示一个超链接
- 常用属性
	- href:需要打开的URL
	- target:在哪里打开
		- _self:在当前页面中打开(覆盖当前页面)
		- _blank:当新页面中打开
		- _parent:在父页面中打开
		- _top:在顶层页面中打开
		- 某个iframe的name属性值:在某个iframe中打开
- 图片链接
- 锚点链接


在标签<a> 中使用了href属性来描述链接的地址。
默认情况下，链接将以以下形式出现在浏览器中：
- 一个未访问过的链接显示为蓝色字体并带有下划线。
- 访问过的链接显示为紫色并带有下划线。
- 点击链接时，链接显示为红色并带有下划线。

`注意：如果为这些超链接设置了 CSS 样式，展示样式会根据 CSS 的设定而显示。`


#### HTML 链接- id 属性

id属性可用于创建在一个HTML文档书签标记。其实就是根据目录找到响应的位置

- 本网页查找
```
<p>
<a href="#C4">查看章节 4</a>
</p>
```

- 跨网页查找
```
<p>
<a href="11-锚点链接_01.html#C4">查看章节 4</a>
</p>
```



#### iframe

- 在当前网页中嵌入其他网页
- 常用属性
	- src:其他页面的URL
	- frameborder:是否需要边框
		- 1:需要
		- 0:不需要


```
<!-- 需要设置iframe的name属性值（不能用id属性值），才能实现在某个iframe中打开新的页面 -->
<iframe name="frame1" src="http://www.baidu.com" frameborder="1"></iframe><br>

<iframe name="frame2" src="http://www.taobao.com" frameborder="1"></iframe><br>


<a href="http://www.qq.com" target="frame1">腾讯网(frame1)</a>

<a href="http://www.qq.com" target="frame2">腾讯网(frame2)</a>
```


**创建图片链接**

```
<p>图片链接:
        <a href="//www.runoob.com/html/html-tutorial.html">
            <img src="smiley.gif" alt="HTML 教程" width="32" height="32">
        </a>
    </p>
```

**在当前页面链接到指定位置**

```
<p>
<a href="#C4">查看章节 4</a>
</p>

<h2>章节 1</h2>
<p>这边显示该章节的内容……</p>

<h2>章节 2</h2>
<p>这边显示该章节的内容……</p>

<h2>章节 3</h2>
<p>这边显示该章节的内容……</p>

<h2><a id="C4">章节 4</a></h2>
<p>这边显示该章节的内容……</p>

<h2>章节 5</h2>
<p>这边显示该章节的内容……</p>

<h2>章节 6</h2>
<p>这边显示该章节的内容……</p>
```



### img

用来显示一张图片

常用属性
 - src:图片的URL
 - width:图片的宽度
 - height:图片的高度
 - alt:占位文字(当图片显示失败的时候显示这个占位文字)


```
<img   src="https://www.baidu.com/img/bd_logo1.png" 
            alt="这是百度的LOGO" 
            height="200" 
            width="100">
```


 
### HTML 区块元素

HTML 可以通过 `<div>` 和 `<span>`将元素组合起来。

大多数 HTML 元素被定义为`块级元素或内联元素`。

- 块级元素在浏览器显示时，通常会以新行来开始（和结束）。
	-  `<h1>, <p>, <ul>, <table>`

- 内联元素在显示时通常不会以新行开始。
	- `<b>, <td>, <a>, <img>`


**div**

HTML <div> 元素是块级元素，它可用于组合其他 HTML 元素的容器。

<div> 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。

如果与 CSS 一同使用，<div> 元素可用于对大的内容块设置样式属性。

<div> 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 <table> 

元素进行文档布局不是表格的正确用法。<table> 元素的作用是显示表格化的数据。

**span**


HTML <span> 元素是内联元素，可用作文本的容器

<span> 元素也没有特定的含义。

当与 CSS 一同使用时，<span> 元素可用于为部分文本设置样式属性。











 







