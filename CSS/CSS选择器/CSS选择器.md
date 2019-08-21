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



### 属性选择器（attribute selectors） - [att]


可以为拥有指定属性的 HTML 元素设置样式，而不仅限于 class 和 id 属性。

【注释】：只有在规定了 !DOCTYPE 时，IE7 和 IE8 才支持属性选择器。在 IE6 及更低的版本中，不支持属性选择。


**拥有title属性的元素**


```
<style>
    [title]{
        color: red;
    }
</style>


<body>
    <div title="one">我是内容1</div>
    <div title="two">我是内容2</div>
    <div title="">我是内容3</div>
    <div>我是内容4</div>
</body>
```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/属性1.png)


**title属性值恰好等于one的元素**


```
<style>
    [title="one"]{
        color: red;
    }
</style>


<body>
    <div title="one">我是内容1</div>
    <div title="two">我是内容2</div>
    <div title="">我是内容3</div>
    <div>我是内容4</div>
</body>
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/属性1.png)


**[attr~=val]**

title属性值包含单词one的元素（单词one与其他单词之间必须用空格隔开）
```
[title~="one"]{
        color: red;
    }
```

**[attr|=val]**


title属性值恰好等于one 或者 以单词one开头且后面紧跟着连字符-的元素

**[attr^=val]**

title属性值以单词one开头的元素


**[attr$=val]**

title属性值以单词one结尾的元素


**`[attr*=val]`**

title属性值包含单词one的元素

### 后代选择器（descendant combinator）


div元素里面的span元素（包括直接、间接子元素）

```
<style>
    div span{
        color: red;
    }
</style>

<body>
    <div>我是内容1</div>
    <div>
        <span>我是内容2</span>
        <p><span>我是内容3</span></p>
    </div>
</body>
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/后代选择器.png)


### 子选择器（child combinators）

div元素里面的直接span子元素（不包括间接子元素）

```
<style>
    div>span{
        color: red;
    }
</style>

<body>
    <div>我是内容1</div>
    <div>
        <span>我是内容2</span>
        <p><span>我是内容3</span></p>
    </div>
</body>
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/子选择器.png)



### 相邻兄弟选择器（adjacent sibling combinator）

div元素后面紧挨着的p元素（且div、p元素必须是兄弟关系）

```
<style>
    div+p{
        color: red;
    }
</style>

<body>
    <p>我是内容1</p>
    <div>
        <p>我是内容2</p>
    </div>
    <p>我是内容3</p>
</body>
```
 


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/兄弟选择器.png)


### 选择器组 

**交集选择器**

同时符合2个条件的元素：div元素、class值有one
```
div.one {
    color: red;
}
```


**并集选择器**

所有的div元素 + 所有class值有one的元素 + 所有title属性值等于test的元素

```
div, .one,[title="test"] {
    color: red;
}
```


### 伪类


CSS 伪类用于向某些选择器添加特殊的效果。

- 动态伪类（dynamic pseudo-classes）
    - `:link、:visited、:hover、:active、:focus`
- 目标伪类（target pseudo-classes）
    - `:target`
- 语言伪类（language pseudo-classes）
    - `lang( )`
- 元素状态伪类（UI element states pseudo-classes）
    - `:enabled、:disabled、:checked`
- 结构伪类（structural pseudo-classes）
    - `:nth-child( )、:nth-last-child( )、:nth-of-type( )、:nth-last-of-type( )、:first-child、:last-child、:first-of-type、:last-of-type:root、:only-child、:only-of-type、:empty`
- 否定伪类（negation pseudo-classes）
    - `:not()`


#### 动态伪类

使用举例
- a:link 未访问的链接
- a:visited 已访问的链接
- a:hover 鼠标挪动到链接上
- a:active 激活的链接（鼠标在链接上长按住未松开）


使用注意
`:hover`必须放在`:link`和`:visited`后面才能完全生效
`:active`必须放在`:hover`后面才能完全生效
所以建议的编写顺序是 `:link、:visited、:hover、:active`

记忆：女朋友看到LV包包后，ha ha大笑

除了a元素，:hover、:active也能用在其他元素上

```
<style>
        /* 未访问的链接 */
        a:link {
            color: red;
        }
        /* 已访问的链接 */
        a:visited {
            color: green;
        }
        /* 当鼠标移动到链接上 */
        a:hover {
            color: blue;
        }
        /* 被激活的链接（当鼠标左键单击链接时，未松开） */
        a:active {
            color: yellow;
        }
</style>
```

**:focus**

:focus指当前拥有输入焦点的元素（能接收键盘输入）

文本输入框一聚焦后，背景就会变红色

```
input:focus {
    color: red;
}
```


#### 目标伪类（target pseudo-classes）

当元素被锚点链接当作目标跳转之后起作用


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/target.png)

#### 语言伪类（language pseudo-classes）


语言是en系列（英语）的所有div元素

```
div:lang(en){
    color: red
}

<body>
   <div>文本1</div>
   <span>文本2</span> 
</body>
```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS选择器/语言伪类.png)





























































































