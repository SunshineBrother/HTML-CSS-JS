# Font


### font-size

font-size决定文字的大小


常用的设置
- 具体数值+单位
	- 比如100px
	- 也可以使用em单位：1em代表100%，2em代表200%，0.5em代表50%
- 百分比:基于父元素的font-size计算，比如50%表示等于父元素font-size的一半
- 一般给body设置font-size就代表设置网页的默认字体大小



### font-family

font-family用于设置文字的字体名称

可以设置1个或者多个字体名称（从左到右按顺序选择字体，直到找到可用的字体为止）

一般情况下，英文字体只适用于英文，中文字体同时适用于英文和中文,所以，如果希望中英文分别使用不同的字体，应该先将英文字体写在前面，中文字体写在后面

```
div{
	font-family:"courier New","华文彩云"
}
```

### @font-face


@font-face可以让网页支持网络字体(Web Font)，不再局限于系统自带的字体

常见的字体种类
- TrueType字体：拓展名是 .ttf
- OpenType字体：拓展名是 .ttf、.otf，建立在TrueType字体之上
- Embedded OpenType字体：拓展名是 .eot，OpenType字体的压缩版
- SVG字体：拓展名是 .svg、 .svgz
- web开放字体：拓展名是 .woff，建立在TrueType字体之上


并不是所有浏览器都支持以上字体，使用时要多加测试

字体下载：http://font.chinaz.com/


### font-weight

font-weight用于设置文字的粗细（重量）

100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900：每一个数字表示一个重量

- normal：等于400 

- bold：等于700


`strong`、`b`、`h1~h6`等标签的font-weight默认就是bold


### font-stlye

font-style用于设置文字的常规、斜体显示
- normal：常规显示
- italic：用字体的斜体显示
- oblique：文本倾斜显示


### line-height

line-height用于设置文本的最小行高

行高可以先简单理解为一行文字所占据的高度


可以设置的值如下
- 具体数值+单位：比如40px
- 百分比：比如200%，最终的行高值是用百分比乘以元素的字体大小。如果是写百分比，继承下来的就是经过计算后的像素值
- 具体数值：比如1、2.5，最终的行高值是用数字乘以元素的字体大小。如果是写具体数值，继承下来的就是具体数值（比如父元素是1.5，那么子元素继承下来也是1.5）
- normal：常规显示，浏览器会基于元素字体调整成一个合理值，范围在`1.0~1.2`


注意区分height和line-height的区别

- height：元素的整体高度
- line-height：元素中每一行文字所占据的高度

应用实例：假设div中只有一行文字，如何让这行文字在div内部垂直居中
让line-height等同于height


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/font-size/lineheight.png)

line-height设置的仅仅是最小行高，不能决定最终的行高


![](https://github.com/SunshineBrother/HTML-CSS-JS/blob/master/CSS/font-size/lineheight1.png)














