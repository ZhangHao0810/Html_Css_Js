# JavaScript基础 结合案例。

##### JavaScript概述

什么是javascript: 一种直译式脚本语言，

什么是脚本语言?  
​	java源代码 ----> 编译成.class文件 -----> java虚拟机中才能执行  
​	脚本语言:   源码  -------- > 解释执行  
​	js由我们的浏览器来解释执行

- HTML: 决定了页面的框架  
- CSS: 用来美化我们的页面
- JS:	提供用户的交互的

##### JS的组成:

ECMAScript : 核心部分 ,定义js的语法规范

DOM: document Object Model 文档对象模型 , 主要是用来管理页面的

BOM : Browser Object Model  浏览器对象模型, 前进,后退,页面刷新, 地址栏, 历史记录, 屏幕宽高

##### JS的语法:

- 变量弱类型: var i = true
- 区分大小写
- 语句结束之后的分号 ,可以有,也可以没有
- 写在script标签


##### JS的数据类型:

- 基本类型
  - string
  - number
  - boolean 
  - undefine
  - null
- 引用类型
  - 对象, 内置对象
- 类型转换
  - js内部自动转换 

##### JS的运算符和语句:

- 运算符和java 一样
  - "===" 全等号: 值和类型都必须相等
  - == 值相等就可以了
- 语句和java 一样


##### JS的输出

- alert()  直接弹框
- document.write()  向页面输出
- console.log() 向控制台输出
- innerHTML:  向页面输出
- 获取页面元素: document.getElementById("id的名称");


#### JS的开发步骤

```html
1. 确定事件
2. 通常事件都会出发一个函数
3. 函数里面通常都会去操作页面元素,做一些交互动作
```

## 下面开始结合案例进行学习：

### [0.简单的数据校验](00-JS入门案例/使用JS完成简单的数据校验.md)

### [0. 轮播图自动播放](01-自动轮播图片)

#### 需求: 

有一组图片, 每隔3秒钟,就去切换一张,最终是一直在不停切换

#### 技术分析:

​	切换图片:  
​	每个三秒钟做一件事:


### [1. 完成页面定时弹出广告](02-网站定时弹出广告)

#### 1.1 需求分析

​	一般网页，当我们刚打开的时候，它会5秒之后，显示一个广告，让我们看5秒钟，然后他的广告就自动消失了！

#### 1.2 技术分析

- 定时器
  - setInterval : 每隔多少毫秒执行一次函数
  - setTimeout: 多少毫秒之后执行一次函数
  - clearInterval
  - clearTimeout
- 显示广告 img.style.display  = "block"
- 隐藏广告 img.style.display  = "none"


#### 引入一个外部js文件 

```html
<script src="js文件的路径"  type="text/javascript"/>
```

### [2. 完成表单的校验](03-JS表单校验)

#### 2.1 需求分析

​	昨天我们做了一个简单的表单校验，每当用户输入出错的时候，我们是弹出了一个对话框，提示用户去修改。这样的用户体验效果非常不好好。我们今天就是需要来对他进行一个修改，当用户输入信息有问题的时候，我们就再输入框的后面给他一个友好提示。

#### 2.2 技术分析

【HTML中innerHTML属性】

【JS中的常用事件】
​	onfocus: 获取焦点事件

​	onblur : 失去焦点的事件

​	onkeyup: 按键抬起的事件

​	onclick:  单击事件

​	ondblclick:  双击事件 

表格隔行换色,鼠标移入和移除要变色:

​	onmouseenter:  鼠标移入

​	onmouseout:  鼠标移出

​	onload:  文档加载完成事件

​	onsubmit:  提交

​	onchange:   下拉列表内容改变

checkbox.checked  选中状态
### [3.表格隔行换色](04-表格的隔行换色/表格隔行换色.html)

#### 3.1 需求分析

​	我们商品分类的信息太多，如果每一行都显示同一个颜色的话会让人看的眼花，为了提高用户体验，减少用户看错的情况，需要对表格进行隔行换

### [4. 复选框的全选和全不选](05-表格的全选和全不选/表格全选和全不选.html)

#### 4.1 需求分析

​	商品分类界面中，当我们点击全选框的时候，我们希望选中所有的商品，当我们取消掉的时候，我们希望不选中所有的商品

#### 4.2 技术分析

​	事件 : onclick点击事件

### [5. 省市联动效果](06-省市联动案例/省市联动.html)


#### 5.2 技术分析

什么是DOM: Document Object Model : 文件对象模型,用来管理我们的文档 增删改查规则

[【HTML中的DOM操作】](06-省市联动案例/DOM操作.html)

```html
一些常用的 HTML DOM 方法：

​	添加节点: appendChild

​	创建节点: document.createElement

​	创建文本节点: document.createTextNode()

  getElementById(id) - 获取带有指定 id 的节点（元素） 
  appendChild(node) - 插入新的子节点（元素） 
  removeChild(node) - 删除子节点（元素） 

  一些常用的 HTML DOM 属性：
  innerHTML - 节点（元素）的文本值 
  parentNode - 节点（元素）的父节点 
  childNodes - 节点（元素）的子节点 
  attributes - 节点（元素）的属性节点 

查找节点：
getElementById() 返回带有指定 ID 的元素。 
getElementsByTagName() 返回包含带有指定标签名称的所有元素的节点列表（集合/节点数组）。 
getElementsByClassName() 返回包含带有指定类名的所有元素的节点列表。 

增加节点：
createAttribute() 创建属性节点。 
createElement() 创建元素节点。 
createTextNode() 创建文本节点。 
insertBefore() 在指定的子节点前面插入新的子节点。 
appendChild() 把新的子节点添加到指定节点。 

删除节点：
removeChild() 删除子节点。 
replaceChild() 替换子节点。 

修改节点：
setAttribute()  修改属性
setAttributeNode()  修改属性节点
```




### [6. 使用JS控制下拉列表左右选择](07-商品的左右选择/商品的左右选择.html)

#### 6.1 需求分析:

在我们的分类管理中,我们要能够去修改我们的分类信息,当我们一点修改的时候,跳转到一个可以编辑的页面,这里面能够修改分类的名称,分类的描述,以及分类的商品





