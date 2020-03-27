### HTML介绍

HTML（超文本标记语言）是一种用于创建网页的标准标记语言。 HTML 不需要编译，可以直接由浏览器执行，它的解析依赖于浏览器的内核。 它不是一种编程语言，而是一种标记语言。

### HTML基本结构

一个html基本有以下结构：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
</html>
```

`<!DOCTYPE html>`是我们的文档声明头。他告诉了浏览器，本文档处理的是 HTML 文档。`html` 标签即根元素，此处表示文档的开始。`head` 标签是网页的头部，设置网页的相关信息。`title` 标签设置网页标题。`body` 标签定义文档的主体，也就是我们的主要内容。

### HTML标签介绍

标记标签通常被称为 HTML 标签，HTML 标签是 HTML 语言中最基本的单位，HTML 标签是 HTML（标准通用标记语言下的一个应用）最重要的组成部分。HTML 标签的大小写无关的，例如 `<body>` 和 `<BODY>` 表示的意思是一样的，都代表“主体”，推荐使用小写。

##### 双标签（双标记）

是指由开始和结束两个标记符组成的标记，格式为`<标记名></标记名>` ，常见的双标签有：

```html
<html></html>
<head></head>
<title></title>
<body></body>
<h1></h1>
<p></p>
<div></div>
<span></span>
<a></a>
<ul></ul>
```

##### 单标签（单标记）

单标记是指用一个标记符号即可完整地描述某个功能的标记，最好在结尾加上`/>`，常见的单标签有：

```html
<br />
<hr />
<meta />
<img />
```

### HTML常用标签

#### 1、注释的形式为 `<!-- 在此处写注释 -->`

```html
<!-- <div style="width: 100px;height: 100px;"></div> -->
```

#### 2、meta标签

提供有关页面的元信息，如：页面编码、刷新、跳转、针对搜索引擎和更新频度的描述和关键词。

**1、页面编码（告诉浏览器是什么编码）**

```html
<meta http-equiv="content-type" content="text/html;charset=utf-8"> 
```

**2、刷新和跳转**

```html
<meta http-equiv="Refresh" Content="30">
<meta http-equiv="Refresh" Content="5; Url=http://www.autohome.com.cn" />
```

**3、搜索关键词**

```html
<meta name="keywords" content="星际2,星际老男孩,专访,F91,小色,JOY" >
```

**4、描述信息**

```html
<meta name="description" content="免费 Web & 编程 教程">
```

#### 3、p标签

```html
<p>I Love You</p>  <!-- p表示段落，默认段落之间是有间隔的。-->
```

#### 4、br标签和空格字符

`br`标签起到换行的作用，当要写的空格多的话就不能用空格符得换成`&nbsp;`，[特殊字符对照](https://www.jb51.net/onlineread/htmlchar.html)

#### 5、span标签

行内标签，为白板标签。

#### 6、div标签

块级标签，为白板标签。

#### 7、h系列标签

`h` 标签有六种 `h1`，`h2`，`h3`，`h4`，`h5`，`h6`，它代表着我们的标题。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <h1>我是一级标题</h1>
    <h2>我是二级标题</h2>
    <h3>我是三级标题</h3>
    <h4>我是四级标题</h4>
    <h5>我是五级标题</h5>
    <h6>我是六级标题</h6>
</body>
</html>
```

#### 8、img标签

html的图像是通过标签 `img`来定义的， 语法: `<img src="图片地址"/>` 。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
   <a href="http://www.baidu.com">
      <img src="s2.png" title="截图" style="height:200px;width:200px" alt="截图"/>
   </a>
       <!--实现点击图片转到百度-->
