# html基础
- html标签:
作用: 网页的根节点
- head标签:
 作用: 存放 `title`;`meta`;`style`;`script`;`link`等标签.
- title标签:
作用: 让页面拥有一个属于自己的标题
- body标签:
作用: 页面主题, 存放网页要展示的标签`p`;`h`;`a`;`img`等
> 在`body`中多个空格会当作一个空格处理

`meta` 标签:
设置网页的元数据,不同的属性会使`meta`标签具备不同的功能.
- 用于设置关键字`meta name="keywords" content="xxx"/`
- 用于设置描述信息`meta name="description" content="xxx/`

## 常用标签
- 段落标签 `p` `p`标签会自动换行
- 标题标签 `h` 一共有6级标题  `h1` `h2` `h3` `h4` `h5` `h6`
(一级标签只能出现一次)

- 水平线标签 `hr`(分割线)
- 换行标签 `br` 自动换行
- `div` `span` 没有语义  `div`会自动换行  `span`不自动换行
### 文本格式化标签
- 斜体`em` /加粗`strong` `em`用于表示一段内容中的着重点, `strong`用于表示一个内容的重要性.
- 斜体`i`/加粗`b` 都没有语义
- 上标`sup`/下标`sub`,如`5 sup 2 sup`  `H sub 2 /sub 0`
- 下划线`ins` /删除线`del`
- 转义字符
    - 空格 `&#bsp;` `&#160;`
    - 小于号 `&lt;` `&#60;` 
    - 大于号 `&gt;` `&#62;`
### 图像标签 
 `img src="图像url alt="""`
`src`属性用于指定图像文件的路径和文件名 
 `alt`属性用于指定图片未找到时，显示的内容。
**图像引入路径**
- 相对路径
    - 相对当前文件
    - 同一级目录下,输入图像文件的名称`img src="avatar.jpg"`
    - 图像文件位于当前文件的下一级目录: 输入文件夹名和文件名,之间用`/`/隔开
    - 图像文件位于当前文件的上一级目录: 在文件夹之前加`../`,如果两级,须要使用`../../`,以此类推.
- 绝对路径
    - 本地绝对路径 `D:/web/img/avatar.jpg/`
    - 网络路径 `网络地址`
- 超链接标签
> `a href="跳转目标" target="目标窗口的弹出方式" /a`
target:
- `_self` 为在当前窗口打开(默认值)
- `_blank` 为在新窗口打开

### 列表标签
#### 无序列表 `ul`
><ul>
	<li>列表项1</li>
	<li>列表项2</li>
	<li>列表项3</li>
	......
</ul>


注意
- 列表具有严格的嵌套关系
- `ul`中只能嵌套`li`,直接在`ul`中输入其他标签或者文字的做法是不被允许的;
- `li`之间相当于一个容器,可以容纳所有y元素;
- 无序列表会带有自己的样式属性,一般不用
#### 有序列表 `ol`

><ol>
	<li>列表项1</li>
	<li>列表项2</li>
	<li>列表项3</li>
	......
</ol>

#### 自定义列表

><dl>
	<dt>名词1</dt>
	<dd>名词1解释1</dd>
	<dd>名词1解释2</dd>
	...
	<dt>名词2</dt>
	<dd>名词2解释1</dd>
	<dd>名词2解释2</dd>
	...
</dl>

### html新增标签 

#### 多媒体标签
 (视频)`<video src="../素材/小手拍拍.mp4" width="400" muted height="400" controls autoplay></video>`
 - `autoplay` 自动播放
 - `controls` 是否显示默认播放控件
 - `loop` 循环播放
 - `preload` 预加载,同时设置`autoplay`,此属性失效
 - `width` 设置播放窗口宽度
 - `height` 设置窗口播放的高度 
 - `muted` 静音 开启静音自动播放就可以生效

(音频)`<audio src="../素材/小手拍拍.mp3" loop autoplay controls></audio>`

