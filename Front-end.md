# 前端开发

[TOC]



## 前端开发语言

* HTML 超文本标记语言 --- 结构

* CSS 层叠样式表 ------------ 样式

* JS(JavaScript) --------------- 行为

| 标准 | 说明                                                         |
| ---- | ------------------------------------------------------------ |
| 结构 | 结构用于对网页元素进行整理的分类，主要是HTML                 |
| 表现 | 表现用于设置网页元素的版式、颜色、大小等外观样式，主要指的是CSS |
| 行为 | 行为是指网页模型的定义及交互的编写，主要是Javascript         |

Web标准提出的最佳体验方案：结构、样式、行为相分离。

结构写到HTML文件中，表现写到CSS文件中，行为写到JavaScript文件中。

----

## HTML超文本标记语言

`<` 标记      `<html>` 标签     `<html> </html>` 标签对 

大多数为双标签，极少数为单标签，如换行标签`<br />` 。

标签的关系：<u>包含关系</u>和<u>并列关系</u> 



### HTML基本结构标签

```html
<html>
    <head>
        <title>第一个页面</title>
    </head>
    <body>
        这是我的第一个页面
    </body>
</html>
```

| 标签名            | 定义       | 说明                                                   |
| ----------------- | ---------- | ------------------------------------------------------ |
| `<html></html>`   | HTML标签   | 页面中最大的标签，根标签                               |
| `<head></head>`   | 文档的头部 | 在head标签中我们必须设置的标签是title                  |
| `<title></title>` | 文档的标题 | 让页面拥有一个属于自己的网页标题                       |
| `<body></body>`   | 文档的主体 | 元素包含文档的所有内容，页面内容基本都是放到body里面的 |

在vscode里可采用输入!或者tab键生成大体框架。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我用vscode创建的第一个页面</title>
</head>
<body>
    我的页面创建出来啦
</body>
</html>
```

`<!DOCTYPE>` 文档类型的声明标签，用来告诉浏览器使用哪种HTML版本显示网页。（要写在最前面）。

`<html lang="en">` 用来定义当前文档的显示语言，`en` 定义为英语，`zh-CH` 定义为中文。

`<meta charset="UTF-8">`UTF-8为万国码，防止乱码情况，一定要写。



### HTML常用标签

#### 标题标签`<h1>`-`<h6>`

```html
<h1>我是一级标题</h1>
```

h是单词head的缩写，意为头部、标题。

<u>标签语义</u>:作为标题使用，并且依据重要性递减。

<u>特点</u>:标题文字会较大较粗，独占一行。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>标题一共六级选</h1>
    <h2>文字加粗一行选</h2>
    <h3>由大到小依次减</h3>
    <h4>从重到轻随之变</h4>
    <h5>语法规范书写后</h5>
    <h6>具体效果刷新见</h6>
</body>
</html>
```



#### 段落和换行标签

 ```html
<p>我是一个段落标签</p>
 ```

<u>标签语义</u>：可以把HTML文档分割为若干段落。

<u>特点</u>：文本在一个段落会根据浏览器窗口大小自行换行。段落与段落之间有空隙。

```html
<br />
```

单词break的缩写，意为打断、换行。

<u>标签语义</u>：强制换行。

<u>特点</u>：`<br />` 是个单标签。`<br />` 只是简单的开始新的一行，跟段落不一样，不会有间隙。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>这是第一段的第一句，<br />这是第一段的第二句。</p>
    <p>这是第二段。</p>>
</body>
</html>
```



 #### 文本格式化标签

文本文字中 **粗体** , *斜体* ，<u>下划线</u>  等效果。

<u>标签语义</u>：突出重要性，比普通文字更重要。

| 语义   | 标签                             |
| ------ | -------------------------------- |
| 加粗   | `<strong></strong>`或者`<b></b>` |
| 倾斜   | `<em></em>`或者`<i></i>`         |
| 删除线 | `<del></del>`或者`<s></s>`       |
| 下划线 | `<ins></ins>`或者`<u></u>`       |

tips:更推荐`<strong>`,`<em>`,`<del>`,`<ins>`语义更强烈。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    我是<strong>加粗</strong>的文字<br />
    我是<em>倾斜</em>的文字<br />
    我是<del>删除线</del>的文字<br />
    我是<ins>下划线</ins>的文字<br />
</body>
</html>
```



#### `<div>`和`<span>`标签

`<div>`和`<span>`是没有语义的，它们是一个盒子，用来装内容。

```html
<div>这是头部</div>
<span>今日价格</span>
```

div是division的缩写，表示分割、分区。span意为跨度、跨距。

div独占一行（大盒子），span一行可以放多个（小盒子）。



#### 图像标签和路径

在HTML标签中，`<img>`标签用于定义HTML页面中的图像。

```html
<img src="图像URL"/>
```

`<img>`是<u>单标签</u>，是单词image的缩写，意为图像。

**src**是`<img>` 标签的必须属性，用于指定图像文件的路径和文件名。

图像标签的其他属性：

| 属性   | 属性值   | 说明                                 |
| ------ | -------- | ------------------------------------ |
| src    | 图片路径 | 必须属性                             |
| alt    | 文本     | 替换文本，图片不能显示的文字         |
| title  | 文本     | 提示文本，鼠标放到图像上，显示的文字 |
| width  | 像素     | 设置图像的宽度                       |
| height | 像素     | 设置图像的高度                       |
| border | 像素     | 设置图像的边框粗细                   |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h4>图像标签的使用：</h4>
    <img src="img.jpg">
    <h4>alt替换文本 图像显示不出来的时候用文字替换</h4>
    <img src="img1.jpg" alt="图片加载失败"/>
    <h4>title提示文本，鼠标放到图像上面会提示文字</h4>
    <img src="img.jpg" title="这里是图像上提示文字"/>
    <h4>width给图片设定宽度</h4>
    <img src="img.jpg" title="这里是图像上提示文字" width="500"/>
    <h4>height给图片设定高度</h4>
    <img src="img.jpg" title="这里是图像上提示文字" height="200"/>
    <h4>border给图片设定边框</h4>
    <img src="img.jpg" title="这里是图像上提示文字" width="500" border="5"/>
</body>
</html>
```

* 宽度、高度设定一般仅修改一个。

* 图像标签可以拥有多个属性，必须写在标签名后面。

* 属性之间部分先后顺序，用空格隔开，属性=“属性值”。

<u>相对路径</u>：以引用文件所在位置为参考基础，而建立出的目录路径。简单来说，图片相对于HTML页面的位置。

| 相对路径分类 | 符号 | 说明                                                         |
| ------------ | ---- | ------------------------------------------------------------ |
| 同一级路径   |      | 图片文件位于HTML文件同一级                                   |
| 下一级路径   | /    | 图片文件位于HTML文件下一级                                   |
| 上一级路径   | ../  | 图片文件位于HTML文件上一级，如`<img src="../img.jpg">`，需要先通过`../`返回到上一级 |

<u>绝对路径</u>:是指目录下的绝对位置，直接到达目标位置，通常是从盘符开始的路径。

<u>相对路径`/`，绝对路径`\`。</u> 



#### 超链接标签

`<a>`标签用于定义超链接，作用是从一个页面连接到另一个页面。

```html
<a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像</a>
```

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| href   | 用于指定连接目标的url地址，（必须属性）当为标签应用href属性时，它就具有了超链接的功能。 |
| target | 用于指定链接页面的打开方式，其中`_self`为默认值，`_blank`为在新窗口中打开方式。 |

**链接的分类**：

1. 外部链接，例如：

   ```html
   <a href="http://www.baidu.com">百度</a>
   ```

2. 内部链接：网站内部页面之间的相互链接，直接链接内部页面名称即可，例如：

   ```html
   <a href="index.html">首页</a>
   ```

3. 空链接：如果当时没有确定链接目标时，

   ```html
   <a href="#">首页</a>
   ```

4. 下载链接：如果href里面地址是一个`.exe`文件或者`.zip`压缩包，会下载这个文件。

   ```html
   <a href="ysb.zip">下载文件</a>
   ```

5. 网页元素链接：在网页中的各种网页元素，如文本、图像、表格、音频、视频都可以添加超链接。

   ```html
   <a href="http://www.baidu.com"><img src="img.jpg"></a>
   ```

6. 锚点链接：点击链接，可以快速定位到页面中的某个位置。

   ```html
   <a href="#two">第2集</a>
   <h3 id="two">第2集介绍</h3>
   ```



### HTML中注释和特殊字符

#### 注释

HTML中的注释以`<!--`开头，以`-->`结束。快捷键：`ctrl + /`。

#### 特殊字符

| 特殊字符 | 描述   | 字符的代码 |
| -------- | ------ | ---------- |
|          | 空格符 | `&nbsp;`   |
| &lt;     | 小于号 | `&lt;`     |
| &gt;     | 大于号 | `&gt;`     |
| &amp;    | 和号   | `&amp;`    |



### HTML其他标签

#### 表格标签

表格主要用于显示，展示数据。

```html
<table>
    <tr>
        <td>单元格内的文字</td>
    </tr>
</table>
```

`<table></table>`用于定义表格的标签。

`<tr></tr>`用于定义表格中的行，必须嵌套在`<table></table>` 标签中。

`<td></td>`用于定义表格中的单元格，必须嵌套在`<tr></tr>`标签中。



##### 表头单元格标签

`<th>`标签表示HTML表格的表头部分。

`<th>`与`<td>`不同于，表头单元格内的文本内容会加粗居中显示。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table>
        <tr>   <th>学号</th>  <th>姓名</th>  <th>性别</th></tr>
        <tr>   <td>001</td>    <td>方灿</td>  <td>男</td></tr>
    </table>
</body>
</html>
```



##### 表格属性 

表格标签这部分属性我们实际开发并不常用，后面通过CSS来设置。

| 属性名      | 属性值              | 描述                                             |
| ----------- | ------------------- | ------------------------------------------------ |
| align       | left、center、right | 规定表格相对周围元素的对齐方式                   |
| border      | 1或“”               | 规定表格单元是否拥有边框，默认为“”，表示没有边框 |
| cellpadding | 像素值              | 规定单元边沿与其内容之间的空白，默认1像素        |
| cellspacing | 像素值              | 规定单元格之间的空白，默认2像素                  |
| width       | 像素值或百分比      | 规定表格的宽度                                   |

```html
<table align="center" border="1" cellpadding="10" cellspacing="0">
        <tr>   <th>学号</th>  <th>姓名</th>  <th>性别</th></tr>
        <tr>   <td>001</td>   <td>方灿</td>  <td>男</td></tr>
    </table>
```



#####表格结构标签

`<thead>`标签：表格的头部区域，`<tbody>`标签：表格的主体区域。



#####合并单元格

合并单元格方式：

* 跨行合并：rowspan="合并单元格的个数"。上侧单元格为目标单元格，写合并代码。
* 跨列合并：colspan="合并单元格的个数"。左侧单元格为目标单元格，写合并代码。



#### 列表标签

列表是用来布局的。

列表分为三大类：无序列表、有序列表和自定义列表。



##### 无序列表

`<ul>`标签表示HTML页面中项目的无序列表，一般会以项目符号呈现列表项，而列表项使用`<li>`标签定义。

```html
<ul>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
</ul>
```



##### 有序列表

`<ol>`标签表示HTML页面中项目的有序列表，列表排序以数字来显示，而列表项使用`<li>`标签定义。



##### 自定义列表

自定义列表经常用于对术语或名词进行解释和描述，定义列表的列表项前没有任何项目符号。

`<dl>`标签用于定义描述列表，该标签会与`<dt>`（定义项目/名字）和`<dd>`（描述每一个项目/名字）一起使用。

```html
<dl>
    <dt>关注我们</dt>
    <dd>新浪微博</dd>
    <dd>官方微信</dd>
</dl>
```



#### 表单标签

使用表单是为了收集用户信息。

在HTML中，一个完整的表单是由<u>表单域</u>、<u>表单控件（表单元素）</u>和<u>提示信息</u>组成。



##### 表单域

表单域是一个包含表单元素的区域。

在HTML标签中，`<form>`标签用于定义表单域，实现用户信息的收集和传递。

<u>`<form>`会把它范围内的表单元素信息提交给服务器。</u>

```html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
```

常用属性：

| 属性   | 属性值   | 作用                                               |
| ------ | -------- | -------------------------------------------------- |
| action | url地址  | 用于指定接收并处理表单数据的服务器程序的url地址    |
| method | get/post | 用于设置表单数据的提交方式，其取值为get或者post    |
| name   | 名称     | 用于指定表单的名称，以区分同一个页面中的多个表单域 |



##### 表单控件（表单元素）

`<input>`<u>单标签</u>用于收集用户信息。

```html
<input type="属性值" />
```

在`<input>`标签中，包含一个type属性，根据不同的type属性值，输入字段拥有很多形式。

| 属性值   | 描述                                                 |
| -------- | ---------------------------------------------------- |
| button   | 可点击按钮（多数情况下，用于通过JavaScript启动脚本） |
| checkbox | 复选框                                               |
| file     | 输入字段和浏览按钮，供文件上传                       |
| hidden   | 隐藏的输入字段                                       |
| image    | 图像形式的提交按钮                                   |
| password | 密码字段                                             |
| radio    | 单选按钮                                             |
| reset    | 重置按钮                                             |
| submit   | 提交按钮，会把表单数据发送到服务器                   |
| text     | 输入字段，默认宽度20                                 |

`<input>`除了type属性外还有很多其他属性：

| 属性      | 属性值     | 描述                                |
| --------- | ---------- | ----------------------------------- |
| name      | 用户自定义 | 定义input元素名称                   |
| value     | 用户自定义 | 规定input元素的值                   |
| checked   | checked    | 规定此input元素首次加载时应当被选中 |
| maxlength | 正整数     | 规定输入字段中字符的最大长度        |

name和value是每个表单元素都有的属性值，主要给后台人员使用。

name是每个表单元素的名字，<u>要求单选按钮和复选按钮要有相同的name值</u>，用于区分不同的表单元素。

value可以使某些表单元素刚打开就默认显示几个文字。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Input 表单元素</title>
</head>
<body>
    <form>
        <!-- text 文本框 -->
        用户名：<input type="text" name="username" value="请输入用户名" maxlength="6"> <br>
        
        <!-- password 密码框 -->
        密码：<input type="password" name="pwd"> <br>
        
        <!-- radio 单选按钮 可以实现多选一 -->
        <!-- name 是表单元素名字 这里性别单选按钮必须有相同的名字name 才可以实现多选一 -->
        <!-- 单选框和复选框可以设置checked属性，当页面打开的时候就可以默认选中这个按钮 -->
        性别：男<input type="radio" name="sex" value="男" checked="checked"> 女<input type="radio" name="sex" value="女"> <br>
        
        <!-- checkbox 复选框 可以多选 -->
        爱好：吃饭<input type="checkbox"> 睡觉<input type="checkbox"> 打豆豆<input type="checkbox"> <br>
        
        <input type="submit" value="免费注册">
        <input type="reset" value="重新输入">
        
        <!-- button 普通按钮 后期搭配js使用 -->
        <input type="button" value="获取短信验证码"><br>
        
        <!-- 文件域 使用场景 上传文件使用的 -->
        上传头像：<input type="file">
        
    </form>
</body>
```

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200725223003265.png" alt="image-20200725223003265" style="zoom:67%;" />



##### `<label>`标签 

`<label>`标签为input元素定义标注（标签）。

`<label>`标签用于绑定一个表单元素，当点击`<label>`标签的文本时，浏览器会自动将焦点（光标）转到或者选择对应的表单元素上，用来增加用户体验。

```html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex" />
```

`<label>`标签的for属性应当与相关元素的id属性相同。



##### `<select>`表单元素

我们可以用`<select>`标签控件定义下拉列表。

```html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
</select>
```

`<select>`中至少包含一对`<option>`。

在`<select>`中定义 selected=“selected” 时，当前项即为默认选中项。



##### `<textarea>`表单元素

当输入内容较多时，可以用`<textarea>`文本域标签，可以定义多行文本输入。

```html
<textarea rows="3" cols="20">
    文本内容
