## Html学习笔记

[TOC]



#### 1.HTML总体格式

1. 结构写到HTML文件中表现写道CSS文件中行为写道Javascript文件中

2. 语法规范1.标签要在<>之间一般有两个标签一个开始一个结束如<html>  </html>,这是双标签。有些是单标签如<br />

3. 标签关系分为两类包含关系和并列关系 如

<html>

<head>

</html>

4. 基本结构标签<html>是最大的标签，页面中最大的标签是根标签，<head>是文档的头部，必须head标签中必须要设置的标签是title，<title>是文档的标题，让页面拥有一个属于自己的网页标题，<body>是文档的主题页面内容基本都是放在body里面的，这些都是双标签

5. 关系为如下

<html>

 <head>

   <title>第一个页面</title>

 </head>

 <body>

 键盘敲烂，工资过万

 </body>

</html>

6. HTML文档的后缀名一定是.html

7. <!DOCTYPE html>作用是告诉浏览器使用哪种HTML版本来显示网页，必须写在<html>标签的前面

8. lang语言<html lang="en">用来定义当前文档显示的语言en为英语zh-CN为中文，但对于文档显示来说，定义成en的文档也可以显示中文，定义成zh-CN的文档也可以显示英文，fr是法文，如果是法文时网页中的中文可能会出错

9. <meta charset="UTF-8">用来规定HTML文档应该使用那种字符编码。charset常用的值有GB2312、BIG5、GBK和UTF-8，其中UTF-8被称为万国码，基本包含了所有需要用的字符，UTF-8用的最多，这句代码时必须的

#### 2. HTML的标题，文字，换行

1. HTML有6个等级的网页标题即<h1>-<h6>用法为<h1>  </h1>在这之间加标题，都是独占一行，会由大到小变小，重要性也会逐渐变化

2. 段落和换行标签<p>  </p>段落标签可以分段落，空白中间是一个段落，段落会随着浏览器的变化自动换行，有几个段落写几个p

3. 强制换行用单标签<br />可以添在<p>   </p>之间

4. 加粗标签<strong>  </strong>,之间的文字变粗，<b>  </b>也能加粗，更推荐使用<strong>

5. 倾斜标签<em>  </em>，之间的文字倾斜

6. 删除键<del>  </del>,之间的文字有删除线

7. 下划线<ins>  </ins>，之间的文字有下划线

#### 3. HTML的div,图像链接，图像属性

1. <div>和<span>没有语义，它是一个盒子，可以放文字和图片等内容，都是双标签，div是分割分区，独占一行的盒子，一行只有一个div。span是跨度和跨距，一行可以有多个span。

2. <img src="图像URL" />是图像标签，src是图像的必须属性，用于指定图像文件的路径和文件名，图像URL是图像的地址，名称，如img.jpg

3. alt替换文本，图像显示不出来时用文字替换，<img src="img.jpg" alt="我是" />，如果图片显示不出来时会显示“我是”

4. title是提示文本，鼠标放在图像上，提示的文字<img src="img.jpg" alt="我是" title="我是" />当鼠标放在图片上会显示“我是”

5. width设置图像的宽度，如<img src="img.jpg" alt="我是" title="我是" width="500" />  height用于设置高度 如<img src="img.jpg" alt="我是" title="我是" width="500" height="200" /> 宽度和高度一般改一个就可以了，因为会自动等比例变换

6. border用于添加边框如<img src="img.jpg" alt="我是" title="我是" width="500" height="200" border="15" />，图片的边框会出现15粗细的边框

7. 图像标签的多种属性，一定要写在img后面，属性和属性之间一定要有一个空格，格式为属性=”属性值“

8. /是下一级意思，如果一个图片在一个文件夹里就用<img src="images/img.jpg>

Images是文件夹的名字，img.jpg是图像的地址，名称

9. ../是上一级意思路径

#### 4.HTML的超链接，锚点链接，特殊字符，注释格式

1. 绝对路径是指文件或图片的绝对地址

2. <a>标签用于定义超链接，作用是一个页面链接到另一个页面

3. 格式为<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>,外部链接，外部链接必须以http://开头，target=”_self”,表示用当前窗口打开，target=”_blank”，表示用新窗口打开

4. 内部链接<a href=” .html”>内部链接不用http://，只要是同一个文件夹内就是内部链接。

5. 空链接<a href="#">,这代表是一个空链接

6. 下载链接,地址链接的是文件.exe或者是.zip等压缩包形式，与上面方式相同

7. 如果是<a href="img.zip">下载文件</a>，这样‘下载文件’加了超链接，如果是<a href="img.zip"><img src="img.jpg"></a>这样就给图片加了超链接

8. 锚点链接，点击链接可以快速定位到页面中的某个位置<a href="#two">第二集</a>,链接的名字是two，#是必须的，然后对‘第二集’<id=”two”>第二集，这样就可以了

9. 注释标签<!--  -->可以在空白处添加注释，不会执行也不会显示

10. 特殊字符 &nbsp 代表一个空格，&lt代表一个小于号，&gt代表一个大于号，要有分号！，空格，大于号，小于号三个常用

#### 5.表格，列表格式