#### 布局标签
- `section`:表示页面中的一个内容区块,比如章节、页眉、页脚或页面的其他部分。可以和`h1`、`h2`……等元素结合起来使用，表示文档结构。
- `article`:表示页面中一块与上下文不相关的独立内容。比如一篇文章。
- `aside`:表示一个页面的一部分，它的内容跟这个页面的其它内容的关联性不强，或者是没有关联，单独存在。`aside`元素通常显示成侧边栏`(sidebar)`或一些插入补充内容。通常用来在侧边栏显示一些定义，比如目录、索引、术语表等；也可以用来显示相关的广告宣传，作者的介绍，相关链接，当前页内容简介等。
- `header`: 表示页面中一个内容区块或真个页面的标题。
- `hgroup`: 表示对整个页面或页面中的一个内容区块的标题进行组合。
- `footer`: 表示整个页面或页面中一个内容区块的脚注。一般来说，他会包含创作者的姓名、创作日期以及创作者的联系信息。
- `nav`:表示页面中导航链接的部分。
- `figure`:表示一段独立的流内容，一般表示文档主体流内容中的一个独立单元。



### 表格
```html
<table>
	<tr>
		<th>表头内的文字</th>
		...
	</tr>
	<tr>
		<td>单元格内的文字</td>
		...
	</tr>
	...
</table>

```

- `<table></table>`用于定义一个表格。
- `<tr></tr>` 用于定义表格中的一行，必须嵌套在`<table></table>`标签中，在` <table></table>`中包含几对`<tr></tr>`，就有几行表格.就有几行表格。
- `<td></td>` `用于定义表格中的单元格，必须嵌套在标签中，一对 中包含几对`，就表示该行中有多少列（或多少个单元格）。
- `<th></th>' 表头一般位于表格的第一行或第一列，必须嵌套在标签中。

### 表格属性
 
![](../img/表格属性.png)

### 合并单元格
- rowspan 单元格所占行
- colspan 单元格所占列
```html
<table backgroundcolor="orange" cellspacing="20" cellpadding="10" border="5">
	<!-- 表格标题 -->
	<caption>
		课程表
	</caption>
	<tr>
		<th>周一</th>
		<th>周二</th>
		<th>周三</th>
		<th>周四</th>
	</tr>
	<tr>
		<td rowspan="2">语文</td>
		<td colspan="2">数学</td>
		<!-- <td>语文</td> -->
		<td>体育</td>
	</tr>
	<tr>
		<!-- <td>语文</td> -->
		<td>数学</td>
		<td>语文</td>
		<td>体育</td>
	</tr>
</table>
```

### 表单
在 HTML 中，一个完整的表单通常由表单控件（也称为表单元素）、提示信息和表单域 3 个部分构成。
- 表单控件:
​ 包含了具体的表单功能项，如单行文本输入框、密码输入框、复选框、提交按钮、重置按钮等。
- 提示信息:
一个表单中通常还需要包含一些说明性的文字，提示用户进行填写和操作。
- 表单域:
相当于一个容器，用来容纳所有的表单控件和提示信息，可以通过他定义处理表单数据所用程序的 url 地址，以及数据提交到服务器的方法。如果不定义表单域，表单中的数据就无法传送到后台服务器。

#### `input`控件

![](../img/input控件.png)

新增input type类型
- `email` 限制用户输入必须为Email类型
- `tel` 手机号码 (移动端支持)
- `url` 限制用户输入必须为url类型
- `number` 只能输入数字
- `search` 具有搜索意义的表单属性
- `range` 范围 滑动条
- `color` 拾色器
- `time` 时间
- `date` 选取日、月、年
- `datetime` 选取时间、日、月、年(UTC时间)(移动端支持)
- `datetime-local` 选取时间、日、月、年（本地时间）
- `month` 选取月、年
- `week` 选取周和年

### 新增表单元素(标签)
- `datalist` 数据列表 自动补齐,常与`input`标签配合使用
```html
<input type=”text” list=”data”>
	<datalist id=”data”>
	<option>男</option>
	<option>女</option>
	<option>不详</option> 
