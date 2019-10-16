2019年10月16日20:28:31

## 什么是JQuery:

jQuery是一个快速、简洁的JavaScript框架，是继Prototype之后又一个优秀的JavaScript代码库（*或JavaScript框架*）。jQuery设计的宗旨是“write Less，Do More”，即倡导写更少的代码，做更多的事情。它封装JavaScript常用的功能代码，提供一种简便的JavaScript设计模式，优化HTML文档操作、事件处理、动画设计和Ajax交互。

jQuery的核心特性可以总结为：具有独特的链式语法和短小清晰的多功能接口；具有高效灵活的css选择器，并且可对CSS选择器进行扩展；拥有便捷的插件扩展机制和丰富的插件。jQuery兼容各种主流浏览器，如IE 6.0+、FF 1.5+、Safari 2.0+、Opera 9.0+等

### JQuery的作用:

​	1. 写更少的代码,做更多的事情: write Less ,Do more   
    2. 将我们页面的JS代码和HTML页面代码进行分离  

### 为什么学习JQuery:

​	提高我们的工作效率


#### JQ的开发步骤: 

	1. 导入JQ相关的文件
	2.  文档加载完成事件: $(function)  : 页面初始化的操作: 绑定事件, 启动页面定时器
	3. 确定相关操作的事件
	4. 事件触发函数
	5. 函数里面再去操作相关的元素

### [JQ的入门](01-网页定时弹出广告/JQ的入门/JQ的入门.html)


##### [ JQ中根据ID查找元素](01-网页定时弹出广告/JQ的入门/JQ查找元素.html)

```html
全都是根据选择器去找的
#ID{}
.类名{}
$("#ID的名称")
```

##### [JQ和JS之间的转换](01-网页定时弹出广告/JQ的入门/JQ和JS对象之间的转换.html)

- JQ对象,只能调用JQ的属性和方法
- JS对象 只能调用JS的属性和方法


##### [JQ中的动画效果](01-网页定时弹出广告/JQ的入门/动画效果.html)


动画效果:

​	show : 显示

​	hide : 隐藏

​	slideDown: 

​	slideUp: 向上滑动

​	fadeIn

​	fadeOut


#### 1.3 步骤分析：

1. 导入JQ的文件
2. 编写JQ的文档加载事件
3. 启动定时器 setTimeout("",3000);
4. 编写显示广告的函数
5. 在显示广告里面再启动一个定时器
6. 编写隐藏广告的函数



### JQuery中的选择器

让我们能够更加精确找到我们要操作的元素	

##### [基本选择器](01-网页定时弹出广告/JQ的入门/选择器/基本选择器.html)

- ID选择器 :     #ID的名称
- 类选择器:     以 . 开头  .类名
- 元素选择器:    标签的名称
- 通配符选择器:   * 
- 选择器,选择器:  选择器1,选择器2

##### [JQ中的层级选择器](01-网页定时弹出广告/JQ的入门/选择器/层级选择器.html)

- 子元素选择器: 选择器1 > 儿子
- 后代选择器: 选择器1 儿孙
- 相邻兄弟选择器 :  选择器1 + 选择器2 : 找出紧挨着的一个弟弟
- 所有弟弟选择器: 选择器1~ 选择器2 找出所有的弟弟

##### [JQ中的基本过滤器](01-网页定时弹出广告/JQ的入门/选择器/基本过滤器.html)

基本过滤器:

​	选择器:first  : 找出的是第一个

​	:last  

​	:even   找出索引为偶数

​	:odd    找出奇数索引

​	:gt(index) :  大于索引

​	:lt(index)   小于

​	:eq(index)  等于

##### [JQ中的属性选择器](01-网页定时弹出广告/JQ的入门/选择器/属性选择器.html)

属性选择器:

```html
选择器[href]  : 单个属性
选择器[href][title] : 多个属性
选择器[href][title='test'] : 多个属性,包含值
```

##### [JQ中的表单过滤器](01-网页定时弹出广告/JQ的入门/选择器/表单选择器.html)

```html
<script>
  //1.文档加载事件	
  $(function(){
    $(":text").css("background-color","pink");
  });
</script>
```
​	:input   找出所有输入项:  input  textarea  select 

