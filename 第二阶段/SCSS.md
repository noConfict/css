

# 一.scss的由来

## 1.css的特点

语法不够强大，没有合理的代码复用机制，导致代码难以维护我们可以使用动态样式语言，赋予css新的特性常见的动态样式语言1.scss,是sass的升级版。scss的语法就是css和js的结合体2.stylus3.less

## 2.什么是scss

scss是一种强化css的辅助工具他和css和js的十分接近在css的基础上，添加变量，嵌套，混合，导入，函数，指令等高级功能这些功能让css更加的强大且优雅

## 3.scss运行的原理

scss运行在后台，把scss文件转换成css文件传递给前台，让浏览器运行css文件我们安装的软件，就是把scss文件转换成css文件

## 4.把scss转换成css

### ①单文件转换

node-sass  要转换的scss文件   要转换成的css文件node-sass  scss/1.scss  css/1.css 

### ②多文件转换

转换一个文件夹内所有的文件node-sass  scss文件夹  -o  css文件夹

### ③单文件监听

黑窗口打开监听，在scss文件按ctrl+S. 自动转换为cssnode-sass  -w  scss文件  css文件

### ④多文件监听

node-sass  -w  scss文件夹  -o  css文件夹  

# 二.scss基础语法

## 1.变量

以$开头定义变量，用:号赋值变量的命名规则基本同选择器包含数字，字母，-  _不能用关键字，不能以数字开头可以保存在变量中值1.数值2.颜色3.字符串4.样式属性5.其它变量$my_width:1px;$jd_red:#f10215;$str:"子曾经曰过";$border-style:solid;$my_border:$my_width $border-style $jd_red;

## 2.嵌套

| 在一个选择器内部，嵌套其它选择器和样式，形成后代选择器的关系#content{ color:#123; p{color:#123;}}会生成#content{color:#123;}#content p{color:#123;} |
| ------------------------------------------------------------ |
| 群组的嵌套nav,div,#top{	a{color:#123;}}生成nav a, div a, #top a { color: #123; } |
| 伪类的嵌套需要在被嵌套的伪类之前，添加占位符，不然会自动生成空格a{	color:red;	&:hover{color:green;}} |

## 3.导入

以下划线开头的scss文件，叫做局部scss。局部scss不会生成对应的css文件不以下划线开头的scss文件，叫做全局scss.全局scss会生成对应的css文件一般在全局scss文件中导入很多局部scss文件，最后生成一个css文件_aa.scss 被导入在全局scss中 @import  "aa";

## 4.混合器

把一系列样式封装进一个混合器，哪里调用定义混合器@mixin  混合器名称(参数1，参数2.。。。){  多行样式}调用混合器#d1{@include 混合器名称(参数1，参数2....)}

## 5.继承

一个选择器，可以继承另一个选择器的所有样式#d1{@extend #d2}  #d1会继承#d2的所有样式，最后的显示形式为群组

## 6.运算 +  -  *  /  %

### ①加法

+可以用于字符串的拼接在做字符串拼接的时候，以前面的字符串是否带双引号为准带了，结果就带双引号不带，结构就不带双引号

### ②减法

由于scss的变量中可以包含-。所有系统有些时候分不清是减号还是变量名在减号前后添加空格

### ③除法

在scss中 / 有两个功能1.除法2.做分隔符scss中把以下情况判定为除法1.除法计算式有一端是变量 height:$my_height/2;2.除法计算式被小括号包裹 margin: (500px/2);3.除法计算式属于其他计算式的一部分 padding:5px+8px/2;

# 7.颜色的运算

分段运算 红+红  绿+绿  蓝+蓝最大值是ff，不会超出

# 8.字符串中的插值运算

#{插值}

# 三.scss中的函数

## 1.预定义函数

round($v)floor($v)ceil($v)min($v1,$v2,$v3....)max($v1,$v2,$v3....)random()unquote($str) 去除$str的双引号quote($str) 给$str添加双引号

## 2.自定义函数

@function add($a,$b){  @return $a+$b;}

## 3.if-else

关键字之前添加@@if(){}@else if(){}@else{}