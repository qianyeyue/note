# JS笔记

[TOC]

function addEvent() 定义addEvent()的作用

var li = document.createElement("div")也就是定义li是一个新的创建的div元素

Var Document.createElement() 方法用于创建一个由标签名称 tagName 指定的 HTML 元素

window.alart() 可以弹出警告框。括号中填入要输出的变量/常量。

console.log() 可以将内容写到控制台。在浏览器中使用F12启动调试模式。 

关键字 var 来定义变量，使用等号来赋值，变量的值为下述量类型

数字字面量  整数/小数/科学计数

字符串字面量  可以使用单引号或双引号

表达式字面量   

数组字面量   如 [40, 100, 5]

对象字面量   如 { name:"xyx", age:19 }

函数字面量   如 function F(a,b) { return a + b; }

可以使用 typeof 操作符来检测变量的数据类型如typeof "John"         // 返回 string 

JavaScript里单引号和双引号没啥区别

HTML事件

onchange ，表单等HTML元素改变，如填写表单。在改变完成后。

onclick ，用户点击HTML元素。

onmouseover ，用户的在HTML元素上移动鼠标。

onmouseout ，用户的鼠标自HTML元素上移开。

onkeydown ，用户按下键盘按键。

onload ，浏览器已经完成页面加载

使用document.getElementById()可以取到页面上一个有id的元素然后访问这个元素的属性，比如value形式是document.getElementById().value

innerHTML在JS是双向功能：获取对象的内容 或 向对象插入内容；

使用document.getElementById("lb1").innerHTML可以取到<label>与</label>之间的内容（也就是显示的内容）

className可以用来改变标签元素的css类[选择器](https://so.csdn.net/so/search?q=选择器&spm=1001.2101.3001.7020)，从而改变元素的样式

使用方法选择子节点。如：var text = document.getElementById("ipt").value;

使用 该属性可访问父元素。如：parentElement btn.onclick = function (event)  {

​    event.target.parentElement.remove() } 

在父级上调用该方法，如event.target.parentElement.remove()就可以移除id=ipt的text的value

innerText 属性设置或返回指定节点及其所有子节点的文本内容。

innerText 属性只返回文本，没有间距和内部元素标记。

innerHTML 属性返回文本，包括所有间距和内部元素标记。

textContent 属性返回带间距但不带内部元素标记的文本。

appendChild() 方法可向节点的子节点列表的末尾添加新的子节点。

可以使用 appendChild() 方法移除元素到另外一个元素。

document.write这个命令简单地打印指定的文本内容到页面上

如果变量名称加上引号，将会打印出变量名称（不会打印变量值）。你可以使用“+”符号来连接变量值和文本字符串

var colour1 = "purple";   var colour2 = "pink"; document.write('<p>colour1: ' + colour1 + '<br>colour2: ' + colour2 + '</p>');  

 打印结果如下

colour1: purple 

colour2: pink

### document.createElement的用法

var node=document.createElement("LI");首先创建 LI 节点，

var textnode=document.createTextNode("Water");然后创建文本节点，

node.appendChild(textnode);然后把这个文本节点追加到 LI 节点（或者说node上）。

document.getElementById("myList").appendChild(node);最后把 LI 节点添加到列表中。

document.createElement()是在对象中创建一个对象，要与appendChild() 或 insertBefore()方法联合使用。其中，appendChild() 方法在节点的子节点列表末添加新的子节点。insertBefore() 方法在节点的子节点列表任意位置插入新的节点。

var k = document.createElement("input");

k.type = "button";

k.value = "这是测试加载的小例子";

board.appendChild(k);

也就是创建了一个类型为button的k并且将k放在id为board的子元素下面

board.appendChild(k);表示k要放在id为board的子元素下面

### alert用法

用于网页上的提醒，比如说弹出一个弹窗提醒用户，如

alert(x.innerHTML)//就是表示弹出弹窗，弹窗的内容是x的value或者说x的显示内容

### getElementByld("")用法

var x = document.getElementByld("x1")表示x获取了id为x1的标签的所有属性

### innerHTML用法

表示使一个元素获取另一个元素的内容，或者使一个元素显示/设置另一个元素的内容

### 清空一个元素内容

 function deleteEvent(event) {

  var parent = document.getElementById("my list2");

  parent.innerHTML = ""

  //让parent的内容清空  

}

### event.target.

event.target.指向引发一个事件的元素