​	:text 

​	:password  

表单对象属性:

​	找出select中被选中的那一项:

​	option:selected

## JQuery的使用，结合案例学习。


#### [1.使用JQuery完成页面定时弹出广告](01-网页定时弹出广告/网页定时弹出广告.html)

#### 1.1 需求分析：

当用户打开界面，3秒钟之后弹出广告，这个广告显示5秒钟，隐藏广告

#### 1.2 技术分析

定时器: 

​	setInterval     clearInterval

​	setTimeout    clearTimeout

显示:  img.style.display  = "block"

隐藏:  img.style.display  = "none"

img 对象

​	style属性:  style对象

#### [2.使用JQuery完成表格的隔行换色](02-表格的隔行换色/表格的隔行换色.html)


#### 需求分析:

在我们的实际开发过程中,我们的表格如果所有的行都是一样的话,很容易看花眼,所以我们需要让我们的表格隔行换色

#### 技术分析:

获取所有行 table.rows[]

​	row.bgColor ="red"

​	row.style.backgroundColor = "black"

​	row.style.background = "red"

​	"background-color:red"

​	"background:red"

根据行号去修改每一行的背景颜色: bgColor

​	style.backgroundColor = "red"


#### 步骤分析:

1. 导入JQ的包
2. 文档加载完成函数: 页面初始化
3. 获得所有的行 :   元素选择器
4. 根据行号去修改颜色




#### [3.使用JQuery完成复选框的全选效果](/03-全选和全不选/全选和全不选.html)

#### 需求分析

​	在我们对表格处理的时,有些情况下,我们需要对表格进行批量处理,

checked属性

如何获取所有复选框:

​	document.getElementsByName   get Elements  By Name  数据库里面

#### [4.使用JQuery完成省市联动效果](/04-省市联动效果/省市联动.html)


#### 需求分析:

​	在我们的注册表单中,通常我们需要知道用户的籍贯,需要一个给用选择的项,当用户选中了省份之后,列出省下面所有的城市

#### 技术分析:

1. 准备工作 : 城市信息的数据

2. 添加节点 :  appendChild (JS)

   1. append  :  添加子元素到末尾
   2. appendTo  : 给自己找一个爹,将自己添加到别人家里
   3. prepend : 在子元素前面添加
   4. after :   在自己的后面添加一个兄弟

3. 遍历的操作:

   ​	

#### 步骤分析:

1. 导入JQ的文件
2. 文档加载事件:页面初始化
3. 进一步确定事件:  change事件
4. 函数: 得到当前选中省份
5. 得到城市, 遍历城市数据
6. 将遍历出来的城市添加到城市的select中

​	JS中的数组:  ["城市"]

​	new Array()

​	DOM树操作:

​		创建节点:  document.createElement

​		创建文本节点: document.createTextNode

​		添加节点:  appendChild

#### [5.使用JQuery完成下列列表左右选择](05-下拉列表左右选择/商品的左右选择.html)

#### 需求分析

我们的商品通常包含已经有了的, 还有没有的,现在我们需要有一个页面用于动态编辑这些商品

#### 步骤分析

	1. 导入JQ的文件
	2. 文档加载函数 :页面初始化
	3.确定事件 :　点击事件　onclick
	4. 事件触发函数
	1. 移动被选中的那一项到右边


​	select下拉列表

​	multiple 允许多选

​	ondblclick : 双击事件

​	for循环遍历,一边遍历一边移除出现的问题


#### [6.使用JQuery完成表单的校验(扩展)](07-JQ方式完成表单校验/表单校验.html)


#### 需求分析

在用户提交表单的时候, 我们最好是能够在用户数据提交给服务器之前去做一次校验,防止服务器压力过大,并且需要给用户一个友好提示

#### 技术分析
- trigger :
  会执行类似浏览将光标移到输入框内的这种浏览器默认行为，并且触发事件对应的函数
- triggerHandler : 仅仅只会触发事件所对应的函数
- is()

#### 步骤分析

