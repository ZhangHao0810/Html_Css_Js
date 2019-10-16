
### 使用BootStrap开发一个响应式的页面出来

#### 需求分析

开发一套响应式页面.让他能够在各种设备上显示正常,提升用户体验

#### 技术分析

##### BootStap概述

- BootStrap有什么作用

  - 复制粘贴, 能够提高开发人员的工作效率

- 什么是响应式页面
  - 适应不同的分辨率显示不同样式,提高用户的体验

    ​
- BootStrap的中文网
  - http://www.bootcss.com
- 下载BootStrap
- BootStrap结构
  - 全局CSS
    - bootStrap中已经定义好了一套CSS的样式表
  - 组件
    - BootStrap定义的一套按钮,导航条等组件
  - JS插件
    - BootStrap定义了一套JS的插件,这些插件已经默认实现了很多种效果

##### [BootStrap的入门开发](BootStrap/03-bootstrap)

- 引入相关的头文件

```html
    <!-- 最新版本的 Bootstrap 核心 CSS 文件 -->
    <link rel="stylesheet" href="../css/bootstrap.css" />
    
    <!--需要引入JQuery-->
    <script type="text/javascript" src="../js/jquery-1.11.0.js" ></script>
    
    <!-- 最新的 Bootstrap 核心 JavaScript 文件 -->
    <script type="text/javascript" src="../js/bootstrap.js" ></script>
    
    <meta name="viewport" content="width=device-width, initial-scale=1">
```

- BootStrap的布局容器

`.container` 类用于固定宽度并支持响应式布局的容器。

```
<div class="container">
  ...
</div>
```

`.container-fluid` 类用于 100% 宽度，占据全部视口（viewport）的容器。

```
<div class="container-fluid">
  ...
</div>
```


校验表单扩展:

trigger  : 触发浏览器默认行为

triggerHandler : 不会触发

is : 判断

find : 查找



- row

   Bootstrap 栅格系统的工作原理：

  - “行（row）”必须包含在 `.container` （固定宽度）或 `.container-fluid` （100% 宽度）中，以便为其赋予合适的排列（aligment）和内补（padding）。
  - 通过“行（row）”在水平方向创建一组“列（column）”。
  - 你的内容应当放置于“列（column）”内，并且，只有“列（column）”可以作为行（row）”的直接子元素。
  - 类似 `.row` 和 `.col-xs-4` 这种预定义的类，可以用来快速创建栅格布局。Bootstrap 源码中定义的 mixin 也可以用来创建语义化的布局。
  - 通过为“列（column）”设置 `padding` 属性，从而创建列与列之间的间隔（gutter）。通过为 `.row` 元素设置负值 `margin` 从而抵消掉为 `.container` 元素设置的 `padding`，也就间接为“行（row）”所包含的“列（column）”抵消掉了`padding`

  ​

- BootStrap的栅格系统

  - 响应式设计: 这种设计依赖于CSS3中的媒体查询
  - 栅格样式:
    - 设备分辨率大于1200 使用lg样式
    - 设备分辨率大于992 < 1200 使用md样式
    - 设备分辨率大于768 < 992  使用sm样式
    - 设备分辨率小于768使用xs样式

- BootStrap的全局CSS
  - 定义了一套CSS
    - 对页面中的元素进行定义
    - 列表元素,表单,按钮,图片...


#### [使用BootStrap布局网站首页](03-bootstrap/网站首页.html)

#### 需求分析

请使用BootStrap对我们的首页进行优化

#### 技术分析

#### 步骤分析

> 1. 新建一个HTML页面.引入bootStrap相关的js和CSS
> 2. 定义一个整体的div, 将整体的div分成8个部分
> 3. 完成没部分的内容显示





### 五天前端内容总结

- JQ方式校验表单(要求做出来)
- json :  (了解)
  - json对象 {}
  - json数组 [{},{}]
- $.get(url,function(data){}) (了解)
- bootstrap:  Bootstrap 是最受欢迎的 HTML、CSS 和 JS 框架，用于开发响应式布局、移动设备优先的 WEB 项目。
  - 全局CSS样式: css样式
    - 栅格系统:
      - 将屏幕划分成12个格子,12列
      - class='row' 当前是行
      - 行里面放的是列 col-屏幕分辨率-数字    (每一种分辨率后的数字总和必须是等于12,如果超过12,另起一行)
      - col-lg-数字: 在超宽屏幕上使用
      - col-md-数字: 在中等屏幕上,PC电脑
      - col-sm-数字:  在平板电脑上
      - col-xs-数字:  在手机上
  - 组件:  导航条 , 进度条, 字体
  - javascript插件 : 轮播图
  - 复制粘贴
- 什么是响应式: 会根据不同的分辨率去显示不同页面结构,提高用户体验



- HTML: 超文本标记语言: 设计网页,决定了网页的结构

- CSS:  层叠样式表 ,主要是用来美化页面, 将美化和HTML代码进行分离,提高代码复用性

- javascript: 脚本语言,由浏览器解释执行, 弱类型语言(var i), 提供用户交互

- jquery:  javascript函数库,进一步的封装

  - 选择器:

    - ID选择器
    - 类选择器
    - 元素选择器
    - 通配符选择器
    - 选择器分组

  - 层级选择器

    - 后代选择器
    - 子元素选择器
    - 相邻兄弟选择器
    - 兄弟选择器 : 找出所有的弟弟

  - 属性选择器:

    - 选择器[属性名称='属性的值']

  - 表单选择器

    - :input
    - :text
    - :password

    body > div > div:nth-child(7) > div:nth-child(3) > div:nth-child(8)

  - 基本的过滤器

    - :first
    - :last
    - :even
    - :odd
    - :gt
    - :lt
    - :eq

  - 表单对象属性

    - :selected
    - :checked