</datalist>
```
- `meter` 用来表示规定范围内的数量值，如磁盘使用量比例饿、关键词匹配程度等。需要注意的是：`meter`不可以用来标记那些没有已知范围的任意值，如重量、高度，除非已经设定了它们值的范围。
```html
<meter value="81" min="0" max="100" low="60" high="80"></meter>
```

- `progress`进度条
```html
<progress value="22" max="100"></progress>
```


#### `label`标签
作用：用于绑定一个表单元素, 当点击 label 标签的时候, 被绑定的表单元素就会获得输入焦点。

#### textaea 控件(文本域)
如果需要输入大量的信息，就需要用到`<textarea></textarea>`标签。通过 `textarea` 控件可以轻松地创建多行文本输入框，其基本语法格式：
```html
<textarea cols="每行中的字符数" rows="显示的行数">
  文本内容
</textarea>
```
#### 下拉菜单
使用 `<select></select>` 控件定义下拉菜单的基本语法格式:
```html
<select>
	<option>选项1</option>
	<option>选项2</option>
	<option>选项3</option>
	...
</select>

```
注意:
- `<select></select>`中至少应包含一对`<option></option>`。
- 在 `<option></option>` 中定义 `selected="selected`"属性时，当前项即为默认选中项。可以简写为`selected`.


#### 表单域
```html
<form action="url地址" method="提交方式" name="表单名称">
	各种表单控件
</form>
```

### 表单补充属性
- `fieldest` 可以实现表单分组(一个框), `legend` 可以给框起名字
- `get` 提交
    - 参数被放到地址提交，比如: /D:/abc?username=张三&pwd=123&sex=0&experience=0
    - 不安全
    - 地址栏拼接的参数长度有限,一般是<4k
    - 一般用于获取数据
- `post` 提交
    - 地址栏不显示提交内容,再请求体显示
    - 相对安全
    - 提交的数据量没有上限
    - 一般用于提交保存数据
- `disabled`禁用
- `readonly`只读
- `placeholder` 占位符提供可描述输入字段预期值的提示信息
- `autofocus` 元素应该自动获得焦点
- `multiple` 多文件上传 
#### 新增表单属性
- `autocomplete` 自动完成,用于表单元素,也可用于表单自身(on/off),是否保存用户输入值 默认为on，关闭提示选择off
- `form` 指定表单项属于哪个form，处理复杂表单时会需要 一般一个页面只有一个form
- `novalidate` 关闭验证.可用于form标签
- `required` 正则表达式 验证表单
- `formaction` 主要应用于表单内某元素提交地址与整个表单提交地址不同，进行单个地址覆盖
	- 如`<input type="submit" formaction="xxx.action">`


```html
<!-- action 是当前表单提交的地址 -->
<form action="www.bufanui.com" method="get">
	<fieldset>
		<legend>基本信息</legend>
		用户名: <input type="text" readonly name="username" value="张三" /> <br />
		曾用名： <input type="text" disabled name="oldname" value="张小三" /><br />
		密码: <input type="password" name="pwd" /> <br />
		性别:
		<label> 男: <input type="radio" name="sex" value="0" /> </label>
		<label> 女: <input type="radio" checked name="sex" value="1" /> <br /> </label>
	</fieldset>

	<fieldset>
		<legend>补充信息</legend>
		爱好:
		<label> 篮球: <input type="checkbox" name="like" value="basketball" /> </label>
		<label> 足球: <input type="checkbox" checked name="like" value="football" /> </label>
		<label> 乒乓: <input type="checkbox" name="like" value="pingpang" /><br /> </label>

		工作年龄:
		<select name="experience">
			<option value="0">--无--</option>
			<option value="1">1年</option>
			<option value="2" selected>2~3年</option>
			<option value="3">3~5年</option>
		</select>
		<br />
		上传头像: <input type="file" name="avatar" multiple /> <br />
		个人描述:
		<textarea name="desc" cols="30" rows="4">
    				我对工作有极大地热情,我喜欢写代码!
    			</textarea
		>
		<br />
	</fieldset>

	<input type="submit" value="提交" />
</form>
```

#### 新增表单事件
- `oninput` 用户输入内容时触发,可用于移动端输入字数统计
- `oninvalid` 验证不通过时触发
- `tabindex` (控制`input`标签按`他爸`键获取到焦点的顺序)
```html
姓名: <input type="text" tabIndex="1"> <br>
年龄: <input type="number" tabIndex="3"> <br>
电话: <input type="tel" tabIndex="2"> <br>
地址: <input type="text" tabIndex="4">
```