</textarea>
```



#### 综合案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>综合案例注册页面</title>
</head>
<body>
    <h4>青春不常在，抓紧学编程</h4>
    <table width="600">
        <!--第一行-->
        <tr>
            <td>性别：</td>
            <td>
                <input type="radio" name="sex" id="man"><label for="man">男</label>&nbsp;
                <input type="radio" name="sex" id="woman"><label for="woman">女</label>
            </td>
        </tr>
        <!--第二行-->
        <tr>
            <td>生日：</td>
            <td>
                <select>
                    <option>--请选择年份--</option>
                    <option>2000</option>
                    <option>2001</option>
                    <option>2002</option>
                    <option>2003</option>
                    <option>2004</option>
                    <option>2005</option>
                </select>
                <select>
                    <option>--请选择月份--</option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                    <option>4</option>
                    <option>5</option>
                    <option>6</option>
                </select>
                <select>
                    <option>--请选择日期--</option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                    <option>4</option>
                    <option>5</option>
                    <option>6</option>
                </select>
            </td>
        </tr>
        <!--第三行-->
        <tr>
            <td>所在学校</td>
            <td>
                <input type="text" value="请输入在读学校">
            </td>
        </tr>
        <!--第四行-->
        <tr>
            <td>专业：</td>
            <td><input type="radio" name="major" checked="checked" id="jk"><label for="jk">计科</label> 
                <input type="radio" name="major" id="rg"><label for="rg">软工</label> 
                <input type="radio" name="major" id="dsj"><label for="dsj">大数据 </label>
                <input type="radio" name="major" id="wlw"><label for="wlw">物联网</label>
            </td>
        </tr>
        <!--第五行-->
        <tr>
            <td>在读年级:</td>
            <td>
                <input type="text" value="请输入在读年级">
            </td>
        </tr>
        <!--第六行-->
        <tr>
            <td>学习方向：</td>
            <td>
                <input type="checkbox" name="direction" checked="checked">前端开发
                <input type="checkbox" name="direction">人工智能
                <input type="checkbox" name="direction">游戏设计
            </td>
        </tr>
        <!--第七行-->
        <tr>
            <td>个人介绍</td>
            <td>
                <textarea>个人简介</textarea>
            </td>
        </tr>
        <!--第八行-->
        <tr>
            <td></td>
            <td>
                <input type="submit" value="注册">
            </td>
        </tr>
        <!--第九行-->
        <tr>
            <td></td>
            <td>
                <input type="checkbox" checked="checked">我同意注册条款和会员加入标准
            </td>
        </tr>
        <!--第十行-->
        <tr>
            <td></td>
            <td>
                <a href="#">我是会员，立即登录</a>
            </td>
        </tr>
        <!--第十一行-->
        <tr>
            <td></td>
            <td>
                <h5>我承诺</h5>
                <ul>
                    <li>信息属实</li>
                    <li>认真学习</li>
                </ul>
            </td>
        </tr>
    </table>
</body>
</html>
```



-----

## CSS

CSS是层叠样式表的简称。

CSS也是一种标记语言。主要用于设置HTML页面中的文本内容（字体、大小、对齐）、图片的外形（宽高、边框样式、边距等）以及版面的布局和外观显示样式。

由HTML专注去做结构呈现，样式交给CSS，结构（HTML）与样式（CSS）相分离。

<u>CSS规则由两个主要的部分构成：选择器以及一条或多条声明。</u>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS语法规范</title>
    <style>
        /* 选择器{样式} */
        /* 给谁改样式{改什么样式} */
        p {
            color: red;
            /* 修改了文字大小为12像素 */
            font-size: 12px;
        }
    </style>
</head>
<body>
    <p>有点意思</p>
