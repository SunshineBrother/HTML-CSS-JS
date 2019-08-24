# CSS盒子模型

CSS 框模型 (Box Model) 规定了元素框处理元素内容、内边距、边框 和 外边距 的方式。也叫盒子模型


HTML中的每一个元素都可以看做是一个盒子，如右下图所示，可以具备这4个属性
- 内容（content）：盒子里面装的东西
- 内边距（padding）
- 边框（border）
- 外边距（margin）

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/Box.png)



### 宽度、高度相关属性


- width：宽度
- min-width：最小宽度，无论内容多少，宽度都大于或等于min-width
- max-width：最大宽度，无论内容多少，宽度都小于或等于max-width

- height：高度
- min-height：最小高度，无论内容多少，高度都大于或等于min-height
- max-height：最大高度，无论内容多少，高度都小于或等于max-height


### 内边距相关属性

- padding-left：左内边距
- padding-right：右内边距
- padding-top：上内边距
- padding-bottom：下内边距
- padding：是padding-top、padding-right、padding-bottom、padding-left的简写属性


**padding的取值规律**


- 按照顺时针方向设值：top、right、bottom、left

- 如果缺少left, 那么left就使用right的值

- 如果缺少bottom, 那么bottom就使用top的



### 外边距相关属性

- margin-left：左外边距
- margin-right：右外边距
- margin-top：上外边距
- margin-bottom：下外边距
- margin：是margin-top、margin-right、margin-bottom、margin-left的简写属性


**上下margin传递**

- margin-top传递
	- 如果块级元素的顶部线和父元素的顶部线重叠，那么这个块级元素的margin-top值会传递给父元素

- margin-bottom传递
	- 如果块级元素的底部线和父元素的底部线重写，并且父元素的高度是auto，那么这个块级元素的margin-bottom值会传递给父元素

- 如何防止出现传递问题？
	- 给父元素设置padding-top\padding-bottom
	- 给父元素设置border
	

**建议**

margin一般是用来设置兄弟元素之间的间距

padding一般是用来设置父子元素之间的间距

### 上下margin折叠

- 垂直方向上相邻的2个margin（margin-top、margin-bottom）有可能会合并为1个margin，这种现象叫做collapse（折叠）
- 水平方向上的margin（margin-left、margin-right）永远不会collapse
- 折叠后最终值的计算规则
	- 如果都是正数，最终值是：绝对值最大的那个正数值
	- 如果都是负数，最终值是：绝对值最大的那个负数值
	- 如果正数、负数都有，最终值是：最大正数和最小负数相加
- 如何防止margin collapse？
	- 只设置其中一个元素的margin
	- 条件允许的话，使用padding取代margin
	


**上下margin折叠**

两个兄弟块级元素之间上下margin的折叠

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/上下折叠.png)


父子块级元素之间margin的折叠

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/上下折叠1.png)


无内容块级元素内部margin的折叠


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/上下折叠2.png)



块级元素折叠问题看似有点莫名其妙，实际上还是有实用之处的
比如连续段落之间的margin，恰好需要这种折叠效果


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/上下折叠3.png)




## 边框相关的属性

- 边框宽度
	- border-top-width、border-right-width、border-bottom-width、border-left-width
	- border-width是上面4个属性的简写属性

- 边框颜色
	- border-top-color、border-right-color、border-bottom-color、border-left-color
	- border-color是上面4个属性的简写属性

- 边框样式
	- border-top-style、border-right-style、border-bottom-style、border-left-style
	- border-style是上面4个属性的简写属性


边框颜色、宽度、样式的编写顺序任意


### 边框样式的取值

- none：没有边框，边框颜色、边框宽度会被忽略
- hidden：与“none”类似，多用在表格上，用于解决边框冲突
- dotted：边框是一系列的点 
- dashed：边框是一条虚线
- solid：边框是一条实线 
- double：边框有两条实线。两条线宽和其中的空白的宽度之和等于border-width的值
- groove：边框看上去好象是雕刻在画布之内 
- ridge：和grove相反，边框看上去好象是从画布中凸出来
- inset：该边框使整个框看上去好象是嵌在画布中
- outset：和inset相反，该边框使整个框看上去好象是从画布中凸出来



![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/边框样式.png)



### 边框的形状


边框的形状可能是
矩形、梯形、三角形等形状


```
div{
            display: inline-block;
            border-top: 5px solid #f00;
            border-left: 5px solid #f0f;
            background-color: aquamarine;
        }
```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/边框样式1.png)


```
div{
            display: inline-block;
            border-top: 100px solid #f00;
            border-left: 100px solid #f0f;
            background-color: aquamarine;
        }
```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/边框样式2.png)


```
div{
            display: inline-block;
            border-top: 100px solid #f00;
            border-right: 100px solid #00f;
            border-bottom: 100px solid #000;
            border-left: 100px solid #f0f;
            background-color: aquamarine;
        }
```


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/边框样式3.png)


```
div{
            margin: 100px;
            width: 0;
            height: 0;
            border-top: 100px solid #f00;
            border-left: 100px solid transparent;
            transform: rotate(-45deg);
        }
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/边框样式4.png)




```
div{
            margin: 100px;
            width: 100px;
            height: 50px;
            border-bottom: 50px solid #111;
            background-color: #ddd;
        }
```

![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/CSS盒子模型/边框样式5.png)


### 行内级非替换元素的注意点

- 以下属性对行内级非替换元素不起作用
	- width、height、margin-top、margin-bottom

- 以下属性对行内级非替换元素的效果比较特殊
	- padding-top、padding-bottom、上下方向的border




### CSS属性radius


border-*-*-radius定义的是四分之一椭圆的半径


- 4个值的顺序是top-left、top-right、bottom-right、bottom-left（顺时针方向）
- 如果bottom-left没设置，就跟随top-right
- 如果bottom-right没设置，就跟随top-left
- 如果top-right没设置，就跟随top-left
- border-radius大于或等于50%时，就会变成一个圆





### CSS属性 - outline



- outline表示元素的外轮廓
- 不占用空间
- 默认显示在border的外面
- 每个部位都是完整连接的，不会像border那样有可能会断开（比如行内级非替换元素的换行）




outline相关属性有
outline-width
outline-style：取值跟border的样式一样，比如solid、dotted等
outline-color
outline：outline-width、outline-style、outline-color的简写属性，跟border用法类似
outline-offset：设置outline和border之间的间距

[应用实例]
去除a元素、input元素的focus轮廓效果




### CSS属性 - box-shadow

- box-shadow属性可以设置一个或者多个阴影
- 每个阴影用<shadow>表示
- 多个阴影之间用逗号,隔开，从前到后叠加
- <shadow>的常见格式如下






## 元素的水平居中显示



在一些需求中，需要元素在父元素中水平居中显示（父元素一般都是块级元素、inline-block）

- 行内级元素、inline-block元素
	- 水平居中：在父元素中设置text-align: center

- 块级元素
	- 水平居中：margin: 0 auto































