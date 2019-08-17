# HTML 基础
 

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
- meta
- title
- style
- link
- base
- script
- noscritpt


































