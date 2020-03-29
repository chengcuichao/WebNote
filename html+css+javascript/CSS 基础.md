### CSS 简介

CSS 指层叠样式表 (Cascading Style Sheets)，一种用来为结构化文档（如 HTML 文档或 XML 应用）添加样式（字体、间距和颜色等）的计算机语言，定义如何渲染 HTML 标签，设计网页显示效果，

### CSS基础

#### 1、语法

```css
h1 {color: red;}
/*  h1是选择器，color是属性，red是属性值，各属性通过 ; 隔开 */  注释是通过/* */来注释的
```

#### 2、CSS数值与单位

**1、颜色值**

网页中的颜色设置有字体颜色，背景颜色，边框颜色等，设置颜色的方法也有很多，通过英文来命名颜色：

```css
p {color: pink;}
```

由 Red、Green、Blue 三种颜色的比例来配色，简称 RGB：

```css
p {color: rgb(154, 32, 432);}
p {color: rgb(30%, 20%, 40%);}
```

现在较为普遍的颜色使用法，其原理其实也是 RGB 设置，但是其每一项的值由 `0~255` 变成了十六进制 `00-ff`：

```css
p {color: #00eeff;}
```

[RGB颜色对照表](https://www.114la.com/other/rgb.html)

**2、长度值**

长度单位常用的有：`px`，`em`，`%`，这三种单位都是相对单位。px 像素（Pixel）。相对长度单位，像素 px 是相对于显示器屏幕分辨率而言的。

```css
    p {
      font-size: 14px;
      line-height: 2em;
    }
    div {
        width: 50%;
        background-color: aqua;
        height: 100px
    }
    /*就是本元素给定字体的 font-size 值，如果元素的 font-size 为 14px，那么 1em=14px。如果 font-size 为 18px，那么 2em=36px*/
```

#### 3、CSS的存在形式

**1、在标签里面**

```html
<div style="background-color: aqua;height: 50px;width: 1000px"></div>
```

**2、可以写在head里面**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div {
            width: 300px;
            height: 100px;
            background-color: aqua;
            border: 3px groove black;
        }
    </style>
</head>
<body>
<div ></div>
</body>
</html>
```

**3、通过引入CSS文件**

```html
<link rel="stylesheet" href="commons.css" />
```

PS：生效的优先级为离标签近的优先级最高

#### 4、标签选择器

**1、id选择器：**

id 选择器可以为标有特定id的html元素指定特定的样式，html元素以id属性来设置id选择器，css中id选择器以 "#" 来定义，如：

```css
#para1 {text-align:center;color:red; }
```

**2、class选择器：**

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用class 选择器在HTML中以class属性表示, 在 CSS 中，类选择器以一个点"."号显示：

```css
.center {text-align:center;}
```

**3、标签选择器：**

标签选择器是为特定的标签添加特定样式，在css中直接以标签名来定义：

```css
div {color:red;}
```

**4、层级选择器**

层级选择器是通过上面特定选择器进行一层一层向下筛选，中间使用","隔开：

```css
.c1 .c2 div{text-align:center;}
```

**5、组合选择器**

组合选择器是每个逗号隔开的选择器都生效下去：

```css
#i1,.c2,div{color:red;}
```

 **6、属性选择器**

对选择到的标签再通过属性再进行一次筛选，属性通过"[]"括起来：

```css
.c1[name='jack']{ width:100px; height:200px; }
```

**7、伪类选择器**

CSS 伪类用于向某些选择器添加特殊的效果，前面跟选择器后面加冒号和伪类名。

- :link       应用于未被访问过的链接。
- :hover   应用于有鼠标指针悬停于其上的元素。
- :active   应用于被激活的元素，如被点击的链接、被按下的按钮等。
- :visited  应用于已经被访问过的链接。

### CSS的基本样式

#### 1、文字样式

**1、字体**

通过 `font-family` 属性设置字体种类，注意不要设置不常用的字体，因为如果用户本地电脑上如果没有安装你设置的字体，就会显示浏览器默认的字体。几乎所有系统都能够支持的几种字体：Arial，Courier New，Georgia，Times New Roman，Trebuchet MS，Verdana。

**2、字体样式属性**

|      属性       |                           属性说明                           |
| :-------------: | :----------------------------------------------------------: |
|    font-size    |              字体大小，字体的常用单位是：px，em              |
|      color      |                            颜色值                            |
|   font-weight   |       设置字体的粗细，normal：字体正常，bold：文字加粗       |
|   font-style    | 属性设置文字格式，normal: 将存在的斜体关闭，italic: 将字体设置为斜体版本 |
| text-decoration | none: 取消已经存在的任何文本装饰，underline: 文本下划线，overline: 文本上划线，line-through: 穿过文本的线（删除线）。 |
|   text-align    |   left 设置左对齐，使用 right 设置右对齐，center 中间对齐    |

**3、段落排版**

| 属性           | 属性说明                                     |
| -------------- | -------------------------------------------- |
| text-indent    | 段落缩进，常用的单位em                       |
| line-height    | 行高，常用单位是：px，em                     |
| letter-spacing | 设置中文字间距、字母间距，常用单位是：px，em |

**4、Web字体**

可以通过@font-face 指定要下载的字体文件，再通过font-family应用字体。

```css
<style>
    @font-face {
      font-family: "Bitstream Vera Serif Bold";
      src: url("http://developer.mozilla.org/@api/deki/files/2934/=VeraSeBd.ttf");
    }
    body {
        font-family: "Bitstream Vera Serif Bold", serif;
    }
</style>
```

#### 2、边框样式

边框 (border) 是围绕元素内容和内边距的一条或多条线，可以设置它的粗细，样式和颜色，边框语法：

```css
border: border-width||border-style||border-color;
div {
  border: 2px solid red;
}
/* 
常用的样式有 dashed（虚线）、dotted（点线）、solid（实线） 
border-radius:25px;      #圆角边框50%的话变为圆
box-shadow:5px 5px 4px;  #出现阴影
*/
```

也可以通过`border-width`，`border-style`，` border-color`来直接设置。

#### 3、背景

背景常用属性：

|       属性名        |    属性说明    |                           书写格式                           |
| :-----------------: | :------------: | :----------------------------------------------------------: |
|  background-color   |    背景颜色    |                    background-color:red;                     |
|  background-image   |    背景图片    |       background-image:url('image/4.gif');默认重复堆放       |
| background-position | 背景图片的位置 | background-position-x:10px；移动图片的位置（左右）                background-position-y:10px；  移动图片的位置（上下） |
|  background-repeat  |  背景如何重复  | repeat-y 只重复竖直方向，repeat-x只上下重复，no-repeat不重复 |
|   background-size   |  背景图片大小  |  background-size:20px 30px; 第一个设置宽度，第二个设置高度   |

### CSS的区块化样式

#### 1、Html 标签的分类

​	HTML 中的标签大体被分为三类：块级、行内、行内块。**块级标签**有自己的宽度和高度，也就是可以自定义 width 和 height，除此之外，块级元素独自占据一行高度（float 浮动除外），一般可以作为其他容器使用，可容纳块级元素和行内元素。**行内标签**不可以设置宽（width）和高（height），但可以与其他行内标签位于同一行，行内标签内一般不可以包含块级元素。行内元素的高度一般由元素内部的字体大小决定，宽度由内容的长度控制。**行内块标签**，它既具有块级元素的特点，也有行内元素的特点，它可以自由设置元素宽度和高度，也可以在一行中放置多个行内块级元素。比如 input、img 就是行内块级元素，它可以设置高宽以及一行多个。

#### 2、盒子模型

区块模型也就是我们常说的盒子模型，而所谓盒子模型就是把 HTML 页面中的元素看作是一个矩形的盒子，也就是一个盛装内容的容器。

盒模型的宽度和高度和我们平常所说的物体的宽度和高度是不一样的。CSS 定义的宽和高，指的是填充以里的内容范围。

因此盒子的宽度=左外边距+左边框+左内边距+内容宽度+右内边距+右边框+右外边距。

每个矩形都由元素的内容（content）、内边距（padding）、边框（border）和外边距（margin）组成。

#### 3、Panding

`padding` 内边距位于内容框的外边缘与边界的内边缘之间。`padding-top`：上内边距，`padding-right`：右内边距，`padding-bottom`：下内边距，`padding-left`：左内边距。`padding` 属性接受长度值或百分比值，但不允许使用负值。

#### 4、Margin

外边距（margin）代表 CSS 框周围的外部区域，称为外边距。和 padding 类似，也有 `margin-top`、`margin-right`、`margin-bottom` 和 `margin-left`，与 padding 不同的是 margin 可以是负值。

#### 5、 Overflow

当你使用绝对的值设置了一个框的大小（如，固定像素的宽/高），允许的大小可能不适合放置内容，这种情况下内容会从盒子溢流。我们使用 `overflow` 属性来控制这种情况的发生。

```css
/*
auto     当内容过多的时候溢流的内容被隐藏，然后出现滚动条，让我们滚动查看所有的内容。
hidden   当内容过多，溢流的内容被隐藏。
visible  当内容过多，溢流的内容被显示在盒子的外边。
*/
```

**6、Display**

| 属性值       | 说明                                                         |
| ------------ | ------------------------------------------------------------ |
| none         | 让标签消失                                                   |
| inline       | 把标签设为行内标签                                           |
| block        | 把标签设为块标签                                             |
| inline-block | 默认自己有多少占多少，具有block属性，可以设置高度，宽度，padding margin |

行内标签：无法设置高度，宽度，无法设置padding，margin
		块级标签：设置高度，宽度，可以设置padding，margin

### CSS 的布局模型

#### 1、流动模型

块状元素都会在所处的包含元素内，自上而下按顺序垂直延伸分布，因为在默认状态下，块级元素的宽度都为 100%，实际上，块状元素都会以行的形式占据位置（每一个便签都显示着自己本来默认的那个宽高）。

在流动模型下，行内元素都会在所处的包含元素内从左到右水平分布显示（内联元素可不像块级元素独占一行的）。

#### 2、浮动模型

块状元素都是独占一行，如果现在我们想让两个块状元素并排显示，怎么办呢？设置元素浮动就可以实现。 任何元素在默认情况下是不能浮动的，但可以用 CSS 定义为浮动，如 div、p、table、img 等元素都可以被定义为浮动。

float 可以使块标签堆叠起来

```html
<head>
  <style>
    div {
      width: 200px;
      height: 200px;
      border: 2px blue solid;
      float: left;
    }
  </style>
</head>
<body>
  <div></div>
  <div></div>
</body>
```

#### 3、层模型

`position` 主要是让标签固定到屏幕的固定位置，position会把标签变为行内标签，会把标签分层

|              属性示例              |                   说明                    |
| :--------------------------------: | :---------------------------------------: |
|          position: fixed;          | 固定在屏幕的特定位置，可以用fixed进行分层 |
|        position: absolute;         |   固定开始屏幕的位置，不会随下拉而移动    |
|    position: relative+absolute;    |      固定在relative标签里的相对位置       |
| top: 0;bottom: 0;left: 0;right: 0; |           离上下左右距离有多远            |
|            z-index: -2;            |         层级顺序，越大优先级越高          |
|            opcity: 0.5;            |                  透明度                   |

**固定定位 position: fixed**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .pg-header{
            height: 48px;
            background-color: black;
            color: #dddddd;
            position: fixed;
            top:0;
            right: 0;
            left: 0;
        }
        .pg-body{
            background-color: #dddddd;
            height: 5000px;
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <div class="pg-header">头部</div>
    <div class="pg-body">内容</div>
</body>
</html>
<!--始终固定在顶部-->
```

**绝对定位 absolute**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title></title>
    <style type="text/css">
      div {
        width: 200px;
        height: 200px;
        border: 5px red solid;
        position: absolute;
        left: 100px; /*相对于浏览器向左偏移100像素*/
        top: 80px; /*相对于浏览器向上偏移80像素*/
      }
    </style>
  </head>
  <body>
    <div></div>
    <!-- 相对于浏览器进行定位 -->
  </body>
</html>
```

**相对定位 relative+absolute**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body style="margin: auto">
<div style="height: 300px;width: 300px;background-color: aqua;position:relative;margin: 0 auto;">
    <div style="height: 20px;background-color:greenyellow;width: 20px;position: absolute;left: 0;bottom: 0"></div>
</div>
</body>
</html>
```

**对标签进行分层**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <div style="display:none;z-index:10; position: fixed;top: 50%;left:50%;
    margin-left: -250px;margin-top: -200px; background-color:white;height: 400px;width:500px; ">

        <input type="text" />
        <input type="text" />
        <input type="text" />

    </div>

    <div style="display:none;z-index:9; position: fixed;background-color: black;
    top:0;
    bottom: 0;
    right: 0;
    left: 0;
    opacity: 0.5;
    "></div>

    <div style="height: 5000px;background-color: green;">
        asdfasdf
    </div>
</body>
</html>

```

