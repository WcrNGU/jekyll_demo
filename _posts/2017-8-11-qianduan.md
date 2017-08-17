---
layout: defualt
title: 前端开发知识梳理
---

# {{page.title}}

## 快捷键
在编辑器中输入elementname即相当于<elementname></elementname>
在编辑器中输入.classname按回车即相当于<div class="classname"></div>
选中一部分，按下Ctrl+d，就会选中接下来跟选中部分相同的部分。多光标。  

## HTML部分
传统HTML的各种标签，做到标签语义化，以及HTML5的新特性   
h5新加入的表单(form)元素：<datalist>、<keygen>、<output>。  
h5新加入的输入<input>类型(type):color、date、datetime、datetime-local、email、month、number、range、search、tel、time、url、week，不支持时被视为text。 
h5标准允许4中不同的属性语法，分别为：Empty、Unquoted、Double-quoted、Single-quoted。quoted意为引号。  
h5的canvas使用javascript在网页上画图，
<!DOCTYPE html> 不是 HTML 标签。它为浏览器提供一项信息（声明），即 HTML 是用什么版本（html5）编写的。  
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">表示网站用html 4.01编写。  
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">表示网站用html 1.0编写。  
<pre>标签为预格式文本，它保留了空格和换行，适用于代码的显示。  
<frameset cols="" rows="" > <frame scr=""></frame> </frameset>用于在一个浏览器显示多个页面，但不能与<body>同时使用。iframe用于显示内联框架。   
target属性用于指明链接的打开位置，head部分的base元素可以为页面上的所有链接指明打开位置。  
meta标签可以用于标注姓名、作者、编辑器、描述、关键字，也可以用于确定页面显示方法及重定向（对于域名不确定的某些网站来说）。  
cookies只有4kb，用于在客户端存储少量信息，有时间限制。LocalStorage有8mb，用于在客户端存储数据，无时间限制。Session Storage用于在本地存储暂时性的数据，生命周期只有一个session的时间。  

## CSS部分
在css中，选择器用于选择需要添加样式的元素，同时jQuery也可以通过css选择器选取元素。  
盒模型，包括content内容、padding内距、border边框、margin外距四种属性。  
当你设置一个元素为 box-sizing: border-box; 时，此元素的内边距和边框不再会增加它的宽度，这种设置通常使用*选择器。  
css的position属性有四种：默认普通流式static（非positioned）、相对定位relative、绝对定位absolute、固定定位fixed   
css的display属性常用的有：不显示none、块级元素block、行内元素inline、行内块级元素inline-block，inline-block通常用来布局一堆小格子（例如淘宝商品）。   
absolute定位是相对于它的最近的positioned父元素的绝对定位，如果没有这样的父元素，则相对body进行绝对定位。  
float通常用于实现文字环绕和浮动布局,overflow通常用于设置内容溢出，vertical-align用于设置垂直对其方式，Z-index用于设置元素堆叠顺序。  
行元素和块元素  
flex布局  
使用新的CSS属性时，要用-moz-...以及-webkit-...以及...因为新属性可能对某些浏览器不兼容，需要从webkit和mozilla获取。  