</body>
</html>
```

* 属性和属性值以“键值对”的形式出现
* 属性是对指定的对象设置的样式属性，如字体大小、文本颜色
* 属性和属性值之间用英文“:”分开
* 多个键值对之间用“;”进行区分



### CSS代码风格

样式格式书写：

紧凑格式

```html
h3 { color: deeppink;font-size: 20px;}
```

展开格式

```html
h3 { 
   color: deeppink;
   font-size: 20px;
}
```

样式大小写风格：

选择小写。

样式空格风格：

```html
h3 {
   color: pink;
}
```

* 属性值前面，冒号后面保留一个空格
* 选择器（标签）和大括号中间保留空格



### CSS基础选择器

选择器就是根据不同需求把不同的标签选出来，简单来说就是选择标签用的。

选择器分为<u>基础选择器</u>和<u>复合选择器</u>两个大类。

* 基础选择器是由单个选择器组成的
* 基础选择器又包括：标签选择器、类选择器、id选择器和通配符选择器



#### 标签选择器

标签选择器（元素选择器）是指用HTML标签作为选择器，按标签名称分类，为页面中某一类标签指定统一的CSS样式。

```html
标签名 {
     属性1: 属性值1;
     属性2: 属性值2;
     属性3: 属性值3;
     ···
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>基础选择器之标签选择器</title>
    <style>
        /* 标签选择器 ： 写上标签名 */
        p {
            color: green;
        }
        div {
            color: pink;
        }
    </style>
</head>
<body>
    <p>男生</p>
    <p>男生</p>
    <p>男生</p>
    <div>女生</div>
    <div>女生</div>
    <div>女生</div>
</body>
</html>
```

标签选择器可以把某一类标签全部选择出来，比如所有的`<div>`标签和所有的`<span>`标签。



#### 类选择器

单独选一个或者几个标签，可以使用类选择器。

```html
.类名 {
     属性1: 属性值1;
     ···
}
```

例如，将所有拥有red类的HTML元素均为红色：

```html
.red {
    color: red;
}
```

结构需要用**class属性**来调用class类对的意思。

```html
<div class="red">变红色</div>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>基础选择器之类选择器</title>
    <style>
        /* 类选择器口诀：样式点定义 结构类调用 一个或多个 开发最常用 */
        .red {
            color: red;
        }
    </style>
</head>
<body>
    <ul>
        <li class="red">陈</li>
        <li class="red">写</li>
        <li>意</li>
    </ul>
</body>
</html>
```

* 类选择器使用“.”（英文点号）进行标识，后面紧跟类名（自定义，我们自己命名）
* 长名称或者词组可以使用横线来为选择器命名
* 不要使用纯数字、中文等命名，尽量使用英文字母表示
* 命名要有意义，尽量使别人一眼就知道这个类名的目的

用类选择器设置盒子背景颜色：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>类选择器画三个盒子</title>
    <style>
        .red {
            width: 100px;
            height: 100px;
            background-color: red;
        }
        .green {
            width: 100px;
            height: 100px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="red"></div>
    <div class="green"></div>
    <div class="red"></div>
</body>
</html>
```



**类命名规范：**

 头：header 

 内容：content/container

 尾：footer

 导航：nav  

 侧栏：sidebar

 栏目：column

 页面外围控制整体布局宽度：wrapper

 左右中：left right center

 登录条：loginbar

 标志：logo

 广告：banner

 页面主体：main

 热点：hot

 新闻：news

 下载：download

 子导航：subnav

 菜单：menu

 子菜单：submenu

 搜索：search

 友情链接：friendlink

 页脚：footer

 版权：copyright

 滚动：scroll

 内容：content

 标签页：tab

 文章列表：list

 提示信息：msg

 小技巧：tips

 栏目标题：title

 加入：joinus

 指南：guild

 服务：service

 注册：regsiter

 状态：status

 投票：vote

 合作伙伴：partner

**(二)注释的写法:**

 /* Footer */

 内容区

 /* End Footer */

**(三)id的命名:**

 **(1)页面结构**

 容器: container

 页头：header

 内容：content/container

 页面主体：main

 页尾：footer

 导航：nav

 侧栏：sidebar

 栏目：column

 页面外围控制整体布局宽度：wrapper

 左右中：left right center

 **(2)导航**

 导航：nav

 主导航：mainbav

 子导航：subnav

 顶导航：topnav

 边导航：sidebar

 左导航：leftsidebar

 右导航：rightsidebar

 菜单：menu

 子菜单：submenu

 标题: title

 摘要: summary

 **(3)功能**

 标志：logo

 广告：banner

 登陆：login

 登录条：loginbar

 注册：regsiter

 搜索：search

 功能区：shop

 标题：title

 加入：joinus

 状态：status

 按钮：btn

 滚动：scroll

 标签页：tab

 文章列表：list

 提示信息：msg

 当前的: current

 小技巧：tips

 图标: icon

 注释：note

 指南：guild

 服务：service

 热点：hot

 新闻：news

 下载：download

 投票：vote

 合作伙伴：partner

 友情链接：link

 版权：copyright\



**多类名的使用方式：**

```html
<div class="red font20">亚瑟</div>
```

* 在标签class属性中写多个类名
* 多个类名中间必须用空格分开

```html
<html>
    <head>
    <title>多类名的使用方式</title>
    <style>
        .red {
            color: red;
        }
        .font35 {
            font-size: 35px;
        }
    </style>
</head>
<body>
    <div class="red font35">123456</div>
</body>
</html>
```



#### id选择器

id选择器可以为特定id的HTML元素指定特定的样式。

HTML元素以id属性来设置id选择器，CSS中id选择器以`#`来定义。

```tml
#id名 {
    属性1： 属性值1；
    ···
}
```

<u>id选择器口诀：样式#定义，结构id调用，只能调用一次，别人切勿使用</u>

```txt
类选择器好比人的名字昵称，id选择器好比人的身份证号码无重复。
```



#### 通配符选择器

在CSS中，通配符选择器使用`*`定义，它表示选取页面中所有元素（标签）。

```html
* {
  属性1： 属性值1；
  ···
}
```



#### 四种选择器总结

| 基础选择器   | 作用                   | 特点                               | 使用情况     | 用法                 |
| :----------- | ---------------------- | ---------------------------------- | ------------ | -------------------- |
| 标签选择器   | 可以选出所有相同的标签 | 不能差异化选择                     | 较多         | p {color: red;}      |
| 类选择器     | 可以选出1个或多个标签  | 可以根据需求选择                   | 非常多       | .nav {color: red;}   |
| id选择器     | 一次只能选择一个标签   | ID属性只能在每个HTML文档中出现一次 | 一般与JS搭配 | `#`nav {color: red;} |
| 通配符选择器 | 选择所有标签           | 选择的太多，有部分不需要           | 特殊情况使用 | *{color: red;}       |



### CSS字体属性

CSS Fonts（字体）属性用于定义字体系列、大小、粗细、和文字样式（如斜体）。



#### 字体系列

CSS使用font-family属性定义文本的字体系列。

```html
p {
  font-family: "微软雅黑";
}
div {
  font-family: Arial,"Microsoft Yahei","微软雅黑"；
}
```

* 各种字体之间必须用英文状态下的逗号隔开
* 一般情况下，如果有空格隔开的多个但系组成的字体，加引号



#### 字体大小

CSS使用font-size属性定义文字大小。

```html
p {
  font-size: 20px;
}
```

* px（像素）大小是网页常用的单位
* 谷歌浏览器默认的文字大小是16px
* 不同浏览器可能默认显示的字号大小不一致，我们尽量给一个明确值的大小，不要默认大小
* 可以给body指定整个页面文字的大小
* 标题标签比较特殊，需要单独指定文字大小



#### 字体粗细

CSS使用font-weight属性设置文本字体的粗细。

```html
.bold {
     /* font-size:bold */
     /* 700后面不要跟单位 等价于bold 都是加粗的效果 */
     /* 实际开发中更体长用number表示加粗或变细 */
     font-weight： 700;
}
h2 {
     /* 变细可用以下两种 */
     font-weight: 400;
     font-weight: normal;
}
```

| 属性值  | 描述                                         |
| ------- | -------------------------------------------- |
| normal  | 默认值（不加粗的）                           |
| bold    | 定义粗体（加粗的）                           |
| 100-900 | 400等同于normal，700等同于bold，后面不跟单位 |



#### 文字样式

CSS使用font-style属性设置文本的风格。

```html
p {
  font-style: normal;
}
```

| 属性值 | 作用                                                  |
| ------ | ----------------------------------------------------- |
| normal | 默认值，浏览器会显示标准的字体样式font-style: normal; |
| italic | 浏览器会显示*斜体*的字体样式                          |

* 平时很少给文字加斜体，反而要给斜体标签（em,i）改为不倾斜字体



#### 字体复合属性

字体属性可以把以上文字样式综合来写，这样可以更节约代码。

```html
body {
    font: font-style font-weight font-size/line-height font-family;
}
```

```html
<style>
    div {
        font: italic 700 16px 'Microsoft Yahei';
        /* 下面两个不能省略 */
        font:16px 'Microsoft Yahei';
    }
</style>
```

* 使用font属性时，必须按上面语法格式中的顺序书写，不能更换顺序，并且各个属性间以空格隔开
* 不需要设置的属性可以忽略（取默认值），但必须保留font-size和font_family属性，否则font属性将不起作用



### CSS文本属性

CSS Text（文本）属性可以定义文本的外观，比如文本的颜色、对齐文本、装饰文本、文本缩进、行间距等。



#### 文本颜色

color属性用于定义文本的颜色。

```html
div {
   color: red;
}
```

| 表示           | 属性值                 |
| -------------- | ---------------------- |
| 预定义的颜色值 | red，green，blue，pink |
| 十六进制       | `#`FF0000              |
| RGB代码        | rgb(255,0,0)           |



#### 对齐文本

text-align属性用于设置元素内文本内容的水平对齐方式。

```html
div {
   text-align: center;
}
```

| 属性值 | 解释             |
| ------ | ---------------- |
| left   | 左对齐（默认值） |
| right  | 右对齐           |
| center | 居中对齐         |



#### 装饰文本

text-decoration属性规定添加到文本的修饰，可以给文本添加下划线、删除线、上划线等。

```html
div {
    text-decoration: underline;
}
```

| 属性值       | 描述                            |
| ------------ | ------------------------------- |
| none         | 默认。没有装饰线                |
| underline    | 下划线。链接a自带下划线（常用） |
| overline     | 上划线。（几乎不用）            |
| line-through | 删除线。（不常用）              |

链接a去掉下划线：

```html
<html>
    <head>
        <style>
            a {
                text-decoration: none;
            }
        </style>
    </head>
    <body>
        <a href="#">没有下划线的链接</a>
    </body>
</html>
```



#### 文本缩进

text-indent属性用来指定文本的第一行缩进，通常是将段落的首行缩进。

```html
div {
    text-indent: 20px;
}
```

通过设置该属性，所有元素的第一行都可以缩进一个给定的长度，甚至该长度可以是负值。

```html
p {
    text-indent: 2em;
}
```

em是一个相对单位，就是当前元素（font-size）1个文字的大小，如果当前元素没有设置大小，则会按照父元素1个文字大小。



#### 行间距

line-height属性用于设置行间的距离（行高）。可以控制文字行与行之间的距离。

```html
p {
  line-height: 26px;
}
```

![image-20200805230859732](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200805230859732.png)

文本高度已定不变，改变行间距会改变上间距和下间距。

上间距和下间距会一样高。



#### 文本属性总结

| 属性            | 表示     | 注意点                                        |
| --------------- | -------- | --------------------------------------------- |
| color           | 文本颜色 | 通常用 十六进制                               |
| text-align      | 文本对齐 | 可以设定文字水平的对齐方式                    |
| text-indent     | 文本缩进 | 通常用于首航缩进2个字的距离 text-indent: 2em; |
| text-decoration | 文本修饰 | 添加下划线underline，取消下划线none           |
| line-height     | 行高     | 控制行与行之间的距离                          |



### CSS的引入方式

按照CSS样式书写的位置（或者引入的方式），CSS眼视光hi表可以分为三大类：

* 行内样式表（行内式）
* 内部样式表（嵌入式）
* 外部样式表（链接式）



#### CSS内部样式表

内部样式表（内嵌样式表）是写到html页面内部，是将所有的CSS代码抽取出来，单独放到一个`<style>`标签中。

```html
<style>
    div {
        color: red;
        font-size: 12px;
    }
</style>
```

* `<style>`标签理论上可以放在html文档的任何地方，但一般放在文档的`<head>`标签中
* 通过此种方式，可以方便控制当前整个页面中的元素样式设置
* 代码结构清晰，但并没有实现结构与样式完全分离



#### 行内样式表

行内样式表（内联样式表）是元素标签内部的style属性中设定CSS样式。适合于修改简单样式。

```html
<div style="color: red; font-size: 12px;">行列样式表</div>
```

* style其实是标签的属性
* 在双引号中间，写法要符合CSS规范
* 可以控制当前的标签设置样式
* 由于书写繁琐，没有体现出结构与样式分离



#### 外部样式表

实际开发都是外部样式表，适合于样式比较多的情况，核心是：样式单独写到CSS文件中，之后把CSS文件引入到HTML页面中使用。

**引入外部样式表分两步：**

1. 新建一个后缀名为.css的样式文件，把所有CSS代码都放入此文件中。
2. 在HTML页面中，使用`<link>`标签引入这个文件。

```html
<link rel="stylesheet" href="css文件路径">
```

![image-20200806160850409](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806160850409.png)



#### CSS引入方式总结

| 样式表     | 优点                   | 缺点         | 使用情况 | 控制范围     |
| ---------- | ---------------------- | ------------ | -------- | ------------ |
| 行内样式表 | 书写方便，权重高       | 结构样式混写 | 较少     | 控制一个标签 |
| 内部样式表 | 部分结构和样式分离     | 没有彻底分离 | 较多     | 控制一个页面 |
| 外部样式表 | 完全实现结构和样式分离 | 需要引入     | 最多     | 控制多个页面 |



### 综合案例

html文件：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>北方高温明日达鼎盛 京津冀多地地表温度将超60℃</h1>
    <div class="gray">2019-07-03 16:31:47 来源: <a href="#">中国天气网　</a>  
    <input type="text" value="请输入查询条件" class="search">  <button class="btn">搜索</button>
</div>
    <hr>

    <p>中国天气网讯 今天（3日），华北、黄淮多地出现高温天气，截至下午2点，北京、天津、郑州等地气温突破35℃。
    预报显示，今后三天（3-5日），这一带的高温天气将继续发酵，
    高温范围以及强度将在4日达到鼎盛，预计北京、天津、石家庄、济南等地明天的最高气温有望突破38℃，
    其中北京和石家庄的最高气温还有望创今年以来的新高。</p>
    
    <h4>气温41.4℃！地温66.5！北京强势迎七月首个高温日</h4>
    
    <p><img src="image/pic.jpeg" alt=""></p>

    <p>今天，华北、黄淮一带的高温持续发酵，截至今天下午2点，陕西北部、山西西南部、河北南部、北京、天津、
    山东西部、河南北部最高气温已普遍超过35℃。大城市中，北京、天津、郑州均迎来高温日。</p>
    
    <p>在阳光暴晒下，地表温度也逐渐走高。今天下午2点，
    华北黄淮大部地区的地表温度都在50℃以上，部分地区地表温度甚至超过60℃。其中，河北衡水地表温度高达68.3℃，天津站和北京站附近的地表温度分别高达66.6℃和66.5℃。在阳光暴晒下，
    地表温度也逐渐走高。今天下午2点，华北黄淮大部地区的地表温度都在50℃以上，
    部分地区地表温度甚至超过60℃。其中，河北衡水地表温度高达68.3℃，天津站和北京站附近的地表温度分别高达66.6℃和66.5℃。</p>
    
    <h4>明日热度再升级！京津冀携手冲击38℃+</h4>
    
    <p>中国天气网气象分析师王伟跃介绍，明天（4日），华北、黄淮地区35℃以上的高温天气还将继续升级，
    并进入鼎盛阶段，高温强度和范围都将发展到最强。 明天，北京南部、天津大部、河北中部和南部、山东中部和西部、
    山西南部局地、河南北部、东北部分地区的最高气温都将达到或超过35℃。</p>
    
    <p>不过，专家提醒，济南被雨水天气完美绕开，因此未来一周，当地的高温还会天天上岗。
    在此提醒当地居民注意防暑降温，防范持续高温带来的各种不利影响。（文/张慧 数据支持/王伟跃 胡啸 审核/刘文静 张方丽）</p>

    <p class="footer">本文来源：中国天气网 责任编辑：刘京_NO5631</p>
</body>
</html>
```

CSS文件：

```css
body {
    font: 16px/28px 'Microsoft YaHei';

}
h1 {
    font-weight: 400;
    text-align: center;
}
.gray {
    color: #888888;
    font-size: 12px;
    text-align: center;
}
a {
    text-decoration: none;
}
.search {
    color: #666;
    width: 170px;
}
.btn {
    font-weight: 700;
}
p {
    text-indent: 2em;
}
.footer {
    color: #888;
}
```

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806162522602.png" alt="image-20200806162522602" style="zoom:67%;" />



### Chrome调试工具

![image-20200806163118173](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806163118173.png)



### Emmet语法

#### 快速生成HTML结构语法

1. 生成标签 直接输入标签名 按tab键。比如div然后按tab键，就可以生成`<div></div>`
2. 如果想要生成多个相同标签 加上`*`就可以了。比如 div`*`3就可以快速生成3个div
3. 如果有服自己关系的标签，可以用`>`。比如ul`>`li就可以了
4. 如果有兄弟关系的标签，用`+`就可以。比如div+p
5. 如果生成带有类名或者id名字的，直接写`.demo`或者`#two`tab键就可以了
6. 如果生成的div类名是由顺序的，可以用自增符号`$`
7. 如果下能要在生成的标签内部写内容可以用`{}`表示



#### 快速生成CSS样式语法

CSS基本采取简写形式即可

1. 比如`w200 `按tab键，可以生成`width: 200px;`
2. 比如`lh26`按tab键，可以生成`line-height: 26px;`



#### 快速格式化代码

`shift + alt + F`

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806174746557.png" alt="image-20200806174746557"  />



### CSS的复合选择器

常用的复合选择器包括：后代选择器、子选择器、并集选择器、伪类选择器等等。



#### 后代选择器（重要）

后代选择器又称包含选择器，可以选择父元素里面的子元素。其写法就是把外层标签写在前面，内层标签写在后面，中间用空格分割。当标签发生嵌套时，内层标签就成为外层标签的后代。

语法：

```txt
元素1 元素2 { 样式声明 }
```

上述语法表示选择元素1里面的所有元素2（后代元素）。

例如：

```txt
ul li { 样式声明 } /* 选择ul里面所有的li标签元素 */
```

* 元素1和元素2中间**一定要用空格隔开**
* 元素1是父级，元素2是子级，**最终选择是元素2**
* 只要包含在元素1里不管是子级，孙级都可以
* 元素1和元素2可以是任意基础选择器

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806202850766.png" alt="image-20200806202850766" style="zoom:67%;" />

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806202923803.png" alt="image-20200806202923803" style="zoom:67%;" />

![image-20200806202953676](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806202953676.png)



#### 子选择器（重要）

子元素选择器（子选择器）只能选择作为某元素的最近一级子元素。简单理解是选亲儿子元素。

```html
<html>
    <head>
        <title>子元素选择器</title>
        <style>
            .nav>a {
                color: red;
            }
        </style>
    </head>
    <body>
        <div class="nav">
            <a href="#">我是儿子</a>
            <p>
                <a href="#">我是孙子</a>
            </p>
        </div>
    </body>
</html>
```

语法：

```txt
元素1>元素2 { 样式声明 }
```

上述语法表示选择元素1里面的所有直接后代（子元素）元素2。

例如：

```txt
div > p { 样式声明 } /* 选择div里面所有最近一级p标签元素 */
```

* 元素1和元素2中间用**大于号**隔开
* 元素1是父级，元素2是子级，**最终选择的是元素2**
* **只能选择亲儿子**



#### 并集选择器（重要）

并集选择器可以选择多组标签，同时为他们定义相同的样式。通常用于集体声明。

并集选择器是各选择器通过应为逗号`,`连接而成，任何形式的选择器都可以作为并集选择器的一部分。

语法：

```txt
元素1,元素2{ 样式声明 }
```

上述语法表示选择元素1和元素2。

例如：

```html
ul,
div { 样式声明 } 
/* 选择ul 和 div标签元素 */
```

* 元素1和元素2中间用逗号隔开
* 逗号可以理解为和的意思
* **并集选择器竖着写**



#### 伪类选择器

味蕾选择器用于向某些选择器添加特殊的效果，比如给链接添加特殊效果，或者选择第1个，第n个元素。

伪类选择器书写最大的特点是用冒号`:`表示，比如`:hover`。

伪类选择器由很多：链接伪类、结构伪类等，这里讲的是链接伪类选择器。



##### 链接伪类选择器

```html
a:link     /*选择所有未被访问的链接*/
a:visited  /*选择所有已被访问的链接*/
a:hover    /*选择鼠标指针位于其上的链接*/
a:active   /*选择活动链接（鼠标按下未弹起的链接）*/
```

```html
<html>
    <head>
        <title>链接伪类选择器</title>
        <style>
           /* 未访问的链接 a:link */
            a:link {
                color: #333;
                text-decoration: none;
            }
            /* 访问过的链接 a:visited */
            a:visited {
                color: orange;
            }
            /* 鼠标经过的链接 a:hover */
            a:hover {
                color: skyblue;
            }
            /* 鼠标按下还没弹起的链接 a:active */
            a:active {
                color: green;
            }
        </style>
    </head>
    <body>
        <a href="#">链接伪类选择器</a>
    </body>
</html>
```

* 为了确保生效，按照LVHA的顺序声明：`:link`,`:visited`,`:hover`,`:active`
* 链接指定样式需要单独指定a标签



##### `:focus`伪类选择器

`:focus`伪类选择器用于选取获得焦点的表单元素。

焦点就是光标，一般情况`<input>`类表单元素才能获取，因此这个选择器也主要针对于表单元素来说。

```html
input:focus {
   background-color: yellow;
}
```

谁获得了光标就会改变颜色。



#### 复合选择器总结

| 选择器         | 作用                   | 特征             | 使用情况 | 隔开符号及用法              |
| -------------- | ---------------------- | ---------------- | -------- | --------------------------- |
| 后代选择器     | 用来选择后代元素       | 可以是子孙后代   | 较多     | 符号是**空格** .nav a       |
| 子代选择器     | 选择最近一级元素       | 只选亲儿子       | 较少     | 符号是**大于** .nav>p       |
| 并集选择器     | 选择某些相同样式的元素 | 可以用于集体声明 | 较多     | 符号是**逗号** .nav,.header |
| 链接伪类选择器 | 选择不同状态的链接     | 跟链接相关       | 较多     | 重点记住a{}和a:hover        |
| `:focus`选择器 | 选择获得光标的表单     | 跟表单相关       | 较少     | 记住input:focus             |



### CSS的元素显示模式

元素显示模式就是元素（标签）以什么方式进行显示比如`<div>`自己多占一行，比如一行可以放多个`<span>`。

HTML元素一般分为两大类：块元素和行内元素。



#### 块元素

常见的块元素有：`<h1>~<h6>`，`<p>`，`<div>`，`<ul>`，`<ol>`，`<li>`等，其中`<div>`标签是最典型的块元素。

特点：

* 独占一行
* 高度，宽度，外边距以及内边距都可以控制
* 宽度默认是容器（父级宽度）的100%
* 是一个容器及盒子，里面可以放行内或者块级元素

注意：

* 文字类的元素内不能使用块级元素
* `<p>`标签主要用于存放文字，因此里面不能放块级元素，特别是不能放`<div>`
* `<h1>~<h6>`也不能放块级元素



#### 行内元素

常见的行内元素有`<a>`，`<strong>`，`<b>`，`<em>`，`<i>`，`<del>`，`<s>`，`<ins>`，`<u>`，`<span>`等，其中`<span>`是最典型的行内元素。行内元素也称内联元素。

特点：

* 相邻行内元素在一行上，一行可以显示多个
* 高，宽直接设置是无效的
* 默认宽度就是它本身内容的宽度
* 行内元素只能容纳文本或其他行内元素

注意：

* 链接里面不能放链接
* 特殊情况链接`<a>`里面可以放块级元素，但转换一下块级模式最安全



#### 行内块元素

在行内元素中有几个特殊的标签-----`<img />`，`<input />`，`<td>`，他们同时具有块元素和行内元素的特点，有些资料称行内块元素。

特点：

* 和相邻行内元素（行内块）在一行上，但是他们之间会有空白缝隙，一行可以显示多个（行内元素特点）
* 默认宽度就是他本身内容的宽度（行内元素特点）
* 高度，行高，外边距以及内边框都可以控制（块级元素特点）



#### 元素显示模式总结

| 元素模式   | 元素排列               | 设置样式           | 默认宽度         | 包含                   |
| ---------- | ---------------------- | ------------------ | ---------------- | ---------------------- |
| 块级元素   | 一行只能放一个块级元素 | 可以设置宽度高度   | 容器的100%       | 容器可以包含任何标签   |
| 行内元素   | 一行可以放多个行内元素 | 不可以设置宽度高度 | 它本身内容的宽度 | 容纳文本或其他行内元素 |
| 行内块元素 | 一行放多个行内块元素   | 可以设置宽度和高度 | 它本身内容的宽度 |                        |



####元素显示模式转换

简单理解：一个模式的元素需要另一种模式的特性，比如想要增加链接`<a>`的出发范围。

```html
<html>
     <head>
        <title>元素显示模式转换</title>
        <style>
            a {
                wdith: 150px;
                height: 50px;
                background-color: pink;
                /*行内变块级*/
                display: block;
            }
            div {
                wdith: 300px;
                height: 100px;
                background-color: purple;
                /*块级变行内*/
                display: inline;
            }
            span {
                wdith: 300px;
                height: 30px;
                background-color: skyblue;
                display: inline-block;
            }
        </style>
    </head>    
    <body>
        <a href="#">行内变块级</a>
        <div>
            块级变行内
        </div>
        <span>行内元素转换为行内块元素</span>
    </body>
</html>
```

![image-20200806224123311](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806224123311.png)



####实践：（小米网站侧边栏）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简单版小米侧边栏</title>
    <style>
        a {
            width: 300px;
            height: 40px;
            display: block;
            font-size: 14px;
            color: white;
            background-color: darkgray;
            text-decoration: none;
            text-indent: 2em;
            line-height: 40px;
        }
        a:hover {
            background-color: #ff6700;
        }
    </style>
</head>
<body>
    <a href="#">手机 电话卡</a>
    <a href="#">电视 盒子</a>
    <a href="#">笔记本 平板</a>
    <a href="#">出行 穿戴</a>
    <a href="#">智能 路由器</a>
    <a href="#">健康 儿童</a>
    <a href="#">耳机 音响</a>
</body>
</html>
```

**文字居中：line-height: height;**



### CSS背景

#### 背景颜色

background-color属性定义了元素的背景颜色。

```html
background-color: 颜色值;
```

一般情况下元素背景颜色默认值是transparent（透明），也可手动设置。



#### 背景图片

background-image属性描述了元素的背景图像。实际开发中常见于logo或者一些装饰性的小图片或者是超大的背景图片，非常便于控制位置。

```html
background-image: none | url(url);
```

```html
div {
   width: 300px;
   height: 300px;
   background-image: url(images/Logo.png); 
}
```

| 参数值 | 作用                             |
| ------ | -------------------------------- |
| none   | 无背景图（默认的）               |
| url    | 使用绝对或者相对地址指定背景图像 |



#### 背景平铺

如果需要在HTML页面上对背景图像进行平铺，可以使用background-repeat属性。

```html
background-repeat: repeat| no-repeat| repeat-x| repeat-y;
```

分别是：平铺|不平铺|沿x轴平铺（横向平铺）|沿y平铺（纵向平铺）

背景颜色和背景图片可同在，只不过**背景图片会压住背景颜色。**



#### 背景图片位置

利用background-position属性可以改变图片在背景中的位置。

```html
background-position: x y;
```

x坐标和y坐标。可以使用方位名词或者精准单位。

| 参数值   | 说明                                              |
| -------- | ------------------------------------------------- |
| length   | 百分数\|有浮点数字和单位标识符组成的长度值        |
| position | top\|center\|bottom\|left\|center\|right 方位名词 |

* left top和top left效果一样
* 如果只指定了一个方位名词，另一个省略则默认剧中对齐
* 如果参数值是精确坐标，那么第一个肯定是x坐标，第二个一定是y坐标
* 如果只指定一个数值，那该数值一定是x坐标，另一个默认垂直居中
* 也可以两种混用



#### 背景图像固定（背景附着）

background-attachment属性设置背景图像是否固定或者随着页面的其余部分滚动。

background-attachment后期可以制作视差滚动的效果。

```html
background-attachment: scroll| fixed;
```

| 参数   | 作用                     |
| ------ | ------------------------ |
| scroll | 背景图像是随对象内容滚动 |
| fixed  | 背景图像固定             |



#### 背景的复合写法

简化背景属性的代码，属性合并简写在同一个属性background中，从而节约代码量。

顺序：

```txt
background: 背景颜色 背景图片 背景平铺 背景图像滚动 背景图片位置;
```

```html
background: transparent url(image.ipg) repeat-y fixed top;
```



#### 背景颜色半透明

CSS为我们提供了背景颜色半透明效果。

```html
background: rgba(0,0,0,0.3);
```

* r-red、g-green、b-blue
* 最后一个参数是alpha透明度，取值范围在0-1之间
* 0.3可以省略为.3
* 只有背景颜色半透明



#### 背景总结

| 属性                  | 作用           | 值                                                   |
| --------------------- | -------------- | ---------------------------------------------------- |
| background-color      | 背景颜色       | 预定义的颜色/十六进制/RGB代码                        |
| background-image      | 背景图片       | url（图片路径）                                      |
| background-repeat     | 是否平铺       | repeat/no-repeat/repeat-x/repeat-y                   |
| background-position   | 背景位置       | length/position                                      |
| background-attachment | 背景附着       | scroll（背景滚动）/fixed（背景固定）                 |
| 背景简写              | 书写更简单     | 背景颜色 背景图片 背景平铺 背景图像滚动 背景图片位置 |
| 背景色半透明          | 背景颜色半透明 | background: rgba(0,0,0,0.3);                         |



#### 综合案例：彩虹导航

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>五彩导航</title>
    <style>
        .nav a{
            display: inline-block;
            width: 120px;
            height: 58px;
            background-color: pink;
            text-align: center;
            line-height: 48px;
            text-decoration: none;
            background-repeat: no-repeat;
        }
        .nav .bg1 {
            background-image: url(images/bg1.png);
        }
        .nav .bg1:hover {
            background-image: url(images/bg11.png);
        }
        .nav .bg2 {
            background-image: url(images/bg2.png);
        }
        .nav .bg2:hover {
            background-image: url(images/bg22.png);
        }
        .nav .bg3 {
            background-image: url(images/bg3.png);
        }
        .nav .bg3:hover {
            background-image: url(images/bg3.png);
        }.nav .bg4 {
            background-image: url(images/bg4.png);
        }
        .nav .bg4:hover {
            background-image: url(images/bg4.png);
        }.nav .bg5 {
            background-image: url(images/bg5.png);
        }
        .nav .bg5:hover {
            background-image: url(images/bg5.png);
        }
    </style>
</head>
<body>
    <div class="nav">
        <a href="#" class="bg1">五彩导航</a>
        <a href="#" class="bg2">五彩导航</a>
        <a href="#" class="bg3">五彩导航</a>
        <a href="#" class="bg4">五彩导航</a>
        <a href="#" class="bg5">五彩导航</a>
    </div>
</body>
</html>
```



### CSS三大特性

**层叠性、继承性、优先级。**



#### 层叠性

给相同选择器设置相同的样式，此时一个样式就会覆盖（层叠）另一个冲突的样式。层叠性主要解决样式冲突问题。

层叠性原则：

* 样式冲突，遵循的原则是**就近原则**，那个样式离结构近，就执行哪个样式
* 样式不冲突，不会层叠



#### 继承性

子标签会继承父标签的某些样式，如文本颜色和字号。**子承父业**。

* 子元素可以继承父亲元素的样式（`text-`、`font-`、`line-`这些元素开头的可以继承，以及color属性）



##### 行高的继承

```html
body {
   font: 12px/1.5 Microsoft YaHei;
}
```

* 行高可以跟单位也可以不跟单位
* 1.5是当前文字大小的1.5倍  当前行高：font-size*1.5



#### 优先级

当同一个元素指定多个选择则其，就会有优先级的产生。

* 选择器相同，则执行层叠性
* 选择器不同，则根据**选择器权重**执行

| 选择器               | 选择器权重 |
| -------------------- | ---------- |
| 继承 或者 `*`        | 0,0,0,0    |
| 元素选择器           | 0,0,0,1    |
| 类选择器、伪类选择器 | 0,0,1,0    |
| ID选择器             | 0,1,0,0    |
| 行内样式`style=""`   | 1,0,0,0    |
| `!important`重要的   | 无穷大     |

**行内>ID>类>元素>继承**

* 继承的权重是0，子元素的权重永远是0



##### 权重叠加

复合选择器会有权重叠加的问题

div ul  li ------->0,0,0,3

.nav ul li ------>0,0,1,2

a:hover ------->0,0,1,1

.nav a --------->0,0,1,1



### 盒子模型

网页布局过程：

1. 先准备好相关的网页元素，网页元素基本都是盒子Box
2. 利用CSS设置好的样式，然后摆放到相应位置
3. 往盒子里装内容

CSS核心就是摆盒子。



#### 盒子模型（Box Model）组成

CSS盒子模型本质上是一个盒子，封装周围的HTML元素，它包括：边框、外边距、内边距和实际内容

![image-20200807173615888](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200807173615888.png)



#####边框（border）

border可以设置元素的边框，边框有三部分组成：边框宽度（粗细）、边框样式、边框颜色

语法：

```html
border : border-width|| border-style|| border-color
```

| 属性         | 作用                   |
| ------------ | ---------------------- |
| border-width | 定义边框粗细，单位是px |
| border-style | 边框的样式             |
| border-color | 边框的颜色             |



![image-20200807174518735](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200807174518735.png)

**solid实线边框    dashed虚线边框   dotted点线边框**

CSS边框属性允许指定一个元素边框的样式和颜色

边框简写：

```html
border: 1px solid red; 没有顺序
```

边框分开写法：

```html
border-top: 1px solid red;/* 只设定上边框，其余同理 */
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            border: 1px solid blue;
            border-top: 1px solid red;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```



##### 表格的细线边框

border-collapse属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框。

语法：

```html
border-collapse: collapse;
```

* collapse单词是合并的意思
* `border-collapse: collapse;`表示相邻边框会合并到一起

**合并例子：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>今日小说排行榜</title>
    <style>
        table {
            width: 500px;
            height: 249px;
        }
        table,
        td,
        th {
            border: 1px solid pink;
            border-collapse: collapse;
        }
    </style>
</head>
<body>
    <table align="center" width="500" height="249" border="1" cellspacing="0">
    <thead>
        <tr>
            <th>排名</th>
            <th>关键词</th>
            <th>趋势</th>
            <th>进入搜索</th>
            <th>最近七日</th>
            <th>相关链接</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>鬼吹灯</td>
            <td><img src="down.jpg"></td>
            <td>456</td>
            <td>123</td>
            <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>

        <tr>
                <td>1</td>
                <td>鬼吹灯</td>
                <td><img src="down.jpg"></td>
                <td>456</td>
                <td>123</td>
                <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>
        <tr>
                <td>3</td>
                <td>西游记</td>
                <td><img src="up.jpg"></td>
                <td>456</td>
                <td>123</td>
                <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>
        <tr>
                <td>1</td>
                <td>鬼吹灯</td>
                <td><img src="down.jpg"></td>
                <td>456</td>
                <td>123</td>
                <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>
        <tr>
                <td>1</td>
                <td>鬼吹灯</td>
                <td><img src="down.jpg"></td>
                <td>456</td>
                <td>123</td>
                <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>
        <tr>
                <td>1</td>
                <td>鬼吹灯</td>
                <td><img src="down.jpg"></td>
                <td>456</td>
                <td>123</td>
                <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>
    </tbody>           
    </table>
</body>
</html>
```



##### 边框会影响盒子实际大小

200大小的正方形盒子+两边都有的10px边框=220大小

width/height减去边框。



##### 内边距

padding属性用于设置内边距，即边框与内容之间的距离。

| 属性           | 作用     |
| -------------- | -------- |
| padding-left   | 左内边距 |
| padding-right  | 右内边距 |
| padding-top    | 上内边距 |
| padding-bottom | 下内边距 |

```html
div {
    width: 200px;
    height: 200px;
    background-color: pink;
    padding-left: 20px
}
```

**padding简写属性：**

| 值的个数                     | 表达意思                                                   |
| ---------------------------- | ---------------------------------------------------------- |
| padding: 5px;                | 一个值，代表上下左右都有5像素内边距                        |
| padding: 5px 10px;           | 两个值，代表上下内边距是5像素，左右边距是10像素            |
| padding: 5px 10px 20px;      | 3个值，代表上内边距5像素，左右内边距10像素，下内边距20像素 |
| padding: 5px 10px 20px 30px; | 4个值，上是5像素 右是10像素 下是20像素 左是30像素 顺时针   |



##### padding内边距也会影响盒子的大小

width/height减去多余的内边距。

如果盒子本身没有指定width/height属性，则此时padding不会撑开盒子大小。



##### 实践：新浪导航栏

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .nav {
            height: 41px;
            background-color: #fcfcfc;
            border-top: 3px solid #ff8500;
            border-bottom: 1px solid #edeef0;
            line-height: 41px;
        }
        .nav a {
            display: inline-block;
            font-size: 12px;
            height: 41px;
            padding: 0 20px;
            color: #4c4c4c;
            text-decoration: none;
        }
        .nav a:hover {
            background-color: #eee;
            color: #ff8500;
        }
    </style>
</head>
<body>
    <div class="nav">
        <a href="#">新浪导航</a>
        <a href="#">手机新浪网</a>
        <a href="#">移动客户端</a>
        <a href="#">微博</a>
    </div>
</body>
</html>
```



#####外边距（margin）

margin属性用于设置外边距，则控制盒子和盒子之间的距离。
| 属性           | 作用     |
| -------------- | -------- |
| margin-left   | 左外边距 |
| margin-right  | 右外边距 |
| margin-top    | 上外边距 |
| margin-bottom | 下外边距 |

margin简写方式和padding完全一致。

外边距可以让**块级盒子水平居中**，但是必须满足两个条件：

* 盒子必须指定了宽度（width）
* 盒子左右的外边距都设置为auto

```html
.header { width: 960px; margin: 0 auto;}
```

![image-20200807225823295](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200807225823295.png)



##### 外边距合并

对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会**塌陷**较大的外边距值。

解决方案：

* 可以为父元素定义上边框
* 可以为父元素定义上内边框
* **可以为父元素添加`overflow:hidden`**



##### 清除内外边距

网页元素很多都带有默认的内外边距，而且不同浏览器默认的也不一致。

```html
* {
  padding: 0;  /*清除内边距*/
  margin: 0;   /*清除外边距*/
}
```

行内元素为了照顾兼容性尽量只设置左右内外边距，不要设置上下内外边距。但是转换为块级和行内块元素就可以了。



#### PS基本操作

![image-20200807231659528](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200807231659528.png)

![image-20200807231804114](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200807231804114.png)



####综合案例

案例1：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }
        body {
            background-color: #f5f5f5;
        }
        a {
            text-decoration: none;
            color: #333;
        }
        .box {
            background-color: #fff;
            width: 298px;
            height: 415px;
            margin: 100px auto;
        }
        .box img {
            width: 298px;
        }
        .review {
            font-size: 14px;
            height: 70px;
            /* 段落没有width属性，所以padding不会撑宽宽度 */
            padding: 0 28px;
            margin-top: 30px;
        }
        .appraise {
            font-size: 12px;
            color: #b0b0b0;
            margin-top: 20px;
            padding: 0 28px;
        }
        .info {
            font-size: 14px;
            margin-top: 15;
            padding: 0 28px;           
        }
        .info h4 {
            display: inline-block;  
            font-weight: 400;  
        }
        .info span {
            color: coral;
        }
        .info em {
            font-style: normal;
            color: #b0b0b0;
            margin: 0 6px 0 15px;
        }
    </style>
