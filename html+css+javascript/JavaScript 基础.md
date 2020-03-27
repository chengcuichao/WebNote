### JavaScript 变量

#### 1、JavaScript代码存在的形式

**1、写在 html 的 head 中或 body 标签最下面**

```javascript
<script>
    //javascript代码
    alert(123);
</script>

<script type="text/javascript">
    //javascript代码
    alert(123);
</script>
```

**2、通过文件引入**

```javascript
<script type="text/javascript" src='js文件路径'> </script> 
//  单行注释
/*  
	多行注释   
*/
```

**PS： JS代码最好放置在 `<body>`标签内部的最下方**

#### 2、变量

变量的命名规则如下：

- 变量名必须以字母、下划线 “_”、美元符号 “$” 开头，不能以数字开头。
- 变量可以包含字母、数字、下划线和美元符号。
- 不能使用 JavaScript 中的关键字做为变量名。
- 变量名不能有空格。
- 变量名对大小写敏感，比如：name 和 Name 就是两个完全不同的变量。

```javascript
user = 'cheng';      //全局变量
var user = 'cheng'   //局部变量
```

#### 3、数据类型

null是JavaScript语言的关键字，它表示一个特殊值，常用来描述空值。 undefined是一个特殊值，表示变量未定义。

**1、数字类型**

在 JavaScript 中，不管什么数字类型的全部用 `var` 声明就可以了，而且 JavaScript 中只有一个数据类型：Number。

**算数运算符：**

| 运算符 | 说明 | 示例 |
| :----: | :--: | :--: |
|   +    |  加  | x+y  |
|   -    |  减  | x-y  |
|   *    |  乘  | x*y  |
|   /    |  除  | x/y  |
|   ++   | 累加 | x++  |
|   --   | 累减 | x--  |
|   %    | 取余 | x%y  |

`num++` 和 `++num` 的区别，前者是先赋值再自增，后者是先自增再赋值。

**操作运算符**

| 运算符 |   说明   |      示例      |      等价于       |
| :----: | :------: | :------------: | :---------------: |
|   +=   | 递增赋值 | x = 3;x += 4;  | x = 3;x = x + 4;  |
|   -=   | 递减赋值 | x = 10;x -= 9; | x = 10;x = x - 9; |
|   *=   | 乘法赋值 | x = 8;x * = 7; | x = 8;x  = x * 7; |
|   /=   | 除法赋值 | x = 8;x /= 7;  | x = 8;x = x / 7;  |
|   %=   | 取余赋值 | x = 8;x %= 7;  |  x = 8;x = x%7;   |

**比较运算符**

| 运算符 |       说明       |  示例   |
| :----: | :--------------: | :-----: |
|   <    |       小于       |   8<6   |
|   >    |       大于       |  10>7   |
|   <=   |     小于等于     | 10<=11  |
|   >=   |     大于等于     | 12>=32  |
|  ===   | 比较值和类型相等 | 8===8.0 |
|  !==   |  值和类型不相等  | 8!==8.0 |

**逻辑运算符**

| 运算符 | 示例   | 说明                        |
| ------ | ------ | --------------------------- |
| &&     | x&&y   | 逻辑与                      |
| \|\|   | x\|\|y | 逻辑或                      |
|        | x!y    | 逻辑非                      |
| ? :    | z?x:y  | 当z为true时返回x，否则返回y |
| &      | x&y    | 按位与                      |
| \|     | x\|y   | 按位或                      |
| ^      | x^y    | 按位异或                    |
| ==     | x==y   | 相等                        |
| !=     | x!=y   | 不相等                      |

**2、数组**

**创建数组**

```javascript
var myArray = new Array(1, 2, 3, 4, 5); // 创建数组同时赋值
var myArray = [1, 2, 3, 4, 5];          // 直接输入一个数组
```

**数组方法**

```javascript
obj.length          //数组的大小
obj.push(ele)       //尾部追加元素
obj.pop()           //尾部获取一个元素
obj.unshift(ele)    //头部插入元素
obj.shift()         //头部移除元素
obj.splice(start, deleteCount, value, ...)  //插入、删除或替换数组的元素
                    obj.splice(n,0,val)     //指定位置插入元素
                    obj.splice(n,1,val)     //指定位置替换元素
                    obj.splice(n,1)         //指定位置删除元素
obj.slice()        //切片
obj.reverse()      //反转
obj.join(sep)       //将数组元素连接起来以构建一个字符串
obj.concat(val,..)  //连接数组
obj.sort()         //对数组元素进行排序
```

**4、字符串**

**创建字符串**

```javascript
var surname = 'cheng';
var name = 'cuichao'
var fullName = surname + name  //拼接字符串
```

**字符串方法**

```javascript
obj.length                           //长度
obj.trim()                           //移除空白
obj.trimLeft()
obj.trimRight)
obj.charAt(n)                        //返回字符串中的第n个字符
obj.concat(value, ...)               //拼接
obj.indexOf(substring,start)         //子序列位置
obj.lastIndexOf(substring,start)     //子序列位置
obj.substring(from, to)              //根据索引获取子序列
obj.slice(start, end)                //切片
obj.toLowerCase()                    //大写
obj.toUpperCase()                    //小写
obj.split(delimiter, limit)          //分割
obj.search(regexp)                   //从头开始匹配，返回匹配成功的第一个位置(g无效)
obj.match(regexp)                    //全局搜索，如果正则中有g表示找到全部，否则只找到第一个。
obj.replace(regexp, replacement)     //替换，正则中有g则替换所有，否则只替换第一个匹配项，
                                     //$数字：匹配的第n个组内容；
                                     //$&：当前匹配的内容；
                                     //$`：位于匹配子串左侧的文本；
                                     //$'：位于匹配子串右侧的文本
                                     //$$：直接量$符号
```

**5、类型的转换**

**转换成字符串**

```javascript
numberObj.toString()		//将数字转换成字符串，可以携带一个参数，输出对应进制的值。
String(obj)					//将所有类型转换成字符串
```

**转换成数值类型**

`Number()` 可以把任意值转换成数值，如果要转换的字符串中有一个不是数值的字符，返回 NaN（not a number）

`parseInt()` 把字符串转换成整数，第二个参数可以加进制。

`parseFloat()` 把字符串转换成浮点数，不可以传第二个参数。

**转换成布尔类型**

 `Boolean()` null，undefined，NaN，0，""，[] 都是`false`