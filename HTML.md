# **html基础**
## 什么是html
* 全称为超文本标记语言，在html里任何对文本的操作都可以经过标记实现，这里的标记就是指html代码中的标签。代码格式:`<标签>内容</标签>`。
## html的规范
1. 一个html文件开始标签和结束标签必须是`<html> </html>`
2. html包含两个部分
(1). `<head>`设置相关信息`</head>`
(2). `<body>`显示在页面上的内容都写在body里面`</body>`
3. html代码不区分大小写
4. 有些标签没有结束标签，在标签内结束，例如：`<br/> <hr/>`
## html的操作思想
* 网页中有很多数据，不同的数据可能需要不同的显示效果，这个时候需要使用标签把要操作的数据包起来（封装起来），通过修改标签的属性值实现标签内数据样式的变化。
一个标签相当于一个容器，想要修改容器内数据的样式，只需要改变容器的属性值，就可以实现容器内数据样式的变化。
## html常用标签
1. 文字标签和注释标签
	* 文字标签：修改文字的样式
		- `<font></font>`
		- 属性：
			* size: 文字的大小 取值范围 1-7,超出了7，默认还是7
			* color：文字颜色
				- 两种表示方式
					** 英文单词：red  green  blue  black  white  yellow   gray......
					** 使用十六进制数表示 #ffffff :  RGB
						- 通过工具实现不同的颜色   #66cc66

	* 注释标签
		- java注释几种？三种
		- html的注释 ： `<!--  html的注释  -->`
2. 标题标签、水平线标签和特殊字符
	* 标题标签 
		- `<h1></h1>  <h2></h2>  <h3></h3> .......<h6></h6>`
		- 从h1到h6，大小是依次变小，同时会自动换行
	
	* 水平线标签
		- `<hr/>`
		- 属性
			** size: 水平线的粗细 取值范围 1-7
			** color: 颜色
		- 代码
			`<hr size="5" color="blue"/>`

	* 特殊字符
		- 想要在页面上显示这样的内容   `<html>`:是网页的开始！
		- 需要对特殊字符进行转义
			* <  :  `&lt;`
			* `> :  &gt;`
			* 空格：`&nbsp;`
			* &  :` &amp;`
	
3. 列表标签
	- 比如现在显示这样的效果
		*  传智播客
			 *  财务部
			 *  学工部
			 *  人事部
	-  `<dl> </dl>`: 表示列表的范围
		 在dl里面  `<dt></dt>`: 上层内容
		 在dl里面  `<dd></dd>`：下层内容
	- 代码 
		```
        <dl>
			<dt>传智播客</dt>
			<dd>财务部</dd>			
			<dd>学工部</dd>
			<dd>人事部</dd>
		</dl>
        ```
	
	- 想要在页面上显示这样的效果
	  1. 财务部
	  2. 学工部
	  3. 人事部

	  a. 财务部
	  b. 学工部
	  c. 人事部

	  i. 财务部
	  ii. 学工部
	  iii. 人事部
	
	- ` <ol></ol> `: 有序列表的范围
		- 属性 type：设置排序方式 1(默认)  a  i
	   ** 在ol标签里面` <li>具体内容</li>`
	- 代码
		```
        <ol>
			<li>财务部</li>
			<li>学工部</li>
			<li>人事部</li>
		</ol>
        ```
	
	- 想要在页面上显示这样的效果
		特殊符号（方框） 财务部
		特殊符号（方框） 学工部

		- `<ul></ul> `: 表示无序列表的范围
			* 属性： type: 空心圆circle 、实心圆disc 、实心方块square ，默认disc
			* 在ul里面  `<li></li>`
		- 代码
			```
            <ul>
				<li>财务部</li>
				<li>学工部</li>
				<li>人事部</li>
			</ul>
            ```

