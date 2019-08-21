# CSS选择器

什么是CSS选择器
按照一定的规则选出符合条件的元素，为之添加CSS样式

**选择器的种类繁多，大概可以这么归类**

- 通用选择器（universal selector）
- 元素选择器（type selectors）
- 类选择器（class selectors）
- id选择器（id selectors）
- 属性选择器（attribute selectors）
- 组合（combinators）
- 伪类（pseudo-classes）
- 伪元素（pseudo-elements）




### 元素选择器（type selectors）

所有的div元素

```
<style>
        div{
            color: red;
            background-color: aqua;
        }
</style>


<body>
    <div>文字内容1</div>
    <span>文字内容2</span>
    <div>文字内容3</div>
    <p>文字内容4</p>

</body>

```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/元素选择器.png)



### 通用选择器（universal selector）

所有的元素

一般用来给所有元素作一些通用性的设置
比如内边距、外边距
效率比较低，尽量不要使用

```
<style>
    *{
        color: red;
      }
</style>

<body>
    <span>文本1</span>
    <div>文本2</div>
    <p>文本3</p>
</body>

```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/通用选择器.png)


### id选择器（id selectors）

一个HTML文档里面的id值是唯一的，不能重复

id值如果由多个单词组成，单词之间可以用中划线-、下划线_连接，也可以使用驼峰标识

最好不要用标签名作为id值

```
<style>
    #one{
        color: red;
    }
</style>


<body>
    <div id="one">我是文本1</div>
    <div id="two">我是文本2</div>
</body>
```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/id选择器.png)



### 类选择器（class selectors）

一个元素可以有多个class值，每个class之间用空格隔开

class值如果由多个单词组成，单词之间可以用中划线-、下划线_连接，也可以使用驼峰标识

```
<style>
        .btn{
            font-weight: normal;
            color: #fff;
            font-size: 18px;
            padding: 20px;
            cursor: pointer;
        }
        .danger{
            background-color: red;
        }
        .warning{
            background-color: #f6c12a;
        }
        .normal{
            background-color: #57b5e3;
        }
        .cancel{
            background-color: #57b5e3;
        }

 </style>


<body>
    <strong class="btn normal">确定</strong>
    <strong class="btn warning">重置</strong>
    <strong class="btn cancel">取消</strong>
    <strong class="btn danger">删除</strong>
    <strong class="btn danger">关闭</strong>
</body>



```





![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/类选择器.png)





















































