1. 表格的基本语法

<table>

​     <tr>

​     <td>单元格内的文字</td>

   ...

   </tr>

  ...

 </table>

table用于定义表格的标签，tr是定义表格中的行，td是定义行内的单元格

2. <th>表示表格的表头部分，会加粗、居中显示，用th就可以不用td

3. align规定表格相对周围元素的对齐方式，比如<table align="center">,cellpadding单元格内部文字与单元格边框之间的距离cellspacing是单元格和单元格之间的距离,这些都要放在<table   >的空白处。这些内容可以用CSS来使用，可以不写。

4. <thead>标签表头的区域<tbody>是除了表头之外的主体区域，thead里面必须有tr。

5. rowspan是跨行合并colspan是跨列合并,跨行的目标单元格是目标合并的最左端的单元格，如<td colspan="2"></td>然后删除多余的单元格

6. <ul>   </ul>是无序列表，空白处写li,<li>  </li>是无序列表中的行，空白处写列表项，ul中只能加li标签，也不能直接书写文字，p可以放在li里，实际使用时可以用CSS来变化列表属性，前面的小圆点可以在CSS中去掉。

7. <ol>用来定义有序列表，使用<li>来定义列表项

如<ol>

<li>   </li>在li之中写列表的文本，且在文本前面会有数字进行排序

</ol>这是格式

8. <dl>用来定义自定义列表,<dt>是定义列表项，格式同上且dt是一个较小的类标题，也就是一个小分类的总标题，<dd>是对该这个小标题的具体内容的说明，dl里只能放dt与dd，dd和dt里面可以放任何标签

#### 6.各种元素建立如form input button ，以及各种属性如value等

1. <form>会把它范围内的表单信息提供给服务器，格式为

<form action=”url地址” method=”提交方式” name=”表单域名称”>



</form>

2. input输入表单元素，用来收集用户信息input里面必须要有type属性，格式

<form>
<!--text 用户可以在里面输入任何文字-->(注释)

用户名：<input type="text" name="username">

密码：<input type=”password”>(里面输入的密码会变成**)

性别：男 <input type=”radio” name=”sex” value=”男” checked=”checked”> 女 <input type=”radio” name=”sex” value=”女”>(radio可以实现多选一)

爱好：吃饭<input type=”checkbox”>睡觉<input type=”checkbox”>(可以多选多)

(多选一和多选多的name必须相同，且必须使用，也就必须要有)

</form>

button定义可点击按钮通过Java启动脚本，checkbox定义复选框，file定义输入字段和“浏览”按钮，供文件上传，hidden定义隐藏的输入字段，image定义图像形式的提交按钮，radio定义单选按钮，reset定义重置按钮，重置按钮会清除表单中的所有数据，submit定义提交按钮，该按钮会把表单数据发送给服务器

3. name定义input元素的名称，value只能在文本框和某些点击框中显示，是给用后台人员使用，后台人员就可以知道用户选了什么

4. checked规定input首次加载就会被选中，单选按钮和复选框可以设置checked属性，当页面打开时就可以默认选中这个按钮,格式 checked=”checked”，这样就默认选中了

5. maxlength表示输入的最大字符比如maxlength=6输入最多6个字符

6. submit格式为<input type="submit" value="免费注册">提交按钮里的文字就变为了免费注册，当点了submit的提交框时，会转到后台页面，其中表单域form中的表单内容提交给后台服务器

7. reset<input type="reset" value="重新填写">可以把表单元素的内容还原初始状态

8. <input type="button" value="获取短信验证码">后期搭配JS使用

9. <input type="file" value="上传图片">文件域，可以上传文件

10. <label>标签可以绑定一个表单元素，当点击label标签内的文本时，浏览器会自动将光标转到或者选择对应的表单元素上，用来增加用户体验，格式为

<label for=”sex”>男</label>

<input type=”radio” name=”sex” id=”sex” />核心：label标签的for属性应当与相关元素的id属性相同

11. select用于列表选择，格式为

<select>

 <option>  </option>(选项内容放在空白处)

 <option>  </option>在<option>中定义selected=”selected”

</select>

12. textarea文本域元素，当用户输入内容较多时，就不能用文本框，可以用textarea，相当于一个特大文本框，格式为<textarea>  </textarea>，空白处的文本格式可调，要用CSS进行调试

http://www.w3school.com.cn/查找标签网站

#### 7.div综合 mime target=_blank属性

1. 当class用在div上时，在css里不需要用div如

.riluobingchuan{

  position:relative;

  left:1000px;

  color: rgb(0, 0, 0);

  font: normal 700 40px '宋体';

  text-align: left;

  position:relative;

  left:600px;

}.class名称后不用加div

2. 浏览器通常使用 MIME 类型（而不是文件扩展名）来确定如何处理URL，添加正确的 MIME 类型非常重要

<link rel="stylesheet" type="text/css" href="style.css">这个放在head前面而type="text/css"就是确定MIME类型如text/plain, text/html, text/css, text/javascript等type="text/css"就说明该文件是css 类型。

3. target=_blank这个属性就是表示，在新的窗口打开超链接

如<a href="01.jpg" target="_blank">