4. 图像标签
	* `<img src="图片的路径"/>`
		- src: 图片的路径
		- width：图片的宽度
		- height：图片的高度

		- alt: 图片上显示的文字，把鼠标移动到图片上，停留片刻显示内容
			** 有些浏览器下不显示（没有效果）
	* 图片格式
		* 效果一样，用小的，效果不一样，用好的
		- jpeg（jpg）
			- 支持的颜色比较丰富，不支持透明效果，不支持动图，一般用来显示照片
		- gif
			- 支持的颜色比较少，支持简单透明，支持动图，用来显示颜色单一的图片以及动图
		- png（在网页中用的最多的）
			- 支持的颜色丰富，支持复杂透明，不支持动图，用来显示颜色丰富、复杂透明图片（为网页而生）
		- webp
			- 谷歌新推出的专门用来表示网页中的图片的一种格式，具有所有图片格式的优点，文件也特别小，但是兼容性不好
	    * base64
			- 对图片进行编码，将图片转换成字符，通过字符形式引入，可以对图片实现加密效果
			- 只有一些需要和网页一起加载的图片才用这种方式，图片加载速度会比较快


5. 路径的介绍
	- 分类：两类
	- 绝对路径
		* 完整的路径
	- 相对路径
		
6. 超链接标签
	* 链接资源
		- `<a href="链接到资源的路径"> 显示在页面上的内容  </a>`
			* href: 链接的资源的地址
			* target：设置打开的方式 ，默认是在当前页打开
				- _blank : 在一个新窗口打开
				- _self: 在当前页打开 默认
		- 当超链接不需要到任何的地址 在href里面加#
			- `<a href="#">这是一个超链接2</a>`

	* 定位资源
		- 如果想要定位资源：定义一个位置 
			`<a name="top">顶部</a>`
		- 回到这个位置
			`<a href="#top">回到顶部</a>`
		
		- 引入一个标签 pre：原样输出
	
7. 表格标签（**重要的标签**）
	* 可以对数据进行格式化，使数据显示更加清晰

	* `<table></table>`: 表示表格的范围
		- border：表格线
		- bordercolor：表格线的颜色
		- cellspacing：单元格直接的距离
		- width：表格的宽度
		- height：表格的高度

	* 在table里面 `<tr></tr>`
		-  设置对齐方式 align： left  center  right

	   -  在tr里面 `<td></td>`
	   - 设置显示方式 align： left  center  right

	   * 使用th也可以表示单元格
		- 表示可以实现居中和加粗

	* 代码: 
		`<table border="1" bordercolor="blue" cellspacing="0" width="200" height="150">`
	
	* 画图分析表格的写法
		- 首先定义一个表格的范围使用table
			- 定义一行使用 tr
			- 定义一个单元格使用 td
	* 操作技巧：
		- 首先数有多少行 ，数每行里面有多少个单元格
	
	* 表格的标题:
		`<caption></caption>`

	* 合并单元格 
		- rowspan：跨行
			* `<td rowspan="3">人员信息</td>`
		- colspan：跨列
			* `<td colspan="3">人员信息</td>`

8. 表单标签 (**重要的标签**)
	* 可以提交数据到开心网的服务器，这个过程可以使用表单标签实现

	* `<form></form>`: 定义一个表单的范围
		- 属性
			* action： 提交到地址，默认提交到当前的页面
			* method:  表单提交方式 
				- 常用的有两种  get和post，默认是get请求

			* 面试题目： get和post区别
				1、get请求地址栏会携带提交的数据，post不会携带（请求体里面。在第七天时候讲http协议时候）
				2、get请求安全级别较低，post较高
				3、get请求数据大小的限制，post没有限制
			
			* enctype：一般请求下不需要这个属性，做文件上传时候需要设置这个属性（第22天时候讲文件上传）

	* 输入项：可以输入内容或者选择内容的部分
		- 大部分的输入项 使用  `<input type="输入项的类型"/>`

		- 在输入项里面需要有一个name属性

		* 普通输入项：`<input type="text"/>`
		* 密码输入项：`<input type="password"/>`


		* 单选输入项：`<input type="radio"/>`
			- 在里面需要属性 name
			- 在进行两个及以上内容的选择时name的属性值必须要相同
			- 必须有一个value值，以便通过协议传到到其他特面之类

			* 实现默认选中的属性 
				- `checked="checked"`

		* 复选输入项：`<input type="checkbox"/>`
			- 在里面需要属性 name
			- name的属性值必须要相同
			- 必须有一个value值

			* 实现默认选中的属性 
				- `checked="checked"`
		
		* 文件输入项（在后面上传时候用到）
			- `<input type="file"/>`
		

		* 下拉输入项（不是在input标签里面的）
			```
            <select name="birth">
				<option value="1991">1991</option>
				<option value="1992">1992</option>
				<option value="1993">1993</option>
			</select>
            ```

			- 默认选择
				* `selected="selected"`
		
		* 文本域
			`<textarea cols="10" rows="10"></textarea>`
		
		* 隐藏项（不会显示在页面上，但是存在于html代码里面）
			`<input type="hidden" />`
		
		* 提交按钮:
			`<input type="submit"/>`
			`<input type="submit" value="注册"/>`
			
			* 输入项name的值=输入的值&
			* 参数类似于key-value形式

		* 使用图片提交
			`<input type="image" src="图片路径"/>`
		
		* 重置按钮： 回到输入项的初始状态
			`<input type="reset"/>`
		
		* 普通按钮(和明天讲js在一起使用的)
			`<input type="button" value=""/>`
