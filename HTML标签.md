# HTML标签

### 语法规范

```html
1.HTML标签是由" < > "包围的关键词，例如<html>。

2.HTML标签通常成对出现，例如<html> </html>，我们称为双标签（开始标签和结束标签）。

3.有些特殊标签必须是单个标签，例如 <br />，称为单标签。
```

### 标签关系

双标签关系可以分为两类：包含关系和并列关系。

包含关系：

```html
<head>
	<title></title>
</head>
```

并列关系：

```html
<head> </head>
<body> </body>
```

### HTML页面骨架：

```html
<html>			//根标签
    <head>		//文档头部
        <title>标题</title>		//文档标题
    </head>
    <body>		//文档主体
        这是body
    </body>
</html>
```

### <!DOCTYPE>

文档类型声明，作用是告诉浏览器使用哪种HTML版本来显示网页。

例：

```html
<!DOCTYPE html>
```

即当前页面采取的是HTML5版本来显示网页。

> !DOCTYPE 声明必须位于文档最前面，处在html标签之前。
>
> !DOCTYPE 不是一个HTML标签，是文档类型声明标签。

###  lang语言种类

用来定义当前文档显示的语言。

例：

```html
<html lang="en">
<html lang="zh-CN">
```

"en"定义语言为英语，"zh-CN"定义语言为中文。

但对于文档显示来说，定义成en的文档也可以显示中文，定义成zh-CN的文档也可以显示英文，这个属性对浏览器和搜索引擎还是有作用的。

### 字符集

在<head>标签中，可以通过<meta>标签的charset属性来规定HTML文档应该使用哪种字符编码。

**写在head里，必须有。**

例：

```html
<meta charset="UTF-8" />
```

charset常用值有：GB2312、BIG5、GBK和UTF-8，其中**UTF-8**也被称为**万国码**，基本包含了全世界所有国家需要用到的字符。

### 标题标签

> 共有 <h1> -- <h6> 六个等级的网页标题

例：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>标题标签</title>
	</head>
	<body>
		<h1>标题标签</h1>
		<h2>标题标签</h2>
		<h3>标题标签</h3>
		<h4>标题标签</h4>
		<h5>标题标签</h5>
		<h6>标题标签</h6>
		标题标签
	</body>
</html>
```

显示效果：

> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8">
> 		<title>标题标签</title>
> 	</head>
> 	<body>
> 		<h1>标题标签</h1>
> 		<h2>标题标签</h2>
> 		<h3>标题标签</h3>
> 		<h4>标题标签</h4>
> 		<h5>标题标签</h5>
> 		<h6>标题标签</h6>
> 		标题标签
> 	</body>
> </html>

### 段落和换行标签

- #### 段落标签

```html
<body>
<p>一个段落</p>				//paragraph缩写
<p>又是一个段落</p>
</body>
```

##### 特点

1. 文本在一个段落中会根据浏览器窗口的大小自动换行。
2. 段落和段落之间保有空隙。

- #### 换行标签

```html
<br />				  	  //break的缩写
```

##### 特点

1. br 是个单标签
2. br 标签只是简单地开始新的一行，跟段落不一样，段落之间会插入一些垂直的间距。

```html
<hr> 
```

**特点**

元素在文档中生成一条水平分割线，表示文本中主题的变化（例如话题或场景的改变）。一般就是一条水平的直线。

### 文本格式化标签

**作用：为文字设置粗体、斜体、下划线等效果，突出重要性。**

| 语义   | 标签                         | 说明               |
| ------ | ---------------------------- | ------------------ |
| 加粗   | <strong></strong>或者<b></b> | 更推荐使用<strong> |
| 倾斜   | <em></em>或者<i></i>         | 更推荐使用<em>     |
| 删除线 | <del></del>或者<s></s>       | 更推荐使用<del>    |
| 下划线 | <ins></ins>或者<u></u>       | 更推荐使用<ins>    |

例：

```html
		<strong>标题</strong>标签 <br />
		<b>标题</b>标签			 <br />
		<em>倾斜一波</em>		 <br />
		<del>删了删了</del>		 <br />
		<ins>下划线下划线</ins>	 <br />
		<strong><em>加粗然后倾斜！</strong></em>	<br />
		<strong><del>加粗然后删掉！</del></strong>	<br />