</head>
<body>
    <div class="box">
        <a href="#"><img src="images/img.jpg" alt=""></a>
        <p class="review"><a href="#">快递牛，整体不错蓝牙可以说秒连。红米给力</a></p>
        <p class="appraise">来自于1178928的评价</p>
        <div class="info">
            <h4><a href="#">Redmi AirDots真无线蓝...</a></h4> 
            <em>|</em>
            <span>99.9元</span>
        </div>
    </div>
</body>
</html>
```

![image-20200807235531304](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200807235531304.png)

案例2：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            padding: 0px;
            margin: 0px;        
        }
        .box {
            width: 248px;
            height: 163px;
            border: 1px solid #ccc;
            margin: 100px auto;
        }
        .box h3 {
            height: 32px;
            border-bottom: 1px dotted #ccc;
            font-size: 14px;
            font-weight: 400;
            line-height: 32px;
            padding-left: 15px;
        }
        li {
            list-style: none;
            height: 23px;
            line-height: 23px;
            padding-left: 20px;
        }
        ul {
            margin-top: 7px;
        }
        .box ul li a {
            font-size: 12px;
            text-decoration: none;
            color: gray;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="one">
            <h3 class="title">品优购快报</h3>
        </div>
        <div class="two">
            <ul>
                <li><a href="#">【特惠】爆款耳机5折秒！</a></li>
                <li><a href="#">【特惠】母亲节，健康好礼低至5折</a></li>
                <li><a href="#">【特惠】爆款耳机5折秒！</a></li>
                <li><a href="#">【特惠】9.9元洗100张照片</a></li>
                <li><a href="#">【特惠】长虹立省空调立省1000</a></li>
            </ul>
        </div>
    </div>
</body>
</html>
```

```html
 li {
    list-style: none;
}
```



#### 圆角边框（重点）

border-radius属性用于设置元素的外边框圆角。

```html
border-radius: length;
```

* 参数值可以为数值或者百分比的形式
* **圆形盒子：length=正方形盒子一半 或者 50%**
* 圆角矩形：length=高度的一半
* 该属性是一个简写属性，可以跟四个值，分别代表左上角、右上角、左下角、右下角（顺时针）
* 分开写：border-top-left-radius



#### 盒子阴影（重点）

CSS3中新增了盒子阴影，我们可以使用box-shadow属性为盒子添加阴影。

语法：

```html
box-shadow: h-shadow v-shadow blur spread color inset;
```

| 值       | 描述                                                  |
| -------- | ----------------------------------------------------- |
| h-shadow | 必需。水平阴影的位置，允许负值                        |
| v-shadow | 必需。垂直阴影的位置，允许负值                        |
| blur     | 可选。模糊距离                                        |
| spread   | 可选。阴影的尺寸                                      |
| color    | 可选。阴影的颜色                                      |
| inset    | 可选。将外部阴影（outset,默认，不能出现）改为内部阴影 |

```html
div {
   box-shadow: 10px 10px 10px 10px rgba(0,0,0,.3);
}
```



#### 文字阴影

可以使用text-shadow属性为文本添加阴影。

```html
text-shadow: h-shadow v-shadow blur color;
```

| 值       | 描述                                                  |
| -------- | ----------------------------------------------------- |
| h-shadow | 必需。水平阴影的位置，允许负值                        |
| v-shadow | 必需。垂直阴影的位置，允许负值                        |
| blur     | 可选。模糊距离                                        |
| color    | 可选。阴影的颜色                                      |

```html
div {
    text-shadow: 5px 5px 6px rgba(0,0,0,.3);
}
```





### 浮动

浮动最典型的应用就是可以让多个块级元素一行内排列显示。

**网页布局第一准则：多个块级元素总i昂排列找标准流，多个块级元素横向排列找浮动**。



#### 布局方式

CSS提供了三种传统布局方式（简单说，就是盒子如何进行排列顺序）：

* 普通流（标准流）
* 浮动
* 定位



##### 标准流（普通流/文档流）

就是标签按照规定好的默认方式排列。

1. 块级元素会独占一行，从上向下顺序排列。常用元素：`div`，`hr`，`p`，`h1~h6`，`ul`，`ol`，`dl`，`form`，`table`
2. 行内元素会按照顺序，从左到右顺序排列，碰到父元素边缘则自动换行。常用元素：`span`，`a`，`i`，`em`等



#### 浮动

float属性用于创建浮动框，将其移动到一遍，直到左边缘或右边缘及包含块或另一个浮动框的边缘。

```html
选择器 { float:属性值; }
```

| 属性值 | 描述         |
| ------ | ------------ |
| none   | 元素不浮动   |
| left   | 元素向左浮动 |
| right  | 元素向右浮动 |



#### 浮动特性（重难点）

1. 浮动元素会脱离标准流
2. 浮动的元素会一行内显示并且元素顶部对齐
3. 浮动的元素会具有行内块元素的特性

* **脱离标准普通流的控制（浮）移动到指定位置（动），俗称脱标**
* **浮动的盒子不再保留原先的位置**

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809220809307.png" alt="image-20200809220809307" style="zoom:67%;" />



<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809220935797.png" alt="image-20200809220935797" style="zoom:67%;" />

![image-20200809221058103](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809221058103.png)

* **如果多个盒子都设置了浮动，则他们会按照属性值一行内显示并且顶端对齐排列**

![image-20200809221456178](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809221456178.png)

* **浮动的元素是互相贴靠在一起的（不会有缝隙），如果父级宽度装不下这些浮动的盒子，多出的盒子会另起一行对齐**。

![image-20200809221422947](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809221422947.png)

* 只要添加浮动之后具有**行内块**相似的特性。
* 如果块级盒子没有设置宽度，默认和父级一样宽，但是添加浮动后，他的大小根据内容来决定。
* 浮动的盒子中间是没有缝隙的，是紧挨着一起的。



#### 浮动元素和标准流父级搭配使用

![image-20200809222836971](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809222836971.png)

先用标准流的父元素排列上下位置，之后内部子元素采取浮动排列左右位置，符合网页布局第一准则。



##### 实践：小米布局案例

![image-20200809230742006](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809230742006.png)

![image-20200809230809860](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809230809860.png)

