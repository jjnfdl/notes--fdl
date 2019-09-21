# css基础
## css书写位置
- 外部引入
`<link rel="stylesheet" href="header.css">`
- 内部书写
写在`head`标签内部 ,用`style`标签包裹
- 行内样式
属性名:属性值; 属性名:属性值; 
   外部样式 用的最多 可以复用
   行内样式 少用 样式结构 严重耦合    能复用
   内部样式 平常演示代码时 经常用    能复用


## css选择器
- `*p` 选中所有的`p`标签
- `*`(通配符) 选中所有标签
设置样式    选中这个标签   设置 样式属性 即可 -->
id  唯一标识 (身份证)
class  类名 (给标签分类)
- `class`选择器 (类名选择器)
  用的最多,可以重复
- `id`选择器
  不重复 

## 复杂选择器
- 后代选择器  父类加空格
- 交集选择器  不加空格
- 并集选择器  用`,`隔开
- 子代选择器  父类类名>子类类名
- 兄弟选择器  类名+(选中下一个)


## css层叠性和权重
- 层叠 设置的所有样式共同作用的效果
- 样式冲突时    选择器权重高的  生效
- 权重大小  行内样式(1000)>id选择器(100)>class选择器(10)>标签选择器(1)>通配符
    - 复杂选择器权重  各种选择器权重累加


## 继承性

子类会继承父类样式
`a`标签不能继承父类设置的字体颜色
[css继承性](https://www.cnblogs.com/thislbq/p/5882105.html)

## css常见单位
- 像素单位 `px`
- `em` 基于当前字体的倍数
- 百分比  相对于父类的百分比
- 颜色单位 预定义 `red` `green` `blue` `贫困`
  十六进制 `#ffffff`(白色) #dd5044    rgb(221,80,68)
  rgba的a表示透明度


## css常见属性

|属性名称|属性作用|值|  
|----|---|---|
|width/heigth|宽高|px;百分比;emdeng|
|background-color|背景颜色|color|
|color|字体颜色|color|
|font-size|字体大小|px;em等|
|text-align|文字对齐方式|center;left;right|
|text-intend|首行缩进|px;em等|
|font-family|字体|中文英文都能识别|
|font-weight|字体加粗|100-900;(加粗)700-900/bolder lighter(变细); normal(正常)|
|font-style|字体样式|ltalic(西斜体);normal|
|line-height|行高|单位:px/倍数/百分比; 设置文字的行间距;单行文本垂直局中:行高=父类盒子高度|
|font|字体缩写|`font:italic border 20px/1.2 宋体|

## 标签表现形式
- 块状标签:独占一行，宽高有效。
比如:`div` `p` `h1~h6` `form    ` `table` `hr` `br` `ul>li` `ol>li` `dl>dt>dd`
- 行内块标签:可以同一行显示，宽高有效。
比如:`input` `select` `img` `button`
- 行内标签:可以同一行显示，但是宽高无效。
比如:`a` `span` `strong` `del` `ins` `em` `i` `b`
- `display`:可以修改元素(标签)的性质 
    - `block`:设置元素为块元素
    - `inline`:设置元素为行内元素
    - `inline-block`:设置元素为行内块元素
    - 转换的必要性：比如可以把`a`标签转换为块状元素，设置宽高，使用户可点击的区域增大，进而实现一个按钮的样式。

## 背景图片属性

|属性名称|属性作用|值|
|-------|-----|----|
|background-color|背景图片颜色|color|
|background-image|背景图片|url()|
|background-repeat|平铺方式|repeat(重叠);no-repeat(不平铺);repeat-x(x轴方向平铺);repeat-y(y轴方向平铺)|
|background-position|图片位置|left;right;top;bottom;center|
|background-attachment|背景滚动|scroll(滚动);fixed(固定)|
|background|简写(顺序不能错)|background:green url() no-repeat center center fixed;|

## css3新增属性

- box-shadow（阴影效果）
- border-color（为边框设置多种颜色）- border-image（图片边框）
- text-shadow（文本阴影）
- text-overflow（文本截断） 
- word-wrap（自动换行）
- border-radius（圆角边框）
- opacity（透明度）
- box-sizing（控制盒模型的组成模式）
- resize（元素缩放）
- outline（外边框）
- background-size（指定背景图片尺寸）
- background-origin（指定背景图片从哪里开始显示）
- background-clip（指定背景图片从什么位置开始裁剪）
- background（为一个元素指定多个背景）
- hsl（通过色调、饱和度、亮度来指定颜色颜色值）
- hsla（在hsl的基础上增加透明度设置）
- rgba（基于rgb设置颜色，a设置透明度）
- 给图片加黑白滤镜
```
-webkit-filter: grayscale(100%); 
-moz-filter: grayscale(100%); 
-ms-filter: grayscale(100%); 
-o-filter: grayscale(100%); 
filter: grayscale(100%); 
filter: gray;
```