```

显示效果：

> <strong>标题</strong>标签 <br />
> 		<b>标题</b>标签			 <br />
> 		<em>倾斜一波</em>		 <br />
> 		<del>删了删了</del>		 <br />
> 		<ins>下划线下划线</ins>	 <br />
> 		<strong><em>加粗然后倾斜！</strong></em>	<br />
> 		<strong><del>加粗然后删掉！</del></strong>	<br />

# div 和 span 标签

<strong>这两个标签是没有语义的，它们只是一个用来装内容的容器。</strong>

**div是division的缩写，表示分割、分区。span意为跨度、跨距。**

**特点：**

- div作为块级元素，用来布局，但是一行只能放一个div。

- span作为行内元素，用来布局，一行可以放多个span。

  > **警告：**`<div>` 非常便利但容易被滥用。由于它们没有语义值，会使 HTML 代码变得混乱。要小心使用，只有在没有更好的语义方案时才选择它，而且要尽可能少用， 否则文档的升级和维护工作会非常困难。

# 图像标签

> <img>标签用于定义HTML页面中的图像。

例：

```html
<img src="图像/URL" />
```

**src：**是<img>标签的必须**属性**，它用于指定图像文件的**路径和文件名**。

| 属性   | 属性值   | 说明                                     |
| ------ | -------- | ---------------------------------------- |
| src    | 图片路径 | 必须属性                                 |
| alt    | 文本     | 替换文本。图像显示不出来的时候用文字替换 |
| title  | 文本     | 提示文本。鼠标放到图像上，显示的文字     |
| width  | 像素     | 设置图像的宽度                           |
| height | 像素     | 设置图像的高度                           |
| border | 像素     | 设置图像的边框粗细                       |

例：

```html
<h4> 图像标签的使用： </h4>
<img src="割绳子壁纸.jpg" />
```

![image-20211112174509774](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211112174509774.png)

例：

```html
<h4> 来个alt的示范 </h4>
<img src="名字输错了或者路径不对了.jpg" alt="割绳子" />
```

<img src="C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211112174104085.png" alt="image-20211112174104085" style="zoom:50%;" />

例：

```html
<h4> 来个title的示范</h4>
<img src="割绳子壁纸.jpg" title="鼠标移上来显示文字" />
```

![image-20211112174839592](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211112174839592.png)

例：

```html
<h4> 来个width设置宽度的示范</h4>
<img src="割绳子壁纸.jpg" width="100" />	//单位是像素，也可以用百分比（如width=10%）
```

![image-20211112175602497](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211112175602497.png)

> 设置图片大小时，通常设定宽度和高度中的一个即可，另一项会等比例改变。

例：

```html
<h4> 来个border给图片添加边框的示范</h4>
<img src="割绳子壁纸.jpg" width="100" border="20" />
```

![image-20211112180057154](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211112180057154.png)

# 超链接标签

#### **1.语法格式**

```html
<a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像 </a>
```

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| href   | 用于指定链接目标的url地址（必须属性）                        |
| target | 用于指定链接页面的打开方式，其中 **_self**为**默认值**， **_blank**为在新窗口中打开方式 |

#### **2.链接分类**

##### **①外部链接**

例：

```html
    <h4>外部链接</h4>
    <a href="http://www.baidu.com">百度</a>
```

网页显示：

![image-20211114173118099](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211114173118099.png)

点击“百度” **当前窗口**就会跳转到http://www.baidu.com	**“http://”一定要写**

如果

```html
<a href="http://www.baidu.com" target="_blank">百度</a>
```

就会**新窗口**打开链接

#####  ②内部链接

网站内部页面之间的相互连接，直接链接内部页面名称即可。

例：

当02-第一个页面.html和此html在同一个文件夹时

```html
<a href="02-第一个页面.html"> 02-第一个页面 </a>
```

会打开02-第一个页面.html

##### **③空链接**

暂时没有确定链接目标时，用“#”代替链接地址。

例：

```html
<a href="#"> 还没确定跳转到哪里 </a>
```

##### ④下载链接

如果href里面地址是一个文件或者压缩包，会下载这个文件；地址链接的是 文件.exe或者.zip等形式

例：

```html
<a href="nb.exe"> 下载nb.exe </a>
```

##### ⑤网页元素链接

 给网页元素（如：文本、图像、表格等）添加超链接，点击进行跳转。

例：

```html
<h4>网页元素链接</h4>
<a href="http://www.baidu.com"><img src="割绳子壁纸.jpg" /></a>
```

点击图片就会跳转到百度

##### ⑥锚点链接

点击链接会**定位**到当前页面的某个区域。

- 在点击的超链接的href属性中，设置属性值为 **#名字** 的形式
- 找到想要定位到的标签，里面添加 **id="名字"**

例：

```html
<a href="#b"> 点这里定位到b </a>
...
<h3 id="b">定位到我了</h3><br />
```

点击 超链接“点这里定位到b”，就会定位到h3标题“定位到我了”。

# 表格标签

#### 1.语法格式

```html
<table>						//定义表格的标签
        <tr>				//定义表格中的行
            <th>xxx</th> <th>xxx</th> <th>xxx</th> //表头，文本内容加粗居中显示。
            <td>xxx</td> <td>xxx</td> <td>xxx</td> //table data，定义表格中的单元格         </tr>
        ...
