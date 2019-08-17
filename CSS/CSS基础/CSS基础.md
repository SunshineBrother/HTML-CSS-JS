# CSS基础

CSS (Cascading Style Sheets) 用于渲染HTML元素标签的样式.

CSS 是在 HTML 4 开始使用的,是为了更好的渲染HTML元素而引入的.

CSS 可以通过以下方式添加到HTML中:

- 内联样式 在HTML元素中使用"style" 属性
- 文档样式表 在HTML文档头部 `<head> `区域使用`<style>` 元素 来包含CSS
- 外部引用  使用外部 `CSS` 文件


最好的方式是通过外部引用CSS文件.



### 内联样式

当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性

```
<div style="color:blue;background-color:red;font-size:30px;">我是div</div>
```

### 文档样式表

⽂文档样式表(document style sheet)、内嵌样式表(embed style sheet)

将样式写在head元素的style元素中


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        div {
            /* 文字颜色 */
            color: green;
            /* 设置背景色 */
            background-color: red;
            /* 文字大小 */
            font-size: 30px;
        }
    </style>
</head>
<body>
<div>我是div</div>
</body>
</html>

```


### 外部样式表

将样式写在单独的CSS⽂文件中，然后在当前⽹网⻚页的head元素中⽤用link元素引⽤用

在CSS⽂文件中使⽤用@charset指定⽂文件编码，一般都是UTF-8

page.css

```
@charset "UTF-8";

div {
    color: blue;
    background-color: red;
    font-size: 30px;
}
```


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <link rel="stylesheet" href="css/page.css">
</head>
<body>
<div>我是div</div>
</body>
</html>
```


**@import**



可以在style元素或者CSS⽂文件中使⽤用@import导⼊入其他的CSS⽂文件

不不建议使⽤用@import导⼊入CSS⽂文件，它的效率⽐比link元素低
 


