## JS部分
js获取元素的方法：getElementById、getElementByClass、getElementByTagName，即通过ID、类名、标签名获取对应元素的对象  
js获取当前时间：用Date对象
JS文件位置有：head、body尾部、外部文件，&lt script scr="***.js" &gt &lt /script &gt  
JavaScript是脚本语言，与其它编程语言先编译全部代码再运行不同，脚本语言是逐行执行的。 
var x="123";当数字被双引号包括时，变量会被作为字符串；如果把数字和字符串相加，结果将成为字符串。   
js拥有动态数据类型，声明并未进行赋值的变量，类型为undefined，被赋值后类型自动转换为相应类型，再次以不同类型赋值后依然会进行自动转换。    
js数组声明有var x = new Array(); 和 var x =[]; 两种。  
js的变量均为对象，一旦声明了一个变量，就相当于创建了一个对象。  
可以通过将变量的值设置为null来清空变量。  
如果把值赋给一个未声明的变量，该变量将会自动成为全局变量，即使在函数中执行这个赋值操作。  
NULL与空字符串的区别：NULL未分配存储空间，空字符串是分配了空间但没有内容。  
当网页被加载时，浏览器会创建页面的文档对象模型，HTML DOM 模型被构造为对象的树。文档-根元素<html>-<head>/<body>-...  
HTML DOM 允许js改变HTML的输出流、改变元素内容innerHTML、改变元素属性、改变元素样式(CSS)以及添加或删除HTML元素。  
HTML 事件的例子：当用户点击鼠标时、当网页已加载时、当图像已加载时、当鼠标移动到元素上时、当输入字段被改变时、当提交 HTML 表单时、当用户触发按键时...  
onload 和 onunload 事件会在用户进入或离开页面时被触发，onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本，onload 和 onunload 事件可用于处理 cookie。  
onchange事件经常用于验证输入，onfocus事件经常用于输入时改变输入框样式。  
当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。  
如果需要向HTMLDOM添加新元素，需要使用document.createElement创建新元素，使用document.createTextNode创建一个文本节点，并用xxx.appendChild将文本节点追加到元素，然后用fatherElement.appendChild将子元素追加到父元素内。删除元素时，同时获取父子元素，使用fatherElement.removeChild(childElement);进行操作。  
ECMAScript内部类包括Object、Function、Array、String、Boolean、Number、Date、RegExp以及各种Error（EvalError、RangeError、ReferenceError、SyntaxError、TypeError、URIError）。  
目前js创建对象使用的最多的方法是：混合构造/原型方式 和 动态原型方法，1.成员变量使用构造方式，成员函数使用原型方式（prototype）；2.if (typeof Car._initialized == "undefined") { //原型方式添加成员函数  Car._initialized = true;}。  
对一个数组排序时，使用arr.sort(function)，函数中应返回a-b，因为sort排序会受到0的干扰。  
如果逻辑对象无初始值或者其值为 0、-0、null、""、false、undefined 或者 NaN，那么对象的值为 false。否则，其值为 true（即使当自变量为字符串 "false" 时）。  
浏览器对象模型BOM(Browser Object Model)包含window对象、screen对象、location对象、history对象、navigator对象、popupalter对象、timing对象、cookies对象。  	
Xmlhttp是一种浏览器对象，可用于模拟http的GET和POST请求。配合JavaScript可以实现页面数据在无刷新下的定时数据更新，如果应用在聊天室、文字直播上可以取得较好的视觉效果。  
所有浏览器都支持 window 对象，它表示浏览器窗口，所有 JavaScript 全局对象、函数以及变量均自动成为 window 对象的成员，甚至 HTML DOM 的 document 也是 window 对象的属性之一。  
window.location 对象用于获得当前页面的地址 (URL)，并把浏览器重定向到新的页面，重定向是浏览器重新发起一次http请求，与服务器端的转发不同，转发不经过浏览器。  
cookie 是存储于访问者的计算机中的变量。每当同一台计算机通过浏览器请求某个页面时，就会发送这个 cookie。你可以使用 JavaScript 来创建和取回 cookie 的值。  
js的解析器对函数声明与函数表达式的解析是不同的，对于函数声明，js解析器会优先读取，确保在所有代码执行之前声明已经被解析，而函数表达式，如同定义其它基本类型的变量一样，只在执行到某一句时才会对其进行解析  
console.log可以在控制台输出，通常用于调试。  
Server-Sent用于从服务器获得即时更新，而不需要刷新页面，类似facebook消息刷新。  
关于事件冒泡，一旦有事件发生，onMessage监听器就能捕获事件并且做出反应。WebWoker和ServerSent事件的数据都保存在event.data中。    
```  
document.write(""); //用于直接向HTML输出流写入内容，该语句如果放在函数中在文档加载完成后执行，则会覆盖原文档  
<button type="button" onclick="alter('')">  <!-- 弹出提示框，也可换为function执行函数 -->  
x=document.getElementById(""); x.innerHTML=""; //获取元素，并将内容写入该标签内嵌部分  
element.scr.match(""); //用以匹配元素的属性的内容  
var y=123e5; // 表示12300000  
var person={firstname:"Bill", lastname:"Gates", id:5566}; //js对象的初始化，调用为 object.property  
<h1 onclick="this.innerHTML='谢谢!'">请点击该文本</h1>  //很多HTML元素都有onclick方法，h1也有，p也有  
document.getElementById("id").onclick=function(){displayDate()};  //本句作用等同于上句  
object.prototype.name=value; //使用prototype可以向对象添加成员变量  
&lt script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.min.js" &gt &lt /script &gt //引用jQuery  
```  

## 相关网络协议
### http协议  
URL 只能使用 ASCII 字符集来通过因特网进行发送，有些网站会包含 ASCII 集合之外的字符，这时候就需要使用 "%" 其后跟随两位的十六进制数来替换非 ASCII 字符。  
### tcp协议


## 相关框架

### jQuery框架
更简洁的js代码框架，能更好地使用js  

### BootStrap框架
响应式web设计框架，封装了css，更快布局  