![image-20200809230832477](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809230832477.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box {
            width: 1200px;
            height: 460px;
            background-color: pink;
            margin: 0 auto;
        }
        .left {
            float: left;
            height: 460px;
            width: 230px;
            background-color: purple;
        }
        .right {
            float: left;
            width: 970px;
            height: 460px;
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <div class="box">
    <div class="left">左</div>
    <div class="right">右</div>
    </div>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        .box li {
            float: left;
            margin: 0 14px;
            list-style: none;
            width: 285px;
            height: 285px;
            background-color: pink;
        }
        .box {
            height: 285px;
            width: 1226px;
            background-color: black;
        }
        .box .four {
            margin-right: 0;
        }
        .box .one {
            margin-left: 0;
        }
    </style>
</head>
<body>
    <ul class="box">
        <li class="one">1</li>
        <li class="two">2</li>
        <li class="three">3</li>
        <li class="four">4</li>
    </ul>
</body>
</html>
```

* **网页布局第二准则：先设置盒子大小，之后设置盒子的位置。**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box {
            width: 1226px;
            height: 615px;
            margin: 0 auto;
            background-color: pink;
        }
        .left {
            float: left;
            height: 615px;
            width: 234px;
            background-color: blueviolet;
        }
        .right {
            float: left;
            width: 992px;
            height: 615px;
            background-color: skyblue;
        }
        .right>div {
            float: left;
            width: 234px;
            height: 300px;
            background-color: pink;
            margin-left: 14px;
            margin-bottom: 14px;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="left"></div>
        <div class="right">
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
            <div>5</div>
            <div>6</div>
            <div>7</div>
            <div>8</div>
        </div>
    </div>
</body>
</html>
```



#### 常见网页布局

![image-20200809231043794](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809231043794.png)

![image-20200809231058873](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809231058873.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        li {
            list-style: none;
        }
        .top {
            height: 50px;
            background-color: gray;
        }
        .banner {
            width: 980px;
            height: 150px;
            margin: 10px auto;
            background-color: gray;
        }
        .box {
            width: 980px;
            height: 300px;
            margin: 0 auto;
            background-color:pink ;
        }
        .box li{
            float: left;
            width: 237px;
            height: 300px;
            background-color: gray;
            margin-right: 10px;
        }
        .box .last {
            margin-right: 0px;
        }
        .footer {
            height: 200px;
            background-color: gray;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="top">top</div>
    <div class="banner">banner</div>
    <div class="box">
        <ur>
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li class="last">4</li>
        </ur>
    </div>
    <div class="footer">footer</div>
</body>
</html>
```

**通栏不需要指定宽只需要指定高。**



#### 浮动布局注意点

1. 浮动和标准流的父盒子搭配：**先用标准流的父元素排列上下位置，之后内部子元素采用浮动排列左右位置**
2. 一个元素浮动了，理论上其余的兄弟元素也要浮动：一个盒子里面右多个子盒子，如果其中一个盒子浮动了，那么其他兄弟也应该浮动，以防引起问题。**浮动的盒子之后影响后面的标准流不会影响前面的标准流。**



#### 清除浮动

![image-20200809233631193](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809233631193.png)

清除浮动本质就是清楚浮动元素造成的影响。

如果父盒子本身有高度，则不需要清除浮动。

**清除浮动之后，父级就会根据浮动的盒子自动检测高度。父级有了高度，就不会影响下面的标准流了。**

语法：

```html
选择器 { clear:属性值; }
```

| 属性值 | 描述                                           |
| ------ | ---------------------------------------------- |
| left   | 不允许左侧左浮动元素（清除左侧浮动元素的影响） |
| right  | 不允许左侧右浮动元素（清除右侧浮动元素的影响） |
| both   | 同时清除左右两侧浮动的影响                     |

**几乎只用`clear:both;`。**

**清除浮动的策略是：闭合浮动。**

 

##### 清除浮动的方法

1. 额外标签法（隔墙法），W3C推荐
2. 父级添加overflow属性
3. 父级添加after伪元素
4. 父级添加双伪元素



##### 额外标签法

额外标签法也称隔墙法。

额外标签法会在浮动元素末尾添加一个空的标签。例如`<div style="clear:both"></div>`，或者其他标签（例如`<br />`等)

**注意：要求这个新的空标签必须是块级元素。**

![image-20200809235313163](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809235313163.png)



##### 父级添加overflow

可以给父级添加overflow属性，将其属性值为hidden、auto或scroll。

```html
.box {
    overflow: hidden;
}
```

缺点：无法显示溢出的部分。



#####after伪元素法

:after方式是额外标签法的升级版。也是给父元素添加。

![image-20200809235816706](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809235816706.png)

![image-20200809235925954](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200809235925954.png)



##### 双伪元素清除浮动

也是给父元素添加。

![image-20200810000204939](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810000204939.png)

![image-20200810000307192](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810000307192.png)



#### 清除浮动总结

为什么要清除浮动：

* 父级没高度
* 子盒子浮动了
* 影响下面布局了，就应该清除浮动

| 清除浮动的方式         | 优点               | 缺点                             |
| ---------------------- | ------------------ | -------------------------------- |
| 额外标签法（隔墙法）   | 通俗易懂，书写方便 | 天机许多无意义的标签，结构化较差 |
| 父级`overflow:hidden;` | 书写简单           | 溢出隐藏                         |
| 父级after伪元素        | 结构语义化正确     | 由于IE6-7不支持after，兼容性问题 |
| 父级双伪元素           | 结构语义化正确     | 由于IE6-7不支持after，兼容性问题 |



#### PS切图

![image-20200810151624563](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810151624563.png)



##### 图层切图

![image-20200810152756378](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810152756378.png)



##### 切片切图

![image-20200810153555475](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810153555475.png)



##### PS插件切图

![image-20200810154009831](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810154009831.png)



####综合案例

##### 准备素材和工具

![image-20200810155209908](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810155209908.png)

##### 案例准备工作

![image-20200810155702999](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810155702999.png)



##### CSS属性书写顺序（重点）

建议遵循以下顺序:

1. 布局定位属性: display / position/ float/ clear/ visibility/ overflow (建议display第-一个写 ,毕竟关系到模式)
2. 自身属性: width/ height / margin/ padding / border/ background
3. 文本属性: color/ font / text- decoration/ text-align/ vertical-align/ white- space / break-word
4. .其他属性(CSS3 ) : content/ cursor / border -radius/ box shadow/ text shadow/ background:linear- gradint

![image-20200810161259157](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810161259157.png)



#####页面布局整体思路

![image-20200810162019839](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810162019839.png)



##### 确定版心

![image-20200810165551491](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810165551491.png)



##### 头部制作

![image-20200810165805616](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810165805616.png)

![image-20200810175036976](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810175036976.png)

html：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="header w">
        <!-- 标志 -->
        <div class="logo">
            <img src="images/logo_03.png" alt="">
        </div>
        <!-- 导航栏 -->
        <div class="nav">
            <ul>
                <li><a href="#">首页</a></li>
                <li><a href="#">课程</a></li>
                <li><a href="#">职业规划</a></li>
            </ul>
        </div>
        <!-- 搜索模块 -->
        <div class="search">
            <input type="text" value="输入关键词">
            <button></button>
        </div>
        <!-- 用户模块 -->
        <div class="user">
            <img>qq-lilei
        </div>
    </div>
</body>
</html>
```

CSS：

```css
* {
    margin: 0;
    padding: 0;
}
.w {
    width: 1200px;
    margin: auto;
}
li {
    list-style: none;
}
.header {
    height: 42px;
    background-color: pink;
    margin: 30px auto;
}
.logo {
    float: left;
    width: 198px;
    height: 42px;
    background-color: blueviolet;
}
.nav {
    float: left;
    margin-left: 60px;
}
.nav ul li {
    display: inline-block;
    margin: 0 15px;
}
.nav ul li a {
    display: block;
    height: 42px;
    padding: 0 10px;
    line-height: 42px;
    font-size: 18px;
    color: #050505;
    text-decoration: none;
}
.nav ul li a:hover {
    border-bottom: 2px solid #00a4ff;
    color: #00a4ff;
}
.search {
    float: left;
    width: 412px;
    height: 42px;
    background-color: skyblue;
    margin-left: 50px;
}
.search input {
    float: left;
    width: 345px;
    height: 40px;
    border: 1px solid skyblue;
    border-right: 0;
    padding-left: 15px;
    color: #bfbfbf;
    font-size: 14px;
}
.search button {
    float: left;
    width: 50px;
    height: 42px;
    border: 0;
    background-color: #00a4ff;
}
.user {
    float: right;
    line-height: 42px;
    margin-right: 30px;
    font-size: 14px;
    color: #666;
}
```



##### banner制作

![image-20200810223804746](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200810223804746.png)



##### 精品推荐小模块

![image-20200814151350229](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200814151350229.png)

* 大盒子水平居中goods精品,注意此处有个盒子阴影
* 1号盒子是标题H3左侧浮动
* 2号盒子里面放链接左侧浮动，goods-item 距离可以控制链接的左右外边距(注意行内元素只给左右内外边距)
* 3号盒子右浮动mod修改



##### 精品推荐大模块

![image-20200813153235890](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200813153235890.png)

* 1号盒子为最大的盒子，box版心水平居中对齐
* 2号盒子为上面部分, box-hd --里面左侧标题H3左浮动，右侧链接a右浮动
* 3号盒子为底下部分, box-bd--里面是无序列表,有10个小li组成
* 小li外边距的问题,这里有个小技巧:给box- hd宽度为1215就可以一行装开5个li 



##### 底部模块

![image-20200814152039387](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200814152039387.png)

* 1号盒子是通栏大盒子,底部footer给高度,底色是白色
* 2号盒子版心水平居中
* 3号盒子版权copyright左对齐
* 4号盒子链接组links 右对齐



##### 综合案例：学成网网站

html文件：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- 头部区域 -->
    <div class="header w">
        <!-- 标志 -->
        <div class="logo">
            <img src="images/logo_03.png" alt="">
        </div>
        <!-- 导航栏 -->
        <div class="nav">
            <ul>
                <li><a href="#">首页</a></li>
                <li><a href="#">课程</a></li>
                <li><a href="#">职业规划</a></li>
            </ul>
        </div>
        <!-- 搜索模块 -->
        <div class="search">
            <input type="text" value="输入关键词">
            <button></button>
        </div>
        <!-- 用户模块 -->
        <div class="user">
            <img>qq-lilei
        </div>
    </div>
    <!-- banner部分 -->
    <div class="banner">
        <!-- 版心 -->
        <div class="w">
            <div class="subnav">
                <ul>
                    <li><a href="#">前端开发
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">后端开发
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">移动开发
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">人工智能
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">商业预测
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">云计算大数据
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">运维测试
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">UI设计
                        <span>&gt;</span>
                    </a></li>
                    <li><a href="#">产品
                        <span>&gt;</span>
                    </a></li>
                </ul>
            </div>
            <!-- 课程表 -->
            <div class="course">
                <h2>我的课程表</h2>
                <div class="bd">
                    <ul>
                        <li>
                            <h4>继续学习 程序语言设计</h4>
                            <p>正在学习—使用对象</p>
                        </li>
                        <li>
                            <h4>继续学习 程序语言设计</h4>
                            <p>正在学习—使用对象</p>
                        </li>
                        <li>
                            <h4>继续学习 程序语言设计</h4>
                            <p>正在学习—使用对象</p>
                        </li>
                    </ul>
                    <a href="#" class="more">全部课程</a>
                </div>
            </div>
        </div>
    </div>
    <!-- 精品推荐 -->
    <div class="goods w">
        <h3>精品推荐</h3>
        <ul>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
        </ul>
        <a href="#" class="mod">修改兴趣</a>
    </div>
    <!-- box核心内容区域 -->
    <div class="box w">
        <div class="box-hd">
            <h3>精品推荐</h3>
            <a href="#">查看全部</a>
        </div>
        <div class="box-bd">
            <ul class="clearfix">
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>Think PHP 5.0博客系统实战项目演练</h4>
                    <div class="info">
                        <span>高级</span> · 1125在学习
                    </div>
            </ul>
        </div>
    </div>
    <!-- 尾部footer -->
    <div class="footer">
        <div class="w">
            <div class="copyright">
                <img src="images/logo_03.png" alt="">
                <p>学成在线致力于普及中国最好的教育它与中国-流大学和机构合作提供在线课程。<br>
                    2017年XTCG Ino.保留所有权利。-沪ICP备15025210号
                </p>
                <a href="#">下载APP</a>
            </div>
            <div class="links">
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">关于</a></dd>
                    <dd><a href="#">管理团队</a></dd>
                    <dd><a href="#">工作机会</a></dd>
                    <dd><a href="#">客户服务</a></dd>
                    <dd><a href="#">帮助</a></dd>
                </dl>
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">关于</a></dd>
                    <dd><a href="#">管理团队</a></dd>
                    <dd><a href="#">工作机会</a></dd>
                    <dd><a href="#">客户服务</a></dd>
                    <dd><a href="#">帮助</a></dd>
                </dl>
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">关于</a></dd>
                    <dd><a href="#">管理团队</a></dd>
                    <dd><a href="#">工作机会</a></dd>
                    <dd><a href="#">客户服务</a></dd>
                    <dd><a href="#">帮助</a></dd>
                </dl>
            </div>
        </div>
    </div>
</body>
</html>
```

CSS文件：

```css
* {
    margin: 0;
    padding: 0;
}
.w {
    width: 1200px;
    margin: auto;
}
.clearfix:before,.clearfix:after {
    content:"";
    display: table;
}
.clearfix:after {
    clear: both;
}
.clearfix {
    *zoom:1;
}
li {
    list-style: none;
}
a {
    text-decoration: none;
}
.header {
    height: 42px;
    background-color: whites;
    margin: 30px auto;
}
.logo {
    float: left;
    width: 198px;
    height: 42px;
    background-color: white;
}
.nav {
    float: left;
    margin-left: 60px;
}
.nav ul li {
    display: inline-block;
    margin: 0 15px;
}
.nav ul li a {
    display: block;
    height: 42px;
    padding: 0 10px;
    line-height: 42px;
    font-size: 18px;
    color: #050505;
}
.nav ul li a:hover {
    border-bottom: 2px solid #00a4ff;
    color: #00a4ff;
}
.search {
    float: left;
    width: 412px;
    height: 42px;
    background-color: skyblue;
    margin-left: 50px;
}
.search input {
    float: left;
    width: 345px;
    height: 40px;
    border: 1px solid skyblue;
    border-right: 0;
    padding-left: 15px;
    color: #bfbfbf;
    font-size: 14px;
}
.search button {
    float: left;
    width: 50px;
    height: 42px;
    border: 0;
    background-color: #00a4ff;
}
.user {
    float: right;
    line-height: 42px;
    margin-right: 30px;
    font-size: 14px;
    color: #666;
}
.banner {
    height: 421px;
    background-color: blue;
}
.banner .w {
    height: 421px;
    background: url(img/banner2.png) no-repeat top center;
}
.subnav {
    float: left;
    width: 190px;
    height: 421px;
    background: rgba(0, 0, 0, 0.2);
}
.subnav ul li {
    height: 45px;
    line-height: 45px;
    padding: 0 20px;
}
.subnav ul li a {
    font-size: 14px;
    color: #fff;
}
.subnav ul li a span {
    float: right;
}
.subnav ul li a:hover {
    color: #00a4ff;
}
.course {
    float: right;
    width: 230px;
    height: 300px;
    background-color: #fff;
    /* 浮动的盒子不会有外边距合并的问题 */
    margin-top: 50px;
}
.course h2 {
    height: 48px;
    background-color: #9bceea;
    text-align: center;
    line-height: 48px;
    font-size: 18px;
    color: white;
}
.bd {
    padding: 0 20px;
}
.bd ul li {
    padding: 14px 0;
    border-bottom: 1px solid #a5a5a5;
}
.bd ul li h4 {
    font-size: 18px;
    color: #4e4e4e;
}
.bd ul li p {
    font-size: 12px;
    color: #a5a5a5;
}
.bd .more {
    display: block;
    height: 35px;
    border: 1px solid #00a4ff;
    text-align: center;
    line-height: 35px;
    color: #00a4ff;
    font-size: 16px;
    font-weight: 700;
    margin-top: 4px;
}
.goods {
    height: 60px;
    background-color: #fff;
    margin-top: 10px;
    box-shadow: 0 2px 3px 3px rgba(0, 0, 0, 0.1);
    /* 行高会继承给三个孩子 */
    line-height: 60px;
}
.goods h3 {
    float: left;
    margin-left: 30px;
    color: #00a4ff;
    font-size: 16px;
}
.goods ul {
    float: left;
    margin-left: 30px;
}
.goods ul li {
    float: left;
}
.goods ul li a {
    padding: 0 30px;
    font-size: 16px;
    border-left: 1px solid #a5a5a5;
}
.mod {
    float: right;
    margin-right: 30px;
    color: #00a4ff;
    font-size: 14px;
}
.box {
    margin-top: 30px;
}
.box-hd {
    height: 45px;
}
.box-hd h3 {
    float: left;
    font-size: 20px;
    color: #494949;
}
.box-hd a {
    float: right;
    font-size: 12px;
    color: #a5a5a5;
    margin-top: 10px;
    margin-right: 30px;
}
.box-bd ul {
    width: 1225px;
}
/* 把li的父亲ul修改的足够宽一行能装五个盒子就不会换行了 */
.box-bd ul li {
    float: left;
    width: 228px;
    height: 270px;
    background-color: #fff;
    margin-right: 15px;
    margin-bottom: 15px;
}
.box-bd ul li img {
    width: 100%;
}
.box-bd ul li h4 {
    margin: 20px 20px 20px 25px;
    font-size: 14px;
    color: #050505;
    font-weight: 400;
}
.box-bd .info {
    margin: 0 20px 0 25px;
    font-size: 12px;
    color: #999;
    font-weight: 400;
}
.box-bd .info span {
    color: #ff7c2d;
}
.footer {
    height: 415px;
    background-color: aliceblue;
}
.footer .w {
    padding-top: 35px;
}
.copyright {
    float: left;
}
.copyright p {
    font-size: 12px;
    color: #666;
    margin-top: 20px;
    margin-bottom: 15px;
}
.copyright a {
    display: block;
    width: 118px;
    height: 33px;
    border: 1px solid #00a4ff;
    text-align: center;
    line-height: 33px;
    color: #00a4ff;
    font-size: 16px;
}
.links {
    float: right;
}
.links dl {
    float: right;
    margin-left: 100px;
}
.links dl dt {
    font-size: 16px;
    color: #333;
    margin-bottom: 15px;
} 
.links dl dd {
    font-size: 12px;
    color: #333;
}
```



### CSS定位

浮动可以让多个块级盒子- 行没有缝隙排列显示,经常用于横向排列盒子。

**定位**则是可以让盒子自由的在某个盒子内移动位置或者固定屏幕中某个位置,并且可以压住其他盒子。



####定位的组成

定位:将盒子定在某一个位置 ,所以**定位也是在摆放盒子,按照定位的方式移动盒子。**

**定位=定位模式+边偏移。**

定位模式用于指定一个元素在文档中的定位方式。 边偏移则决定了该元素的最终位置。



##### 定位模式

定位模式决定元素的定位方式,它通过CSS的position属性来设置,其值可以分为四个:

| 值         | 语义         |
| ---------- | ------------ |
| `static`   | **静态**定位 |
| `relative` | **相对**定位 |
| `absolute` | **绝对**定位 |
| `fixed`    | **固定**定位 |



##### 边偏移

边偏移就是定位的盒子移动到最终位置。有**top、bottom. left 和right 4个属性**。

| 边偏移   | 示例           | 描述                                             |
| -------- | -------------- | ------------------------------------------------ |
| `top`    | `top: 80px`    | 顶端偏移量，定义元素相对于其父元素上边线的距离。 |
| `bottom` | `bottom: 80px` | 底部偏移量，定义元素相对于其父元素下边线的距离。 |
| `left`   | `left: 80px`   | 左侧偏移量，定义元素相对于其父元素左边线的距离。 |
| `right`  | `right: 80px`  | 右侧偏移量，定义元素相对于其父元素右边线的距离。 |



#### 定位方式

#####静态定位static（了解）

静态定位是元素的默认定位方式，无定位的意思。

语法：

```html
选择器 { position: static; }
```

* 静态定位按照标准流特性摆放位置,它没有边偏移
* 静态定位在布局时很少用到



##### 相对定位relative（重要）

相对定位是元素在移动位置的时候，是相对于它原来的位置来说。

语法：

```html
选择器 { position: relative; }
```

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200814162711209.png" alt="image-20200814162711209" style="zoom:67%;" />



相对定位的特点：（务必记住）

* 它是**相对于自己原来的位置来移动的**(移动位置的时候参照点是自己原来的位置)。
* 原来在标准流的位置继续占有,后面的盒子仍然以标准流的方式对待它。( 不脱标,继续保留原来位置)

<img src="file:///C:\Users\CXY\Documents\Tencent Files\1018459119\Image\C2C\A(H)X57[SIU}448@BU7AL05.png" alt="img" style="zoom:67%;" />



#####绝对定位absolute（重要）

绝对定位是元素在移动位置的时候，是相对于它的祖先元素来说的。

语法：

```html
选择器 { position: absolute; }
```

绝对定位的特点：（务必记住）

* 如果没有祖先元素或者祖先元素没有定位,则以浏览器为准定位( Document文档)。

<img src="file:///C:\Users\CXY\Documents\Tencent Files\1018459119\Image\C2C\K[I2B{6$K0YS]RFSD}UVK{C.png" alt="img" style="zoom: 80%;" />

<img src="file:///C:\Users\CXY\Documents\Tencent Files\1018459119\Image\C2C\8[I_18~9`S{AX_20S_3_]IF.png" alt="img" style="zoom:67%;" />

* 如果祖先元素有定位(相对、绝对、固定定位) , 则以**最近一级的有定位**祖先元素为参 考点移动位置。

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200814172745058.png" alt="image-20200814172745058" style="zoom: 50%;" />

<img src="file:///C:\Users\CXY\Documents\Tencent Files\1018459119\Image\C2C\0LVL9{S[ITL9Y9}X3C]SXFT.png" alt="img" style="zoom: 50%;" />

* 绝对定位不再占有原先的位置（脱标）

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200814173545498.png" alt="image-20200814173545498" style="zoom: 67%;" />



##### 子绝父相

子级绝对定位,不会占有位置,可以放到父盒子里面的任何一个地方,不会影响其他的兄弟盒子。

父盒子需要加定位限制子盒子在父盒子内显示。

父盒子布局时,需要占有位置,因此父亲只能是相对定位。

这就是子绝父相的由来,所以相对定位经常用来作为绝对定位的父级。

**总结:因为父级需要占有位置,因此是相对定位，子盒子不需要占有位置,则是绝对定位**

当然，子绝父相不是永远不变的，如果父元素不需要占有位置,子绝父绝也会遇到。



##### 固定定位fixed（重要）

固定定位是元素固定于浏览器可视区的位置。主要使用场景:**可以在浏览器页面滚动时元素的位置不会改变。**

语法：

```html
选择器 { position: fixed; }
```

固定定位的特点：（务必记住）

* 以浏览器的可视窗口为参照点移动元素。

​       跟父元素没有任何关系。

​       不随滚动条滚动。

* 固定定位不在占有原先的位置。

​       固定定位也是脱标的,其实固定定位也可以看做是一种特    殊的绝对定位。

###### 固定定位小技巧：固定在版心右侧位置（算法）

小算法：

1. 让固定定位的盒子left: 50%.走到浏览器可视区(也可以看做版心)的-半位置。
2. 让固定定位的盒子margin-left:版心宽度的一半距离。多走 版心宽度的一半位置

就可以让固定定位的盒子贴着版心右侧对齐了。

![image-20200815152720140](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200815152720140.png)

```html
.W {
   width: 800px;
   height: 1400px ;
   background-color: pink;
   margin: 0 auto ;
}
.fixed {
   position: fixed;
   /* 1.走浏览器宽度的一半*/
   left: 50%;
   /* 2.利用margin 走版心盒子宽度的一 半距离*/
   margin-left: 405px;
   width: 50px;
   height: 150px; 
   background-color: skyblue;
}
```



#####粘性定位sticky（了解）

粘性定位可以被认为是相对定位和固定定位的混合。

语法：

```html
选择器 { position: sticky; top: 10px; }
```

粘性定位的特点：

* 以浏览器的可视窗口为参照点移动元素(固定定位特点)
* 粘性定位占有原先的位置(相对定位特点)
* 必须添加top、left、 right. bottom其中一个才有效



##### 定位的总结

| 定位模式         | 是否脱标       | 移动位置           | 是否常用   |
| ---------------- | -------------- | ------------------ | ---------- |
| static静态定位   | 否             | 不能使用边偏移     | 很少       |
| relative相对定位 | 否(占有位置)   | 相对于自身位置移动 | 常用       |
| absolute绝对定位 | 是(不占有位置) | 带有定位的父级     | 常用       |
| fixed固定定位    | 是(不占有位置) | 浏览器可视区       | 常用       |
| sticky粘性定位   | 否(占有位置)   | 浏览器可视区       | 当前阶段少 |

*  一定记住相对定位、固定定位、绝对定位两个大的特点: 1. 是否占有位置(脱标否) 2. 以谁为基准点移动位置。
* 学习定位重点学会子绝父相。



##### 定位叠放次序z-index

在使用定位布局时,可能会出现盒子重叠的情况。此时,可以使用z-index来控制盒子的前后次序(z轴)。

语法：

```html
选择器 { z-index: 1; }
```

* 数值可以是正整数、负整数或0,默认是auto ,数值越大,盒子越靠上
* 如果属性值相同,则按照书写顺序,后来居上
* 数字后面不能加单位
* 只有定位的盒子才有z-index属性



##### 定位的拓展

###### 绝对定位的盒子居中

加了绝对定位的盒子不能通过margin:0 auto水平居中,但是可以通过以下计算方法实现水平和垂直居中。

1. left: 50%; :让盒子的左侧移动到父级元素的水平中心位置。
2. margin-left: -100px; :让盒子向左移动自身宽度的一半。

```css
.box {
    position: absolute;
    /*1.Left走50%父容器宽度的一半*/
    left: 50%;
    /* 2. margin 负值往左边走自己盒子宽度的一半*/
    margin-left: -100px;
    width: 200px;
    height: 200px ;
    background-color: pink;
    margin: auto;
}

```



###### 定位特殊特性

绝对定位和固定定位也和浮动类似。

* 行内元素添加绝对或者固定定位,可以直接设置高度和宽度。
* 块级元素添加绝对或者固定定位,如果不给宽度或者高度,默认大小是内容的大小。



###### 脱标的盒子不会触发外边距塌陷

浮动元素、绝对定位(固定定位)元素的都不会触发外边距合并的问题。



###### 绝对定位（固定定位）会完全压住盒子

浮动元素不同。只会压住它下面标准流的盒子。但是不会压住下面标准流盒子里面的文字(图片)

但是绝对定位(固定定位)会压住下面标准流所有的内容。

浮动之所以不会压住文字,因为浮动产生的目的最初是为了做文字环绕效果的。文字会围绕浮动元素

```css
.box {
    /* 浮动的元素 不会压住下面标准流的文字*/ 
    float: left;
    width: 150px;
    height: 150px; 
    background-color: pink ;
}
```



####综合案例：淘宝焦点图布局

1. 大盒子我们类名为: tb-promo 淘宝广 告
2. 里面先放一张图片
3. 左右两个按钮用链接就好了。左箭头 prev右箭头 next
4. 底侧小圆点ul继续做。类名为 promo-nav

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>淘宝轮播图做法</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        li {
            list-style: none;
        }
        .tb-promo {
            position: relative;
            width: 520px;
            height: 280px;
            background-color: pink;
            margin: 100px auto;
        }
        .tb-promo img {
            width: 520px;
            height: 280px;
        }
        .prev,
        .next {
            position: absolute;
            top: 50%;
            margin-top: -15px;
            /* 加了绝对定位的盒子可以直接设置宽度和高度 */
            width: 20px;
            height: 30px;
            background: rgba(0,0,0,.3);
            text-align: center;
            line-height: 30px;
            color: #fff;
            text-decoration: none;
        }
        .prev {
            /* 如果一个 盒于既有Left属性也有right属性，则默认会执行Left属性同理top bottom 会执行 top */
            left: 0;    
            border-top-right-radius: 15px;
            border-bottom-right-radius: 15px;
        }
        .next {
            right: 0;
            border-top-left-radius: 15px;
            border-bottom-left-radius: 15px;
        }
        .promo-nav {
            position: absolute;
            bottom: 15px;
            left: 50%;
            margin-left: -35px;
            width: 70px;
            height: 13px;
            background-color: rgba(255,255,255,.3);
            border-radius: 7px;
        }
        .promo-nav li {
            float: left;
            width: 8px;
            height: 8px;
            background-color: #fff;
            border-radius: 50%;
            margin: 3px;
        }
        /* 不要忘记权重问题 */
        .promo-nav .selected {
            background-color: #ff5000;
        }
    </style>
</head>
<body>
    <div class="tb-promo">
        <img src="images/tb.jpg" alt="">
        <!-- 左侧按钮 -->
        <a href="#" class="prev">&lt;</a>
        <!-- 右侧按钮 -->
        <a href="#" class="next">&gt;</a>
        <!-- 小圆点 -->
        <ul class="promo-nav">
            <li class="selected"></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </div>
</body>
</html>
```



#### 网页布局总结

通过盒子模型,清楚知道大部分html标签是一个盒子。
通过CSS浮动、定位可以让每个盒子排列成为网页。
一个完整的网页,是标准流、浮动、定位一起完成布局的,每个都有自己的专门用法。
**标准流**
可以让盒子上下排列或者左右排列, 垂直的块级盒子显示就用标准流布局。（擅长上下排列）
**浮动**
可以让多个块级元素一行显示或者左右对齐盒子 ,多个块级盒子水平显示就用浮动布局。（块级盒子一行排列）
**定位**
定位最大的特点是有层叠的概念,就是可以让多个盒子前后叠压来显示。如果元素自由在某个盒子内移动就用定位布局。



#### 元素的显示与隐藏

类似网站广告,当我们点击关闭就不见了,但是我们重新刷新页面,会重新出现

本质:让一个元素在页面中隐藏或者显示出来。

* display 显示隐藏
* visibility 显示隐藏
* overflow 溢出显示隐藏



##### display属性（超重要）

display属性用于设置-个元素应如何显示。

* display: none ;隐藏对象
* display : block ;除了转换为块级元素之外,同时还有显示元素的意思

**display : block ;除了转换为块级元素之外,同时还有显显元索的意思**



#####visibility可见性

visibility属性用于指定一个元素应可见还是隐藏。

* visibility : visible;元素可视
* visibility : hidden;元素隐藏

**visibility隐藏元素后,继续占有原来的位置。**

如果隐藏元素想要原来位置，就用visibility : hidden
如果隐藏元素不想要原来位置，就用display : none (用处更多重点)



##### overflow溢出

overflow属性指定了如果内容溢出一个元素的框(超过其指定高度及宽度)时,会发生什么。

| 属性值  | 描述                                       |
| ------- | ------------------------------------------ |
| visible | 不剪切内容也不添加滚动条                   |
| hidden  | 不显示超过对象尺寸的内容，超出的部分隐藏掉 |
| scroll  | 不管超出内容否，总是显示滚动条             |
| auto    | 超出自动显示滚动条，不超出不显示滚动条     |

一般情况下 我们都不想让溢出的内容 显示出来,因为溢出的部分会影响布局。
但是如果有定位的盒子,请慎用overflow:hidden因为它会隐藏多余的部分。



##### 总结

* display显示隐藏元素但是不保留位置
* visibility显示隐藏元素但是保留原来的位置
* overflow溢出显示隐藏但是只是对于溢出的部分处理



##### 综合案例：土豆网鼠标经过显示遮罩

核心原理:原先半透明的黑色遮罩看不见，鼠标经过大盒子,就显示出来。
遮罩的盒子不占有位置，就需要用绝对定位和display配合使用。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>土豆网隐藏遮罩</title>
    <style>
        .tudou {
            position: relative;
            width: 444px;
            height: 320px;
            margin: 30px auto;
        }
        .tudou img {
            width: 100%;
            height: 100%;
        }
        .mask {
            display: none;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,.4) url(images/arr.png) no-repeat center;
        }
        /* 当我们鼠标经过了 遮罩层显示出来 */
        .tudou:hover .mask {
            /* 显示元素 */
            display: block;
        }
    </style>
</head>
<body>
    <div class="tudou">
        <div class="mask"></div>
        <img src="images/tudou.jpg" alt="">
    </div>
</body>
</html>
```



### CSS高级技巧

#### 精灵图

一个网页中往往会应用很多小的背景图像作为修饰，当网页中的图像过多时，服务器就会频繁地接收和发送请求图片，造成服务器请求压力过大，这将大大降低页面的加载速度。

因此，为了有效地减少服务器接收和发送请求的次数，提高页面的加载速度，出现了**CSS精灵技术**(也称CSS Sprites、CSS雪碧)。



##### 精灵图（sprites）的使用

**使用精灵图核心:**

* 精灵技术主要针对于背景图片使用。就是把多个小背景图片整合到-张大图片中。
* 这个大图片也称为sprites精灵图或者雪碧图
* 移动背景图片位置,此时可以使用background-position.
* 移动的距离就是这个目标图片的x和y坐标。注意网页中的坐标有所不同
* 因为一般情况下都是往上往左移动,所以数值负值。
* 使用精灵图的时候需要精确测量,每个小背景图片的大小和位置。

**使用精灵图核心总结:**

* 精灵图主要针对于小的背景图片使用。
* 主要借助于背景位置来实现--background-position.
* 一般情况下精灵图都是负值。( 千万注意网页中的坐标: x轴右边走是正值,左边走是负值，y轴同理。)



##### 实践案例

![image-20200817162632322](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200817162632322.png)



#### 字体图标

字体图标使用场景:主要用于显示网页中通用、常用的一些小图标。
精灵图是有诸多优点的,但是缺点很明显。

* 图片文件还是比较大的。
* 图片本身放大和缩小会失真。
* 一旦图片制作完毕想要更换非常复杂。

此时,有一种技术的出现很好的解决了以上问题,就是**字体图标iconfont**

字体图标可以为前端工程师提供一种方便高效的图标使用方式 ,展示的是图标,本质属于字体。



##### 字体图标的优点

轻量级:一个图标字体要比一系列的图像要小。 一旦字体加载了,图标就会马上渲染出来,减少了服务器请求

灵活性:本质其实是文字,可以很随意的改变颜色、产生阴影、透明效果、旋转等

兼容性:几乎支持所有的浏览器,请放心使用

**注意:**字体图标不能替代精灵技术,只是对工作中图标部分技术的提升和优化。

**总结：**

如果遇到一些结构和样式比较简单的小图标,就用字体图标。

![image-20200817163305809](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200817163305809.png)

如果遇到一些结构和样式复杂一点的小图片 ,就用精灵图。

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200817163329521.png" alt="image-20200817163329521" style="zoom:50%;" />



##### 字体图标的下载

推荐下载网站:

* icomoon字库http://icomoon.io 
  IcoMoon成立于2011年,推出了第一个自定义图标字体生成器,它允许用户选择所需要的图标,使它们成一字型。 该字库内容种类繁多,非常全面,唯-的遗憾 是国外服务器,打开网速较慢。
* 阿里iconfont字库http://www.iconfont.cn/ 
  这个是阿里妈妈M2UX的一个iconfont字体图标字库,包含了淘宝图标库和阿里妈妈图标库。可以使用Al制作图标上传生成。重点是，免费!

![image-20200817170248058](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200817170248058.png)

```html
<style>
/*字体声明*/ 
@font-face {
font-family: ' icomoon' ;
src: ur1( ' fonts/ icomoon. eot?p4ssmb');
src: ur1( 'fonts/ icomoon. eot ?p4ssmb#iefix') format( ' embedded-opentype'),
url( ' fonts/ icomoon. ttf?p4ssmb') format( 'truetype' ),
url( ' fonts/ icomoon. woff?p4ssmb' ) format( ' woff')，
url( ' fonts/ icomoon. svg ?p4ssmb#icomoon') format('svg' );
font-weight: normal;
font-style: normal;
font-display: block ;
}
</style>
```

![image-20200817171325092](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200817171325092.png)



#####字体图标的追加

如果工作中,原来的字体图标不够用了, 我们需要添加新的字体图标到原来的字体文件中。

把压缩包里面的selectionjson从新上传,然后选中自己想要新的图标,从新下载压缩包,并替换原来的文件即可。

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819161139795.png" alt="image-20200819161139795" style="zoom: 67%;" />

![image-20200819161248063](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819161248063.png)



#### CSS三角

```html
.box2 {
     width: 0;
     height: 0;
     border: 10px solid transparent ;
     border-top-color: pink;
     margin: 100px auto;
}
```

网页中常见一些三角形,使用CSS直接画出来就可以,不必做成图片或者字体图标。

一张图,你就知道CSS三角是怎么来的了做法如下:

![image-20200819162859368](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819162859368.png)



##### 实践案例：京东三角对话框

```html
<style>
    .jd {
        position: relative;
        width: 120px;
        height: 249px;
        background-color: pink;
    }
    .jd span {
        position: absolute;
        right: 15px;
        top: -10px;
        width: 0;
        height: 0;
        /*为了照顾兼容性*/
        line-height: 0;
        font-size: 0;
        border: 5px solid transparent;
        border-bottom-color: pink;
    }
</style>
<body>
    <div class="jd">
        <span></span>
    </div>
</body>
```



####CSS用户界面样式

所谓的界面样式,就是更改一些用户操作样式,以便提高更好的用户体验。

* 更改用户的鼠标样式
* 表单轮廓
* 防止表单域拖拽



#####鼠标样式cursor

```html
li { cursor:pointer; }
```

设置或检索在对象上移动的鼠标指针采用何种系统预定义的光标形状。

| 属性值      | 描述      |
| ----------- | --------- |
| default     | 小白 默认 |
| pointer     | 小手      |
| move        | 移动      |
| text        | 文本      |
| not-allowed | 禁止      |

```html
<ul>
<li style=" cursor: default;">我是默认的小白鼠标样式</li>
<li style=" cursor: pointer;">我是鼠标小手样式</li>
<li style=" cursor: move; ">我是鼠标移动样式</1i>
<li style="cursor: text;">我是鼠标文本样式</1i>
<1i style=" cursor: not- allowed;">我是鼠标禁止样式</1i>
</ul>

```



##### 轮廓线outline

给表单添加outline: 0;或者outline: none;样式之后,就可以去掉默认的蓝色边框。

```html
input { outline:none; }
```



##### 防止拖拽文本域resize

实际开发中,我们文本域右下角是不可以拖拽的。

```html
textarea { resize: none; }
```

![image-20200819171809964](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819171809964.png)



#### vertical-align属性应用

CSS的vertical-align属性使用场景:经常用于设置图片或者表单(行内块元素)和文字垂直对齐。

官方解释:用于设置一个元素的垂直对齐方式,但是它只针对于行内元素或者行内块元素有效。

语法：

```html
vertical-align : baseline | top | middle | bottom;
```

| 值       | 描述                                   |
| -------- | -------------------------------------- |
| baseline | 默认，元素放置在父元素的基线上         |
| top      | 把元素的顶端与行中最高元素的顶端对齐   |
| middle   | 把此元素放置在父元素的中部             |
| bottom   | 把元素的顶端与行中最低的元素的顶端对齐 |

![image-20200819211242865](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819211242865.png)

![image-20200819211303069](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819211303069.png)

##### 解决图片底部默认空白缝隙问题

![image-20200819211744013](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819211744013.png)

主要解决方法有两种:

* 给图片添加vertical-align:middle | topl bottom等。(提倡使用的)
* 把图片转换为块级元素display: block;



#### 溢出的文字省略号显示

##### 单行文本溢出

必须满足三个条件：

```css
/*1.先强制一行内显示文本*/
white - space: nowrap;(默认normal自动换行)
/*2.超出的部分隐藏*/
overflow: hidden;
/*3.文字用省略号替代超出的部分*/
text- -overflow: ellipsis;
```

##### 多行文本溢出

多行文本溢出显示省略号,有较大兼容性问题，适合于webKit浏览器或移动端(移动端大部分是webkit内核)

```css
overflow: hidden;
text-overflow: ellipsis;
/*弹性伸缩盒子模型显示*/
display: -webkit-box;
/*限制在一个块元素显示的文本的行数*/
-webkit-line-clamp: 2;
/*设置或检索伸缩盒对象的子元素的排列方式*/
-webkit-box-orient: vertical ;
```

更推荐让后台人员来做这个效果，因为后台人员可以设置显示多少个字,操作更简单。



#### 常见布局技巧

#####margin负值运用

```css
<style>
  ul li {
    float: left;
    list-style: none ;
    width: 150px;
    height: 200px;
    border: 1px solid red;
    margin-left: -1px;
}
</style>
```

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819213433484.png" alt="image-20200819213433484" style="zoom:50%;" />

* 让每个盒子margin往左侧移动-1px正好压住相邻盒子边框
* 鼠标经过某个盒子的时候,提高当前盒子的层级即可(如果没有定位,则加相对定位(保留位置) , 如果有定位,则加z-index)

```css
ul li:hover {
  position: relative;
  border: 1px solid blue; 
}
/* 或者 */
ul li:hover {
/* 如果Li都有定位，则利用z-index提高层级*/
  z-index: 1;
  border: 1px solid blue;
}
```



##### 文字围绕浮动元素

![image-20200819224117276](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819224117276.png)

```html
<style>
    * {
        margin: 0;
        padding: 0;
    }
   .box {
       width: 300px;
       height: 70px;
       background-color: pink;
       margin: 0 auto;
       padding: 5px;
    }
   .pic {
       float: left;
       width: 120px;
       height: 60px ;
       margin-right: 5px;
    }
   .pic img {
       width: 100%;
    }
</style>
<body>
    <div class="box">
        <div>
            <img src="images/img.png" alt="">
        </div>
        <p>
          【集锦】热身赛-巴西0-1秘鲁
        </p>
    </div>
</body>
```



##### 行内块巧妙运用

![image-20200819230202325](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200819230202325.png)

```html
<head>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        .box {
            text-align: center;
        }
        .box a {
            display: inline-block ;
            width: 36px;
            height: 36px;
            background-color:  #f7f7f7 ;
            border: 1px solid #CCC; 
            text-align: center;
            line-height: 36px ;
            text-decoration: none;
            color: #333;
            font-size: 14px;
        }
       .box .prev,
       .box .next {
            width: 85px ;
        }
       .box .current,
       .box .elp {
            width: 85px;
        }
       .box .current,
       .box .elp {
            background-color: #fff;
            border: none;
        }
       .box input {
            height: 36px;
            width: 45px;
            border: 1px solid #CCC;
            outline: none;
        }
       .box button {
            width: 60px;
            height: 36px;
            background-color:  #f7f7f7 ;
            border: 1px solid #CCC; 
        }
    </style>
</head>
<body>
<div class="box">
   <a href="#" class="prev">&lt;&lt;上一页</a>
   <a href=" #”class="current">2</a>
   <a href="#">3</a>
   <a href="#">4</a>
   <a href="#">5</a>
   <a href="#">6</a>
   <a href="#" class="elp">...</a>
   <a href="#" class="next”>&gt;&gt;下一页</a>
    到第
    <input type="text">
    页
    <button>确定</button>
</div>
</body>

```



##### CSS三角强化

![image-20200820092007026](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820092007026.png)

```css
.box1 {
    width: 0;
    height: 0;
    /*把上边框宽度调大*/
    border-top: 100px solid transparent ;
    border-right: 50px solid skyblue ;
    /*左边和下边的边框宽度设置为0*/
    border-bottom: 0 solid blue;
    border-left: 0 solid green,
}

```

![image-20200820092518662](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820092518662.png)

全部：

```html
<html>
    <head>
        <style>
            .price {
                 width: 160px; 
                 height: 24px;
                 line-height: 24px ;
                 border: 1px solid 24px
                 margin: 0 auto;
            }
             .miaosha {
                 position: relative;
                 float: left;
                 width: 90px;
                 height: 100%;
                 background-color: red;
                 text-align: center;
                 color: #fff;
                 font-weight: 700;
                 margin-right: 8px;
            }
            .miaosha i {
                 position: absolute;
                 right: 0;
                 top: 0;
                 width: 0;
                 height: 0;
                 border-color: transparent #fff transparent transparent;
                 border-style: solid;
                 border-width: 24px 10px 0 0;
            }
            .origin {
                font-size: 12px;
                color: gray;
                text-decoration: line-through;
            }
</style>

        </style>
    </head>
    <body>
        <div class="price">
            <span class="miaosha">
                $1650
                <i></i>
            </span>
            <span class="origin">$5650</span>
        </div>
    </body>
</html>
```



#### CSS初始化

不同浏览器对有些标签的默认值是不同的,为了消除不同浏览器对HTML文本呈现的差异,照顾刘览器的兼容，我们需要对CSS初始化。

简单理解: CSS初始化是指重设浏览器的样式。(也称为CSS reset )

每个网页都必须首先进行CSS初始化。

这里我们以京东css初始化代码为例。

```css
/* 把我们所有标签的内外边距清零 */
* {
    margin: 0;
    padding: 0
}
/* em 和 i 斜体的文字不倾斜 */
em,
i {
    font-style: normal
}
/* 去掉li 的小圆点 */
li {
    list-style: none
}

img {
    /* border 0 照顾低版本浏览器 如果 图片外面包含了链接会有边框的问题 */
    border: 0;
    /* 取消图片底侧有空白缝隙的问题 */
    vertical-align: middle
}

button {
    /* 当我们鼠标经过button 按钮的时候，鼠标变成小手 */
    cursor: pointer
}

a {
    color: #666;
    text-decoration: none
}

a:hover {
    color: #c81623
}

button,
input {
    /* "\5B8B\4F53" 就是宋体的意思 这样浏览器兼容性比较好 */
    font-family: Microsoft YaHei, Heiti SC, tahoma, arial, Hiragino Sans GB, "\5B8B\4F53", sans-serif
}

body {
    /* CSS3 抗锯齿形 让文字显示的更加清晰 */
    -webkit-font-smoothing: antialiased;
    background-color: #fff;
    font: 12px/1.5 Microsoft YaHei, Heiti SC, tahoma, arial, Hiragino Sans GB, "\5B8B\4F53", sans-serif;
    color: #666
}

.hide,
.none {
    display: none
}
/* 清除浮动 */
.clearfix:after {
    visibility: hidden;
    clear: both;
    display: block;
    content: ".";
    height: 0
}

.clearfix {
    *zoom: 1
}
```

**Unicode编码字体: **

把中文字体的名称用相应的Unicode编码来代替，这样就可以有效的避免浏览器解释CSS代码时候出现乱码的问题。

**比如:**
黑体\9ED1\4F53
宋体\5B8B\4F53
微软雅黑\5FAE\8F6F\96C5\9ED1



## HTML5和CSS3提高

HTML5的新增特性主要是针对于以前的不足,增加了-些新的标签、新的表单和新的表单属性等。

这些新特性都有兼容性问题,基本是IE9+以上版本的浏览器才支持,如果不考虑兼容性问题,可以大量使用这些新特性。



### HTML5的新特性

#### HTML5新增的语义化标签

![image-20200820095238212](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820095238212.png)

新增：

```html
<header> :头部标签
<nav> : 导航标签
<article> :内容标签
<section> :定义文档某个区域
<aside> :侧边栏标签
<footer> :尾部标签
```

![image-20200820095554087](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820095554087.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HTML5新增语义化标签</title>
    <style>
        header, nav {
            height: 120px;
            background-color: pink;
            border-radius: 15px;
            width: 800px;
            margin: 15px auto;
        }
        section {
            width: 500px;
            height: 300px;
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <header>头部标签</header>
    <nav>导航栏标签</nav>
    <section>某个区域</section>
</body>
</html>
```

**注意:**

* 这种语义化标准主要 是**针对搜索引擎**的
* 这些新标签页面中可以使用多次
* 在IE9中 ,需要把这些元素转换为**块级元素**
* 其实， 我们移动端更喜欢使用这些标签



####HTML5新增的多媒体标签

新增的多媒体标签主要包含两个:
1. 音频:`<audio>`
2. 视频: `<video>`

使用它们可以很方便的在页面中嵌入音频和视频,而不再去使用flash和其他浏览器插件。



HTML5在不使用插件的情况下,也可以原生的支持视频格式文件的播放,当然,支持的格式是有限的。

#####视频`<video>`
当前`<video>`元素支持三种视频格式：尽量使用mp4格式。

![image-20200820100403475](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820100403475.png)

**语法：**

```html
<video src="文件地址" controls="controls"></video>
```

兼容性写法：

![image-20200820100730742](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820100730742.png)

| 属性     | 值                                       | 描述                                                         |
| -------- | ---------------------------------------- | ------------------------------------------------------------ |
| autoplay | autoplay                                 | 视频就绪自动播放(谷歌浏览器需要添加muted来解决自动播放问题） |
| controls | controls                                 | 向用户显示播放控件                                           |
| width    | pixels（像素）                           | 设置播放器宽度                                               |
| height   | pixels（像素）                           | 设置播放器高度                                               |
| loop     | loop                                     | 播放完是否继续播放该视频，循环播放                           |
| preload  | auto（预先加载视频）none（不应加载视频） | 规定是否预加载视频(如果有了autoplay就忽略该属性)             |
| src      | url                                      | 视频url地址                                                  |
| poster   | imgurl                                   | 加载等待的画面图片                                           |
| muted    | muted                                    | 静音播放                                                     |



#####音频`<audio>`

当前`<audio>`元素支持三种音频格式：

![image-20200820102035174](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820102035174.png)

**语法：**

```html
<audio src="文件地址" controls=" controls"></audio>
```

兼容性：

```html
< audio controls=" controls">
<source src= "happy.mp3" type=" audio/ mpeg" >
<source src= "happy.ogg" type=" audio/ ogg" >
您的浏览器暂不支持<audio> 标签。
</ audio>
```

**常见属性：**

| 属性     | 值       | 描述                                             |
| -------- | -------- | ------------------------------------------------ |
| autoplay | autoplay | 如果出现该属性，则音频在就绪后马上播放。         |
| controls | controls | 如果出现该属性，则向用户显示控件，比如播放按钮。 |
| loop     | loop     | 如果出现该属性，则每当音频结束时重新开始播放。   |
| src      | url      | 要播放的音频的URL。                              |

* 谷歌浏览器把音频和视频自动播放禁止了



##### 多媒体标签总结

* 音频标签和视频标签使用方式基本一致
* 浏览器支持情况不同
* 谷歌浏览器把音频和视频自动播放禁止了
* 我们可以给视频标签添加muted属性来静音播放视频,音频不可以(可以通过JavaScript解决)
* 视频标签是重点,我们经常设置自动播放,不使用controls控件,循环和设置大小属性



#### HTML5新增的input类型

| 属性值        | 说明                        |
| ------------- | --------------------------- |
| type="email"  | 限制用户输入必须为Email类型 |
| type="url"    | 限制用户输入必须URL类型     |
| type="date"   | 限制用户输入必须为日期类型  |
| type="time"   | 限制用户输入必须为时间类型  |
| type="month"  | 限制用户输入必须为月类型    |
| type="week"   | 限制用户输入必须为周类型    |
| type="number" | 限制用户输入必须为数字类型  |
| type="tel"    | 手机号码                    |
| type="search" | 搜索框                      |
| type="color"  | 生成个颜色选择表单          |

```html
<u1>
<li>邮箱: <input[ type="email" /></1i>
<li>网址: <input type="url" /></li>
<li>日期: <input type="date" /></1i> 
<li>日期: <input type="time" /></li>
<li>数量: <input type=" number" /></1i>
<li>手机号码: <input type="tel" /></1i>
<li>搜索: <input type="search" /></li>
<li>颜色: <input type="color" /></1i>
<li> <input type=" submit" value="提交"></1i>
</ul>
```

![image-20200820103654517](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820103654517.png)



#### HTML5新增的表单属性

| 属性            | 值        | 说明                                                         |
| --------------- | --------- | ------------------------------------------------------------ |
| required        | required  | 表单拥有该属性表示其内容不能为空，必填                       |
| **placeholder** | 提示文本  | 表单的提示信息，存在默认值将不显示                           |
| autofocus       | autofocus | 自动聚焦属性，页面加载完成自动聚焦到指定表单                 |
| autocomplete    | off/on    | 当用户在字段开始键入时，浏览器基于之前键入过的值，应该显示出在字段中填写的选项。默认已经打开，如autocomplete="on"，关闭autocomplete ="off"需要放在表单内，同时加上name属性，同时成功提交 |
| **multiple**    | multiple  | 可以多选文件提交                                             |

![image-20200820104814648](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820104814648.png)



### CSS3新特性

* 新增的CSS3特性有兼容性问题, ie9+才支持
* 移动端支持优于PC端
* 不断改进中
* 应用相对广泛
* 现阶段主要学习:新增选择器和盒子模型以及其他特性



#### CSS3新增选择器

CSS3给我们新增了选择器,可以更加便捷,更加自由的选择目标元素。

* 属性选择器
* 结构伪类选择器
* 伪元素选择器



##### 属性选择器

属性选择器可以根据元素特定属性的来选择元素。这样就可以不用借助于类或者id选择器。

| 选择符        | 简介                                  |
| ------------- | ------------------------------------- |
| E[att]        | 选择具有att属性的E元素                |
| E[att="val"]  | 选择具有att属性且属性值等于val的E元素 |
| E[att^="val"] | 匹配具有att 属性且值以val开头的E元素  |
| E[att$="val"] | 匹配具有att 属性且值以val结尾的E元素  |
| E[att*="val"] | 匹配具有att 属性且值以val结尾的E元素  |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3新增属性选择器</title>
    <style>
        /* 必须是input 但是同时具有 value这个属性 选择这个元素  [] */
        /* input[value] {
            color:pink;
        } */
        /* 只选择 type =text 文本框的input 选取出来 */
        input[type=text] {
            color: pink;
        }
        /* 选择首先是div 然后 具有class属性 并且属性值 必须是 icon开头的这些元素 */
        div[class^=icon] {
            color: red;
        }
        section[class$=data] {
            color: blue;
        }
        div.icon1 {
            color: skyblue;
        }
        /* 类选择器和属性选择器 伪类选择器 权重都是 10 */
    </style>
</head>
<body>
    <!-- 1. 利用属性选择器就可以不用借助于类或者id选择器 -->
    <!-- <input type="text" value="请输入用户名">
    <input type="text"> -->
    <!-- 2. 属性选择器还可以选择属性=值的某些元素 重点务必掌握的 -->
    <input type="text" name="" id="">
    <input type="password" name="" id="">
    <!-- 3. 属性选择器可以选择属性值开头的某些元素 -->
    <div class="icon1">小图标1</div>
    <div class="icon2">小图标2</div>
    <div class="icon3">小图标3</div>
    <div class="icon4">小图标4</div>
    <div>我是打酱油的</div>
    <!-- 4. 属性选择器可以选择属性值结尾的某些元素 -->
    <section class="icon1-data">我是安其拉</section>
    <section class="icon2-data">我是哥斯拉</section>
    <section class="icon3-ico">哪我是谁</section>

</body>
</html>
```

**注意:类选择器、属性选择器、伪类选择器,权重为10。**



#####结构伪类选择器

结构伪类选择器主要根据**文档结构**来选择器元素，常用于根据父级选择器里面的子元素。

| 选择符           | 简介                         |
| ---------------- | ---------------------------- |
| E:first-child    | 匹配父元素中的第一个子元素 E |
| E:last-child     | 匹配父元素中最后一个E元素    |
| E:nth-child(n)   | 匹配父元素中的第n个子元素E   |
| E:first-of-type  | 指定类型E的第一个            |
| E:last-of-type   | 指定类型E的最后一个          |
| E:nth-of-type(n) | 指定类型E的第n个             |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3新增结构伪类选择器</title>
    <style>
        /* 1. 选择ul里面的第一个孩子 小li */
        ul li:first-child {
            background-color: pink;
        }
        /* 2. 选择ul里面的最后一个孩子 小li */
        ul li:last-child {
            background-color: pink;
        }
         /* 3. 选择ul里面的第2个孩子 小li */
         ul li:nth-child(2) {
            background-color: skyblue;
        }
        ul li:nth-child(6) {
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <ul>
        <li>我是第1个孩子</li>
        <li>我是第2个孩子</li>
        <li>我是第3个孩子</li>
        <li>我是第4个孩子</li>
        <li>我是第5个孩子</li>
        <li>我是第6个孩子</li>
        <li>我是第7个孩子</li>
        <li>我是第8个孩子</li>
    </ul>
</body>
</html>
```



**nth-child(n)选择某个父元素的一个或多个特定的子元素**

* n可以是数字,关键字和公式
* n如果是数字,就是选择第n个子元素，里面数字从1开始...
* n可以是关键字:even偶数,odd奇数
* n可以是公式:常见的公式如下(如果n是公式,则从0开始计算,但是第0个元素或者超出了元素的个数会被忽略)

| 公式 | 取值                             |
| ---- | -------------------------------- |
| 2n   | 偶数                             |
| 2n+1 | 奇数                             |
| 5n   | 5 10 15 ...                      |
| n+5  | 从第五个开始（包含第五个）到最后 |
| -n+5 | 前5个（包含第五个）...           |

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3新增结构伪类选择器-nth-child</title>
    <style>
        /* 1.把所有的偶数 even的孩子选出来 */
        ul li:nth-child(even) {
            background-color: #ccc;
        }

        /* 2.把所有的奇数 odd的孩子选出来 */
        ul li:nth-child(odd) {
            background-color: gray;
        }
        /* 3.nth-child(n) 从0开始 每次加1 往后面计算  这里面必须是n 不能是其他的字母 选择了所有的孩子*/
        /* ol li:nth-child(n) {
            background-color: pink;
        } */
        /* 4.nth-child(2n)母选择了所有的偶数孩子 等价于 even*/
        /* ol li:nth-child(2n) {
            background-color: pink;
        }
        ol li:nth-child(2n+1) {
            background-color: skyblue;
        } */
        /* ol li:nth-child(n+3) {
            background-color: pink;
        } */
        ol li:nth-child(-n+3) {
            background-color: pink;
        }
    </style>
</head>

<body>
    <ul>
        <li>我是第1个孩子</li>
        <li>我是第2个孩子</li>
        <li>我是第3个孩子</li>
        <li>我是第4个孩子</li>
        <li>我是第5个孩子</li>
        <li>我是第6个孩子</li>
        <li>我是第7个孩子</li>
        <li>我是第8个孩子</li>
    </ul>
    <ol>
        <li>我是第1个孩子</li>
        <li>我是第2个孩子</li>
        <li>我是第3个孩子</li>
        <li>我是第4个孩子</li>
        <li>我是第5个孩子</li>
        <li>我是第6个孩子</li>
        <li>我是第7个孩子</li>
        <li>我是第8个孩子</li>
    </ol>
</body>

</html>
```



**区别:**

1. nth-child 对父元素里面所有孩子排序选择(序号是固定的)先找到第n个孩子,然后看看是否和E匹配
2. nth-of-type 对父元素里面指定子元素进行排序选择。先去匹配E , 然后再根据E找第n个孩子



#####小结

* 结构伪类选择器一 般用于选择父级里面的第几个孩子
* nth-child对父元素里面所有孩子排序选择(号是固定的)先找到第n个孩子,然后看看是否和E匹配
* nth-of-type对父元素里面指定子元素进行排序选择。先去匹配E , 然后再根据E找第n个孩子
* 关于nth-child (n)我们要知道n是从0开始计算的,要记住常用的公式
* 如果是无序列表,我们肯定用nth-child更多
* 类选择器、属性选择器、伪类选择器,权重为10。



#### 伪元素选择器（重点）

伪元素选择器可以帮助我们利用C SS创建新标签元素,而不需要HTML标签,从而简化HTML结构。

| 选择符   | 简介                     |
| -------- | ------------------------ |
| ::before | 在元素内部的前面插入内容 |
| ::after  | 在元素内部的后面插入内容 |

**注意:**

* **before** 和**after**创建一个元素 ,但是属于行内元素
* 新创建的这个元素在 文档树中是找不到的,所以我们称为伪元素语法:` element::before{ }`
* before 和after必须有**content属性**
* before 在父元素内容的前面创建元索, after 在父元索内容的后面插入元素
* **伪元素选择器**和**标签选择器**一样,权重为1



运用1：

![image-20200820155800357](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820155800357.png)

```css
div {
            position: relative;
            width: 200px;
            height: 35px;
            border: 1px solid red;
        }

        div::after {
            position: absolute;
            top: 10px;
            right: 10px;
            font-family: 'icomoon';
            /* content: ''; */
            content: '\e91e';
            color: red;
            font-size: 18px;
        }
```



运用2（土豆遮罩层）：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>伪元素选择器使用场景2-仿土豆网显示隐藏遮罩案例</title>
    <style>
        .tudou {
            position: relative;
            width: 444px;
            height: 320px;
            background-color: pink;
            margin: 30px auto;
        }

        .tudou img {
            width: 100%;
            height: 100%;
        }

        .tudou::before {
            content: '';
            /* 隐藏遮罩层 */
            display: none;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, .4) url(images/arr.png) no-repeat center;
        }

        /* 当我们鼠标经过了 土豆这个盒子，就让里面before遮罩层显示出来 */
        .tudou:hover::before {
            /* 而是显示元素 */
            display: block;
        }
    </style>
</head>

<body>
    <div class="tudou">
        <img src="images/tudou.jpg" alt="">
    </div>
    <div class="tudou">
        <img src="images/tudou.jpg" alt="">
    </div>
    <div class="tudou">
        <img src="images/tudou.jpg" alt="">
    </div>
    <div class="tudou">
        <img src="images/tudou.jpg" alt="">
    </div>
</body>
</html>
```



运用3（伪元素清除浮动）：

* 额外标签法也称为隔墙法,是W3C推荐的做法
* 父级添加overflow属性
* 父级添加after伪元素
* 父级添加双伪元素

![image-20200820161159680](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820161159680.png)

![image-20200820161432625](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820161432625.png)



#### CSS3 2D转换

转换( transform )是CSS3中具有颠覆性的特征之一, 可以实现元素的位移、旋转、缩放等效果
转换( transform )你可以简单理解为变形

* 移动: translate
* 旋转: rotate
* 缩放: scale

![image-20200820202405730](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820202405730.png)

#####2D 转换之移动translate

2D移动是2D转换里面的一种功能,可以改变元素在页面中的位置,类似定位。

![image-20200820220828133](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820220828133.png)

语法：

```html
transform: translate(x,y); 或者分开写;
transform: translatex(n) ;
transform: translateY(n) ;
```

重点：

* 定义2D转换中的移动,沿着X和Y轴移动元素
* translate最大的优点:不会影响到其他元素的位置
* translate中的百分比单位是相对于自身元素的translate(50%,50%);
* 对行内标签没有效果



#####2D 转换之旋转rotate

2D旋转指的是让元素在2维平面内顺时针旋转或者逆时针旋转。

![image-20200820231925093](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820231925093.png)

语法：

```html
transform: rotate (度数)
```

重点：

* rotate里面跟度数，单位是deg比如rotate(45deg)
* 角度为正时,顺时针,负时,为逆时针
* 默认旋转的中心点是元素的中心点



##### 2D转换中心点transform-origin

我们可以设置元素转换的中心点

语法：

```html
transform-origin: x y;
```

重点：

* 注意后面的参数x和y用空格隔开
* x y默认转换的中心点是元素的中心点(50% 50%)
* 还可以给xy设置像素或者方位名词( top bottom left right center )

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820235829860.png" alt="image-20200820235829860" style="zoom:67%;" />

```css
div {
    overflow: hidden;
    width: 200px ;
    height: 200px;
    border: 1px solid pink;
    margin: 100px auto ;
}
div::before {
    content :"黑马";
    display: block;
    width: 100%;
    height: 100%;
    background-color: hotpink;
    transform: rotate(180deg);
    transform-origin: left bottom;
    transition: all 0.4s;
}
/*鼠标经过div里面的before复原*/
div:hover: :before {
transform: rotate(0deg);
}
```



##### 2D转化之缩放scale

缩放,顾名思义,可以放大和缩小。只要给元素添加 上了这个属性就能控制它放大还是缩小。

![image-20200821000344278](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200821000344278.png)

语法：

```html
transform: scale(x,y);
```

注意：

* 注意其中的x和y用逗号分隔
* transform:scale(1,1) : 宽和高都放大-倍,相对于没有放大
* transform:scale(2,2) : 宽和高都放大了2倍
* transform:scale(2) : 只写一个参数,第二个参数则和第一个参数-样,相当于scale(2,2)
* transform:scale(0.5,0.5) :缩小
* sacle缩放最大的优势:可以设置转换中心点缩放,默认以中心点缩放的，而且不影响其他盒子

```html
div {
width: 200px;
height: 200px;
background-color: pink;
margin: 100px auto ;
}
div:hover {
/* 1.里面写的数字不跟单位就是倍数的意思1就是1倍 2就是2倍*/
/* transform: scale(x, y); */
/* transform: scale(2, 2); */
/*2.修改了宽度为原来的2倍高度不变*/
/* transform: scale(2, 19; */
/* 3.等比例缩放同时修改宽度和高度，我们有简单的写法 以下是宽度修改了2倍，高度默认和第一个参数一 样*/
/* transform: scale(2); */
/* 4.我们可以进行缩小 小于1就是缩放*/ 
/* transform: scale(0.5, 0.5); */
transform: scale(0.5);
}
```





#### CSS3盒子模型

CSS3中可以通过box- sizing来指定盒模型,有2个值:即可指定为content- box、border-box ,这样我们
计算盒子大小的方式就发生了改变。
可以分成两种情况:
1. box-sizing: content-box盒子大小为width + padding + border ( 以前默认的)
2. box-sizing: border-box盒子大小为width

如果盒子模型我们改为了box-sizing: border-box， 那padding和border就不会撑大盒子了 (前提padding和border不会超过width宽度)

```css
* {
   margin: 0;
   padding: 0;
   box-sizing:
   border - box;
}
```



####CSS3其他特性

#####CSS3滤镜filter:
filter CSS属性将模糊或颜色偏移等图形效果应用于元素。

```css
filter:函数(); 例如 : filter: blur(5px); blur模糊处理 数值越大越模糊
```

#####CSS3 calc函数:
calc()此CSS函数让你在声明CSS属性值时执行一些计算。

```css
width: calc(100% - 80px);
```

括号里面可以使用+ - * /来进行计算。



####CSS3过渡（重点）

过渡( transition)是CSS3中具有颠覆性的特征之一 , 我们可以在不使用Flash 动画或JavaScript的情况下，当元素从-种样式变换为另一种样式时为元素添加效果。

过渡动画:是从一个状态渐渐的过渡到另外一个状态

可以让我们页面更好看,更动感十足,虽然低版本浏览器不支持( ie9以下版本)但是不会影响页面布局。

我们现在经常和:hover一起搭配使用。

```css
transition:要过渡的属性花费时间运动曲线何时开始;
```

**属性:**想要变化的CSS属性，宽度高度背景颜色内外边距都可以。如果想要所有的属性都变化过渡，写-个all就可以。
**花费时间:**单位是秒(必须写单位)比如0.5s
**运动曲线:**默认是ease ( 可以省略)
**何时开始:**单位是秒(必须写单位)可以设置延迟触发时间默认是0s ( 可以省略)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3 过渡效果</title>
    <style>
        div {
            width: 200px;
            height: 100px;
            background-color: pink;
            /* transition: 变化的属性 花费时间 运动曲线 何时开始; */
            /* transition: width .5s ease 0s, height .5s ease 1s; */
            /* 如果想要写多个属性，利用逗号进行分割 */
            /* transition: width .5s, height .5s; */
            /* 如果想要多个属性都变化，属性写all就可以了 */
            /* transition: height .5s ease 1s; */
            /* 谁做过渡，给谁加 */
            transition: all 0.5s;
        }
        div:hover {
            width: 400px;
            height: 200px;
            background-color: skyblue;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

**记住过渡的使用口诀:谁做过渡给谁加。**




###项目：品优购

#### 项目搭建工作

![image-20200820171013243](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820171013243.png)

![image-20200820171842906](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820171842906.png)

![image-20200820172812688](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200820172812688.png)



p302