1. 首先给必填项,添加尾部添加一个小红点
2. 获取用户输入的信息,做相应的校验
3. 事件: 获得焦点, 失去焦点, 按键抬起
4. 表单提交的事件



​	事件:

​	获得焦点事件: onfocus

​	失去焦点事件: onblur

​	按键抬起事件: onkeyup

​	鼠标移入:  onmouseenter

​	鼠标移出: onmouseout

​	JS引入外部文件 : script 


	数据交换格式:

​		json

​		xml

- 什么是JSON

  [JSON](http://baike.baidu.com/view/136475.htm)([JavaScript](http://baike.baidu.com/view/16168.htm) Object Notation) 是一种轻量级的数据交换格式。它基于[ECMAScript](http://baike.baidu.com/view/810176.htm)的一个子集。 JSON采用完全独立于语言的文本格式，但是也使用了类似于C语言家族的习惯（包括[C](http://baike.baidu.com/subview/10075/6770152.htm)、C++、[C#](http://baike.baidu.com/view/6590.htm)、[Java](http://baike.baidu.com/subview/29/12654100.htm)、JavaScript、[Perl](http://baike.baidu.com/view/46614.htm)、[Python](http://baike.baidu.com/view/21087.htm)等）。这些特性使JSON成为理想的数据交换语言。 易于人阅读和编写，同时也易于机器解析和生成(一般用于提升网络传输速率)。

- JSON格式

  ​	JSON对象

```
{ key1:value}   
{"username":"zhangsan","password":"123"}
```

  ​	JSON数组

  ```
  [{ key1:value},{ key1:value},{ key1:value}]
  ```



#### 内容总结:

定时器

动画效果: show  hide  slideDown  slideUp fadeIn  fadeOut  animate

基本选择器:

​	ID选择器: #ID名称

​	类选择器: .类名

​	元素选择器: 元素/标签名称

​	通配符选择器:  *  找出所有页面元素 包含页面上所有的标签

​	选择器分组 :   选择器1, 选择器2      [选择器1,选择器2]

层级选择器:

​	后代选择器: 选择器1 选择器2  找出来的选择器1 下面的所有选择器2  子孙

​	子元素选择器: 选择器1 > 选择器2   找出来的是所有的子节点  儿子

​	相邻兄弟选择器: 选择器1+选择器2    找出来的紧挨着自己的弟弟

​	兄弟选择器:   选择器1~选择器2    找出所有的弟弟

​		(找出所有兄弟:   $("div").siblings()    )

属性选择器:

​	选择器[属性名称]

```html
选择器 div
选择器[title]
选择器[title='test']
选择器[title='test'][style]
```


基本的过滤器:    选择器:过滤器   $("div:first")

​	:first : 找出第一个元素

​	:last  找出最后一个元素

​	:even   找出偶数索引

​	:odd   找出奇数

​	:gt(index)   greater-than大于

​	:lt(index)    小于

​	:eq(index)  等于


表单选择器:

​	:input   找出所有的输入项 : 不单单找出input  textarea select button

​	:text  找出type类型为 text

​	:password

	:radio

表单对象属性的过滤器

​	:selected

​	:checked

常用函数:

$(function)  : 文档加载完成的事件

html() : 修改innerHTML ​	属性

    prop() properties+

​		如果传入一个参数  就是获取

​	prop("src","../img/1.jpg");  

​		设置图片路径

​	attr : 操作一些自定义的属性  <img  abc='123' />

​	prop: 通常是用来操作元素固有属性的 ,建议大家使用prop来操作属性



​	css() ; 修改css样式

​	addClass()  : 添加一个class样式

​	removeClass() : 移除

​	

​	blur : 绑定失去焦点

​	focus: 绑定获得焦点事件

​	click:

​	dblclick

​	change

​	

​	append    :  给自己添加儿子

​	appendTo :  把自己添加到别人家

​	prepend :  在自己子节点最前面添加子节点

​	after  : 在自己后面添加一个兄弟

​	before: 在自己前面添加一个兄弟

​	empty	:   清空所有子节点


​	$("数组对象").each(function(index,data))

​	$.each(arr,function(index,data))

`$(cities).each(function(i,n){ }) $.each(arr,function(i,n){ });`


