# HTML5

> HTML5的新增特性主要是针对于以前的不足，增加了一些新的标签、新的表单和新的表单属性等。

### 新增的语义化标签**（以下都是都是块级元素）**

- `<header>`：头部标签
- `<nav>`：导航标签
- `<article>`：内容标签
- `<section>`：定义文档某个独立部分（至少要包含一个h1~h6）
- `<aside>`：侧边栏标签
- `<footer>`：尾部标签
- `<figure>`：标签规定的独立内容（如：图像、图标、照片、代码等）

### 新增的多媒体标签

- 音频：`<audio>`

  | 属性                                                         | 值                     | 描述                                                        |
  | ------------------------------------------------------------ | ---------------------- | ----------------------------------------------------------- |
  | [autoplay](https://www.runoob.com/tags/att-audio-autoplay.html) | autoplay               | 如果出现该属性，则音频在就绪后马上播放。                    |
  | [controls](https://www.runoob.com/tags/att-audio-controls.html) | controls               | 如果出现该属性，则向用户显示音频控件（比如播放/暂停按钮）。 |
  | [loop](https://www.runoob.com/tags/att-audio-loop.html)      | loop                   | 如果出现该属性，则每当音频结束时重新开始播放。              |
  | [muted](https://www.runoob.com/tags/att-audio-muted.html)    | muted                  | 如果出现该属性，则音频输出为静音。                          |
  | [preload](https://www.runoob.com/tags/att-audio-preload.html) | auto，metadata  ，none | 规定当网页加载时，音频是否默认被加载以及如何被加载。        |
  | [src](https://www.runoob.com/tags/att-audio-src.html)        | *URL*                  | 规定音频文件的 URL。                                        |

- 视频：`<video>`

  | 属性                                                         | 值                   | 描述                                                         |
  | ------------------------------------------------------------ | -------------------- | ------------------------------------------------------------ |
  | [autoplay](https://www.runoob.com/tags/att-video-autoplay.html) | autoplay             | 如果出现该属性，则视频在就绪后马上播放。                     |
  | [controls](https://www.runoob.com/tags/att-video-controls.html) | controls             | 如果出现该属性，则向用户显示控件，比如播放按钮。             |
  | [height](https://www.runoob.com/tags/att-video-height.html)  | *pixels*             | 设置视频播放器的高度。                                       |
  | [loop](https://www.runoob.com/tags/att-video-loop.html)      | loop                 | 如果出现该属性，则当媒介文件完成播放后再次开始播放。         |
  | [muted](https://www.runoob.com/tags/att-video-muted.html)    | muted                | 如果出现该属性，视频的音频输出为静音。                       |
  | [poster](https://www.runoob.com/tags/att-video-poster.html)  | *URL*                | 规定视频正在下载时显示的图像，直到用户点击播放按钮。         |
  | [preload](https://www.runoob.com/tags/att-video-preload.html) | auto  metadata  none | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
  | [src](https://www.runoob.com/tags/att-video-src.html)        | *URL*                | 要播放的视频的 URL。                                         |
  | [width](https://www.runoob.com/tags/att-video-width.html)    | *pixels*             | 设置视频播放器的宽度。                                       |

### 新增的input类型

`<input type="email">` `<input type="url">` `<input type="date">` `<input type="time">`

`<input type="month">` `<input type="week">` `<input type="number">` 

`<input type="tel">（电话）` `<input type="search">` `<input type="color">`

- 验证的时候必须添加  `<form>`  表单域，提交即验证。

### 新增的表单属性

| 属性         | 值        | 说明                                                         |
| ------------ | --------- | ------------------------------------------------------------ |
| required     | required  | required 属性是一个 boolean 属性。required 属性规定必须在提交之前填写输入域（不能为空）。 |
| placeholder  | 提示文本  | placeholder 属性提供一种提示（hint），描述输入域所期待的值。简短的提示在用户输入值前会显示在输入域上。 |
| autofocus    | autofocus | autofocus 属性是一个布尔属性。autofocus 属性规定在页面加载时，域自动地获得焦点。 |
| autocomplete | off/on    | autocomplete 属性规定 form 或 input 域应该拥有自动完成功能。当用户在自动完成域中开始输入时，浏览器应该在该域中显示填写的选项。 |
| multiple     | multiple  | multiple 属性是一个 boolean 属性。multiple 属性规定  `<input>`  元素中可选择多个值。可以多选文件提交。 |
| min、max     | 数值      | min、max 和 step 属性用于为包含数字或日期的 input 类型规定限定（约束）。 |

