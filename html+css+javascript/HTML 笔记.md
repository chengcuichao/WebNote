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

|   属性名    |                           属性说明                           |
| :---------: | :----------------------------------------------------------: |
|    type     | 标签类型，包括：text、password、submit、button、radio、checkbox、file等 |
|    name     |                     表单提交字典的key值                      |
|    value    |          文字字段的默认取值，也是表单提交的value值           |
|    size     |                          控件的长度                          |
|  maxlength  |                          最长字符数                          |
| placeholder |                     会在输入框里增加提示                     |
|  autofocus  | 当`autofocus="autofocus"` 时，在页面加载时，域自动地获得焦点。 |
|    form     | `form` 属性适用于所有 `<input>` 标签的类型,`form` 属性必须引用所属表单的 `id` |
|  multiple   | 当`multiple="multiple"`时，允许输入域中可选择多个值，适用于 `<input>` 标签：`email` 和 `file` |
|   pattern   | `pattern`后面跟正则表达式，适用于 `<input>` 标签：text, search, url, telephone, email, password |

input 标签 type 属性详细说明：

| type属性值 |                          属性值说明                          |
| :--------: | :----------------------------------------------------------: |
|    text    |                           文本内容                           |
|  password  |                           密码文本                           |
|   submit   |                         表单提交按钮                         |
|   button   |                             按钮                             |
|   radio    |  单选框 ，checked="checked"（默认选中），name属性相同则互斥  |
|  checkbox  | 复选框 , checked="checked"（默认选中），name属性相同批量提交数据 |
|    file    |  文件，依赖form表单的一个属性 enctype="multipart/form-data"  |
|    rest    |                         重置所选内容                         |
|   email    |  e-mail 地址的输入域，在提交表单时，会自动验证 email 域的值  |
|    url     |    URL 地址的输入域，在提交表单时，会自动验证 url 域的值     |
|   number   | 属性 `max` 设定允许输入的最大值，属性 `min` 设定允许输入的最小值，属性 `value` 设定默认值，属性 `step` 设定合法的数字间隔（比如 `step` 的值为 `2`，则合法的数字为 `-2`,`0`,`2`,`4` 等） |
|   range    | 显示为滑动条，同样的 `range` 也有 `max`，`min`，`value`，`step` 属性与上面所讲的 `number` 中的一致。 |
|   color    |                         用于选择颜色                         |
|  日期选择  | date：选取日、月、年   month：选取月、年   week ：选取周和年   time：选取时间（小时和分钟） datetime：选取时间、日、月、年（UTC 时间） datetime-local ：选取时间、日、月、年（本地时间） |

**2、select与option标签**

select 标签所具有的属性：

|  属性名  |                       属性说明                        |
| :------: | :---------------------------------------------------: |
|   size   |                     默认显示几个                      |
| multiple |           当 `multiple="multiple"` 可以多选           |
|   name   |                 表单提交字典里的key值                 |
|  value   |   文本内容写在`option`标签里面，提交字典里的value值   |
| selected | 写在`option`标签里面，当`selected="selected"`默认选中 |

**3、textarea标签**

textarea 标签所具有的属性：

|   属性名    |       属性说明        |
| :---------: | :-------------------: |
|    name     | 表单提交字典里的key值 |
|    clos     |       代表列数        |
|    rows     |       代表行数        |
| placeholder | 会在输入框里增加提示  |

例1：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
     <form action="http://localhost:8888/index" method="get">
         <select name="city" multiple="multiple" size="10">
             <option value="1">北京</option>
             <option value="2">天津</option>
             <option value="3" selected="selected">石家庄</option>
             <option value="4">南京</option>
             <option value="5">成都</option>
             <option value="6">哈尔滨</option>
         </select>
         <input type="text" name="user" value="chengcuichao"/>
         <input type="password" name="pwd" value="949885"/>
         <input type="button" value="登录1" />
         <p>请选择：</p>
         男<input type="radio" name="sex" checked="checked"/>
         女<input type="radio" name="sex"/>
         <p>爱好：</p>
         足球<input type="checkbox" name="like" checked="checked">
         篮球<input type="checkbox" name="like" checked="checked">
         羽毛球<input type="checkbox"  name="like">
         乒乓球<input type="checkbox"  name="like">
         <p>上传文件</p>
         <input type="file" name="filename">
         <p></p>
         <textarea name="text" placeholder="请输入介绍"></textarea>
         <input type="submit" value="提交" />
         <input type="reset" value="重置" />
     </form>
</body>
</html>
```

 实例2，将搜索转发到百度搜索：：

```html
<form action="https://www.baidu.com/s?">
       <input type="text"  style="width: 400px;height: 30px" name="wd"/>
       <input type="submit" style="width: 75px;height: 34px;" value="百度一下"/>
  </form>
```

#### 13、iframe标签

可以使浏览器窗口中显示不止一个页面，src 便是显示url的页面，width，height表示宽度和高度，`frameborder="0"`表示移除 iframe 的边框。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<!--iframe - 设置高度与宽度,移除边框-->
<iframe src="http://baidu.com" frameborder="0" width=100% height="400"></iframe>

 <!--因为 a 标签的 target 属性是名为 shiyanlou 的 iframe 框架，所以在点击链接时页面会显示在 iframe 框架中。-->
<p><a href="https://baidu.com/" target="baidu">实验楼</a></p>
<iframe width="400" height="400" name="baidu" ></iframe>
</body>
</html>
```

#### 14、label 标签

```html
<body>
    <label for="username">用户名：</label>
    <input id="username" type="text" name="user" />
    <!--点击用户名就可以直接输入-->
</body>
```

#### 15、datalist 元素

通常，这是作为一个下拉框向用户展示的，在输入框中输入可能匹配的内容。

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title></title>
  </head>
  <body>
    <label for="myColor">What's your favorite color?</label>
    <input type="text" name="myColor" id="myColor" list="mySuggestion" />
    <datalist id="mySuggestion">
      <option>black</option>
      <option>blue</option>
      <option>green</option>
      <option>red</option>
      <option>white</option>
      <option>yellow</option>
    </datalist>
  </body>
</html>
```

