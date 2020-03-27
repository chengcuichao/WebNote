### CSS 简介

CSS 指层叠样式表 (Cascading Style Sheets)，是为了解决内容与表现相分离的问题。

### CSS 的存在形式

#### 1、在标签里面

```html
<div style="background-color: aqua;height: 50px;width: 1000px"></div>
```

#### 2、可以写在head里面

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

#### 3、通过引入CSS文件

```html
<link rel="stylesheet" href="commons.css" />
```

#### 4、CSS的注释

```html
<!--<img src="a1.png" style="height: 15px;width: 15px"/>-->    #baody里面的注释
/*#text-align: center;*/                                       #style里的注释
```

#### 5、标签选择器

**1、id选择器：**

id 选择器可以为标有特定id的html元素指定特定的样式，html元素以id属性来设置id选择器，css中id选择器以 "#" 来定义，如：

` #para1 {text-align:center;color:red; } `

**2、class选择器：**

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用class 选择器在HTML中以class属性表示, 在 CSS 中，类选择器以一个点"."号显示：

` .center {text-align:center;} `

**3、标签选择器：**

标签选择器是为特定的标签添加特定样式，在css中直接以标签名来定义：

`div {color:red;}`

**4、层级选择器**

层级选择器是通过上面特定选择器进行一层一层向下筛选，中间使用","隔开：

`.c1 .c2 div{text-align:center;}`

**5、组合选择器**

组合选择器是每个逗号隔开的选择器都生效下去：

`#i1,.c2,div{color:red;}`

 **6、属性选择器**

对选择到的标签再通过属性再进行一次筛选，属性通过"[]"括起来：

`.c1[name='jack']{ width:100px; height:200px; }`