9. html中的其他的常用标签的使用
	- b : 加粗
	- s ：删除线
	- u ：下划线
	- i ：斜体
	
	- pre ：原样输出
	
	- sub : 下标
	- sup : 上标

	- p ：段落标签 比br标签多一行
	
	- css时候一直使用
	- div ：自动换行
	- span：在一行显示

10. html的头标签的使用
	* html两部分组成 head和body
	 -  在head里面的标签就是头标签

	* title标签：表示在标签上显示的内容
	* `<meta>`标签：设置页面的一些相关内容
		 ```
        <meta name="keywords" content="毕姥爷，熊出没，刘翔">
		  <meta http-equiv="refresh" content="3;url=01-hello.html" />
          ```
	* base标签：设置超链接的基本设置
		- 可以统一设置超链接的打开方式 
		 `<base target="_blank"/>`
	* link标签：引入外部文件
		- css，可以使用link标签引入css文件
		
11. 框架标签的使用（会用）
	* `<frameset>`
		- rows:按照行进行划分
			* `<frameset rows="80,*">`

		- cols:按照列进行划分
			* `<frameset cols="80,*">`
	* `<frame>`
		- 具体显示的页面
			- `<frame name="lower_left" src="b.html"> `
	
	*  使用框架标签时候，不能写在body里面，使用了框架标签，需要把body去掉

	``` 
    <frameset rows="80,*">                        //把页面划分成上下两部分 
	     <frame name="top" src="a.html">             //上面页面
	
		<frameset cols="150,*">                     //把下面部分划分成左右两部分
			<frame name="lower_left" src="b.html">  //左边的页面
			<frame name="lower_right" src="c.html"> //右边的页面
		</frameset> 
	</frameset> 
    ```

	* 如果在左边的页面超链接，想让内容显示在右边的页面中
		- 设置超链接里面属性 target值设置成名称
		- `<a href="01-hello.html" target="right">超链接1</a>`
**内联框架**
* 用于向当前页面中引入一个其他页面或者图片的内容
* `<iframe>`

12. a标签的扩展（了解）
	- 百度是网络资源
	- 当a标签里面访问网络资源时候，必须要加一个协议 http：表示一个网络的公共协议，
	- 如果加上http协议之后，自动识别访问资源是一个网络资源

	- 当浏览器里面找到相关协议，首先看这个协议是不是公共协议http。
	- 如果不是公共协议，会去本地电脑找支持这个协议的应用程序。
13. 其他类型的标签
* 语义化标签
	- `header` 表示网页的头部内容
	- `main` 表示网页的主体部分（规定一个页面只能有一个）
	- `footer` 表示网页底部内容
	- `nav` 表示网页中导航内容
	- `aside` 和主体相关的其他内容（侧边栏）
	- `article` 表示一个独立的文章
	- `section` 表示一个独立的区块（上面的标签都不能表示是使用这个来表示）
	- `audio` 标签用来向页面引入一个外部音频文件，引入的音频文件默认情况下不允许用户控制，可以通过属性设置来进行设置
	- `div` 没有具体意义，用来表示一个区块，是一般程序员使用的主要布局元素
	- `span` 行内元素，没有任何意义，一般用于在页面中选中文字