</body>
</html>
```

#### 9、a标签

`<a>`标签是超链接标签，意思就是我们点击它可以跳转到一个网页。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <a href="http://www.baidu.com" target="_blank">百度</a>
    <!--target属性，_black表示在新的页面打开-->
    <a href="#1">第一章</a>
    <a href="#2">第二章</a>
    <a href="#3">第三章</a>
    <a href="#4">第四章</a>
    <div id="1" style="height:600px;">第一章</div>
    <div id="2" style="height:600px;">第二章</div>
    <div id="3" style="height:600px;">第三章</div>
    <div id="4" style="height:600px;">第四章</div>
    <!--实现锚的作用，点击一个转到对应位置-->
</body>
</html>
```

#### 10、无序列表与有序列表

**1、无序列表**

```html
<ul type="disc">
    <li>第一章</li>
    <li>第二章</li>
    <li>第三章</li>
    <li>第四章</li>
</ul>
```

`<ul>` 标签的 type 属性：

|   type的值   | 表现形式 |
| :----------: | :------: |
| disc（默认） |  实心圆  |
|    circle    |  空心圆  |
|    square    |  小方块  |

**2、有序列表**

```html
<ol type="I">
    <li>第一章</li>
    <li>第二章</li>
    <li>第三章</li>
    <li>第四章</li>
</ol>
```

`<ol>` 标签的 type 属性：

| type的值  |           表现形式           |
| :-------: | :--------------------------: |
| 1（默认） |    数字表示（1，2，3...)     |
|     A     |   大写字母表示（A,B,C...)    |
|     a     |   小写字母表示（a,b,c...)    |
|     I     | 大写罗马数字表示(I,II,III…)  |
|     i     | 小写罗马数字表示(i,ii,iii….) |

**3、自定义列表**

自定义列表不仅仅是一列项目，而是项目及其注释的组合。自定义列表以 `dl` 标签开始。每个自定义列表项以 `dt` 开始。每个自定义列表项的定义以 `dd` 开始。自定义列表的列表项前没有任何项目符号。

```html
<dl >
    <dt>第一章</dt>
    <dd style="height:600px;">内容一</dd>
    <dt>第二章</dt>
    <dd style="height:600px;">内容二</dd>
    <dt>第三章</dt>
    <dd style="height:600px;">内容三</dd>
    <dt>第四章</dt>
    <dd style="height:600px;">内容四</dd>
</dl>
```

#### 11、表格

表格由 `<table>` 标签来定义。每个表格均有若干行（由`<tr>`标签定义），每行被分割为若干单元格（由 `<td>` 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

```html
<table border="1" width="300px" height="150px">
    <caption>
    支出表
    </caption>
    <thead>
        <tr>
            <th>支出</th>
            <th>备注</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>32</td>
            <td>买西瓜</td>
        </tr>
        <tr>
        <td>214</td>
            <td>买草莓</td>
        </tr>
    </tbody>
</table>
```

caption用来表示表格的标题，格式为`<caption> 表格标题 </caption>`

表格与单元格的属性：

|   属性名    |                           属性说明                           | 单位 |
| :---------: | :----------------------------------------------------------: | :--: |
|   border    | 显示表格边框（只有在style里面颜色和样式才生效，直接使用border属性只有大小） |  px  |
| cellspacing |                 设置单元格与单元格之间的距离                 |  px  |
| cellpadding |                  设置文字与单元格之间的距离                  |  px  |
|    width    |                        设置表格的宽度                        |  px  |
|   height    |                        设置表格的高度                        |  px  |
|   bgcolor   |                         设置背景颜色                         | 颜色 |

 注：colspan横向合并表格，rowspan纵向合并表格。

#### 12、表单

表单的提交需要 `<form>` 标签的配合，form 标签中 action 属性表示提交的url，method 表示提交的方法，能够提交表单的标签有：

**1、input标签**

input 标签所具有的属性：

|  属性名   |                           属性说明                           |
| :-------: | :----------------------------------------------------------: |
|   type    | 标签类型，包括：text、password、submit、button、radio、checkbox、file等 |
|   name    |                     表单提交字典的key值                      |
|   value   |                      文字字段的默认取值                      |
|   size    |                          控件的长度                          |
| maxlength |                          最长字符数                          |



**2、select标签**