</table>
```

例：

```html
<table>
        <tr>  <td>姓名</td> <td>学号</td> <td>班级</td>  </tr>
        <tr>  <td>张三</td> <td>123</td> <td>1班</td>  </tr> 
   		<tr>  <td>李四</td> <td>321</td> <td>1班</td>  </tr>  
</table>
```

结果：

![image-20211114194140299](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211114194140299.png)

#### 2.表格属性

实际开发中通过CSS设置。

![image-20211114194334453](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211114194334453.png)

写到table标签里面

#### 3.表格结构标签

thead标签	头部区域（包含 th tr）

tbody标签	主体区域（包含 td）

#### 4.合并单元格

- 跨行合并（上下）：rowspan="个数"

- 跨列合并（左右）：colspan=“个数”

  > 其实不妨理解为这个单元格的大小，即占多少格。

例：

```html
<table align="center" border="1" cellpadding="20" cellspacing="2" width="500">
        <tr>  <th colspan="2">姓名和学号</th> <th>班级</th>   </tr>
        <tr>  <td>张三</td> <td>123</td> <td>1班</td>   </tr>
        <tr>  <td><a href="http://www.baidu.com">百度</a></td> 
              <td><a href="http://www.qq.com">腾讯</a></td> 
              <td><a href="#">未知</a></td> 
        </tr>
</table>
```

结果：

![image-20211114200519918](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211114200519918.png)

# 列表标签

#### 1.无序列表

例：

```html
<h4>喜欢吃什么</h4>
    <ul>
        <li>苹果</li>
        <li>西瓜</li>
        <li>桃子</li>
    </ul>
```

结果：

![image-20211115081912652](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115081912652.png)

- **ul** 与**/ul**标签中只能嵌套 **li**与**/li**标签，不允许出现其他标签； **li**与**/li** 之间没有这种禁止。

#### 2.有序列表

例：

```html
<h4>喜欢吃什么</h4>
    <ol>
        <li>苹果</li>
        <li>西瓜</li>
        <li>桃子</li>
    </ol>
```

结果：

![image-20211115082333065](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115082333065.png)

注意事项和无序列表一样。

#### 3.自定义列表

例：

```html
    <dl>
        <dt>关注我们</dt>
        <dd>新浪微博</dd>
        <dd>官方微信</dd>
        <dd>联系我们</dd>
    </dl>
```

结果：

![image-20211115083117344](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115083117344.png)

- dl 和 /dl 之间只能包含dt和dd

# 表单标签

组成部分：表单域、表单控件、提示信息。

常见于注册页面。

#### 1.表单域

form标签定于表单域。

语法格式：

```html
<form action="url地址" method="提交方式" name="表单域名称">
        ...各种表单元素控件
</form>
```

| 属性   | 属性值   | 作用                                               |
| ------ | -------- | -------------------------------------------------- |
| action | url地址  | 用于指定接收并处理表单数据的服务器程序的url地址    |
| method | get/post | 用于设置表单数据的提交方式，其取值为get或post      |
| name   | 名称     | 用于指定表单的名称，以区分同一个页面中的多个表单域 |

#### 2.表单控件

#### input

```html
<input type="属性值" />
```

![image-20211115084850693](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115084850693.png)

除了type属性之外，input标签还有其他属性：

![image-20211115090056586](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115090056586.png)

- name和value是每个表单元素都有的属性值，主要给后台人员使用。

- **单选按钮radio和复选框checkbox必须有相同的name值。**
- name的主要作用是区别不同的表单。
- checked可以使单选按钮和复选按钮有默认选中状态。

# label标签

用于绑定一个表单元素，当点击label标签内的文本时，浏览器就会自动将焦点（光标）转到或者选择对应的表单元素上。

例：

```html
<label for ="nb">测试</label>
<input type="text" name="nbb" id="nb">
<input type="submit">
```

结果：

![image-20211115185948935](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115185948935.png)

点击“测试”也可以输入文本。

> lable标签的**for属性**应当与相关元素的**id属性相同**。

# 下拉标签select

多个选项供用户选择。

例：

```html
    <select>
        <option>1</option>
        <option>2</option>
        <option selected="selected">3</option>
    </select>
```

结果：

![image-20211115195346081](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115195346081.png)

在option中定义 selected="selected"，当前项即为默认选中项。

# 文本域标签textarea

当需要输入的内容较多而不能使用text标签时使用textarea。

例：

```html
test:<textarea>默认的显示字段</textarea>
```

结果：

![image-20211115195736024](C:\Users\街灯\AppData\Roaming\Typora\typora-user-images\image-20211115195736024.png)

