### HTML基础:

#### 网站信息案例
  - 字体标签 font
    - color: 颜色
    - size:  大小 1~7
    - face: 改变字体
  - p 段落标签
  - h标题标签 : 1~6
  - br 换行
  - hr 水平线
  - b 加粗
  - i  斜体
  - strong : 加粗  包含语义
  - em : 斜体  包含语义
#### [网站图片案例](网站图片案例.html)
  - img标签
    - src : 指定图片的路径
    - width: 宽度
    - height: 高度
    - alt : 图片加载错误时的提示信息
  - 相对路径:
    - ./  代表的是当前路径
    - ../  代表的上一级路径
    - ../../ 代表的上上一级路径
#### [友情链接:](友情链接.html)
  - ul: 无序列表
    - type : 样式
  - ol: 有序列表
    - type : 样式
    - start : 起始索引
  - li : 列表项
  - a 超链接标签
    - href : 要访问的链接地址
    - target : 在何处打开链接文档。
#### 网站首页 
表格标签
  - table标签
    - border: 指定边框
    - width : 宽度
    - height : 高度
    - bgcolor : 背景颜色
    - align : 对齐方式
    - tr标签
    - td标签   
  - 表格单元格的合并  
    - colspan: 跨列操作
    - rowspan: 跨行操作  
     注意: 跨行或者跨列操作之后,被占掉的格子需要删除掉 
  - 表格的嵌套  
    在td中可以嵌套一个表格
    
#### [网站注册页面](网站注册页面.html)

表单标签
- action : 直接提交的地址
  
- method : 
  -  get 方式 默认提交方式 ,会将参数拼接在链接后面 , 有大小限制 4k 
  - post 方式 会将参数封装在请求体中, 没有大小的限制
  
- input :
  - type: 指定输入项的类型
    - text : 文本 
    - password : 密码框 
    - radio : 单选按钮
    - checkbox : 复选框
    - file : 上传文件
    - submit : 提交按钮
    - button : 普通按钮
    - reset	: 重置按钮
    - hidden : 隐藏域
    - date    : 日期类型 
    - tel     : 手机号  
    - number   : 只允许输入数字  
  
- placeholder :** 指定默认的提示信息  **
- name : 在表单提交的时候,当作参数的名称  
- id : 给输入项取一个名字, 以便于后期我们去找到它,并且操作它  

- textarea : 文本域, 可以输入一段文本  
    - cols : 指定宽度  
    - rows : 指定的是高度  

- select  : 下拉列表  
    option : 选择项      
    
#### [框架标签](框架标签.html)   
- frameset  

注意: 使用了frameset必须将body删掉,否则页面会有问题  

- frame  
  - 常用属性:  
  - src: 引入的html文件路径  
  -	name: 指定框架的名称  
  
  
带链接的句子。把链接地址放到target指定的框当中。

    <h3>Table of Contents</h3>
    <ul>
      <li><a href="pref.html" target="view_window">Preface</a></li>
      <li><a href="chap1.html" target="view_window">Chapter 1</a></li>
      <li><a href="chap2.html" target="view_window">Chapter 2</a></li>
      <li><a href="chap3.html" target="view_window">Chapter 3</a></li>
    </ul> 
另一个文件：

    <frameset cols="100,*">
      <frame src="toc.html">
      <frame src="pref.html" name="view_frame">
    </frameset> 