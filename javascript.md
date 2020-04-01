# **javascript基础**
1. javascript的简介
	* 是基于对象和事件驱动的语言，应用与客户端。
		- 基于对象：
			* 提供好了很多对象，可以直接拿过来使用
		- 事件驱动：
			* html做网站静态效果，javascript动态效果
		
		- 客户端：专门指的是浏览器

	* js的特点
		- 交互性
			- 信息的动态交互

		- 安全性
			- js不能访问本地磁盘的文件

		- 跨平台性
			- java里面跨平台性，虚拟机
			- 只有能够支持js的浏览器，都可以运行
	
	* javascript和java的区别（雷锋和雷峰塔）
		- java是sun公司，现在oracle；js是网景公司
		- JavaScript 是基于对象的，java是面向对象
		- java是强类型的语言，js是弱类型的语言
			- 比如java里面 int i = "10";
			- js:  var i = 10; var m = "10";
		- JavaScript只需解析就可以执行，而java需要先编译成字节码文件，再执行。
	
	* javascript的组成（下面js）
		三部分组成
		- ECMAScript
			- ECMA : 欧洲计算机协会
			- 有ECMA组织制定的js的语法，语句.....

		- BOM
			- broswer object model: 浏览器对象模型

		- DOM
			- document object model：文档对象模型

2. js和html的结合方式（两种）
	* 第一种：
		- 使用一个标签 `<script type="text/javascript">  js代码; </script>`
	
	* 第二种：
		- 使用script标签，引入一个外部的js文件
		* 创建一个js文件，写js代码
		- 	`<script type="text/javascript" src="1.js"></script>`
	
	* 使用第二种方式时候，就不要在script标签里面写js代码了，不会执行。

3. js的原始类型和声明变量
	* java的基本数据类型 byte short int long float double char boolean

	* 定义变量 都使用关键字 var

	* js的原始类型（五个）		
		- string: 字符串
			* `var str = "abc";`

		- number：数字类型
			* `var m = 123;`

		- boolean：true和false
			* `var flag = true;`

		- null
			* `var date = new Date();`
			* 获取对象的引用，null表示对象引用为空 ，所有对象的引用也是object				
		- undifined
			* 定义一个变量，没有赋值
			* var aa;
	* typeof(); 查看当前变量的数据类型

4. js的语句
	- java里面的语句： 
		* if判断
		* switch语句
		* 循环 for  while do-while
	
	- js里面的这些语句
		* if判断语句
			* =:表示赋值
			* ==：表示判断

		* switch语句
			- java里面支持数据类型 string支持吗？在jdk1.7开始支持
			- js里面都支持
			- 
			```
			switch(a) {
				case 5:
					break;
				case 6:
					break;
				default:
				......
			 }
			 ```
		* 循环语句 for  while    do-while
			- while循环
			- 
			```
			var i = 5;
			while(i>1) {
				alert(i);
				i--;
			}
			```
			- for循环
			- 
			```
			for(int i=0;i<=10;i++) { }
			for(var mm=0;mm<=3;mm++) {
				alert(mm);
			}
			```
		* i++ ++i和java里面一样

5. js的运算符
	* +=  ： x+=y;  ===> x=x+y;

	* js里面不区分整数和小数
	```
		var j = 123;
		alert(j/1000*1000);  
		//  j/1000*1000    在java里面得到结果是 0 
		// 在js里面不区分整数和小数，123/1000=0.123 * 1000 = 123
	```
	* 字符串的相加和相减的操作
		- `var str = "123";`

		* 如果相加时候，做是字符串连接
		* 如果相减，做的是相减的运算

		* //字符串的操作
		```
		var str = "456";
		//alert(str+1);   //在java里面操作的结果是 4561 ，在js里面还是 4561
		alert(str-1);    //相减时候，执行减法的运算
		```
		* 提示NaN:表示不是一个数字

	* boolean类型也可以操作
		* 如果设置成true，相当于这个值是1
		* 如果设置成false，相当于这个值是0
	
	* == 和 === 区别
		* 做判断

		* == 比较的只是值
		* === 比较的是值和类型
	
	* 引入知识
		直接向页面输出的语句（可以把内容显示在页面上）
		* `document.write("aaa");`
		`document.wirte("<hr/>");`
		* 可以向页面输出变量，固定值和html代码

6. 实现99乘法表（输出到页面上）
	*	
	```
	document.write("<table border='1' bordercolor='blue'>");
		//循环行 9
		for(var i=1;i<=9;i++) {

			document.write("<tr>");
			//循环列
			for(var j=1;j<=i;j++) {
				document.write("<td>");
				//运算
				document.write(j+"*"+i+"="+i*j);
				document.write("</td>");
			}
			//document.write("<br/>");
			document.write("</tr>");
		}
		document.write("</table>");
	```
	- document.write里面是双引号，如果设置标签的属性需要使用单引号
	- document.write可以输出变量，还可以输出html代码
	
7. js的数组
	* 什么是数组？
		- 使用变量，var m = 10;
		- java里面的数组 定义 int[] arr = {1,2,3};

	* 定义方式（三种）
		- 第一种： `var arr = [1,2,3]`;   `var arr = [1,"4",true];`
		- 第二种：使用内置对象 Array对象
		```
			var arr1 = new Array(5);  //定义一个数组，数组的长度是5
			arr1[0] = "1";
		```
		- 第三种：使用内置对象 Array
			`var arr2 = new Array(3,4,5); //定义一个数组，数组里面的元素是3 4 5 `
	
	* 数组里面有一个属性  length：获取到数组的长度

	* 数组可以存放不同的数据类型的数据

8. js的函数
	* 在java里面定义方法
	```
		public 返回类型void /int   方法名(参数列表) {
			方法体;
			返回值;
		}
	
		public int add(int a,int b) {
			int sum = a+b;
			return sum;
		}
	```
	* 在js里面定义函数（方法）有三种方式
		* 函数的参数列表里面，不需要写var，直接写参数名称
		- 第一种方式：
			* 使用到一个关键字 function
			* 
			```
			function 方法名(参数列表) {
				方法体;
				返回值可有可无（根据实际需要）;
			 }
			```
			* 代码
			```
			//使用第一种方式创建函数
			function test() {
				alert("qqqqq");
			}

			//调用方法
			//test();

			//定义一个有参数的方法  实现两个数的相加
			function add1(a,b) {
				var sum = a+b;
				alert(sum);		
			}

			//add1(2,3);

			//有返回值的效果
			function add2(a,b,c) {
				var sum1 = a+b+c;
				return sum1;
			}
			alert(add2(3,4,5));
			```
		* 第二种方式：
			* 匿名函数
			```
				var add = function(参数列表) {
					方法体和返回值;
				}
			```
			* 代码
			```
			//第二种方式创建函数
			var add3 = function(m,n) {
				alert(m+n);
			}	
			//调用方法
			add3(5,6);
			```
		* 第三种方式：（用的少，了解）
			* 动态函数
			* 使用到js里面的一个内置对象 Function
				`var add = new Function("参数列表","方法体和返回值");`

9. js的全局变量和局部变量
	* 全局变量：在script标签里面定义一个变量，这个变量在页面中js部分都可以使用
		- 在方法外部使用，在方法内部使用，在另外一个script标签使用

	* 局部变量：在方法内部定义一个变量，只能在方法内部使用
		- 如果在方法的外部调用这个变量，提示出错
		- SCRIPT5009: “nn”未定义 
		- js的局部变量.html, 行18 字符3
	
	* ie自带了一个调试工具，ie8及其以上的版本中，键盘上 F12，在页面下方出现一个条

10. script标签放在的位置
	* 建议把script标签放到 `</body>`后面
	* 如果现在有这样一个需求：
		在js里面需要获取到input里面的值，如果把script标签放到head里面,会出现问题。html解析是从上到下解析的，script标签放到的是head里面，直接在里面取input里面的值,因为页面还没有解析到input那一行，肯定取不到。

11. js的重载
	* js里面是否有重载？
		- js没有重载，但可以通过aruguments数组来模拟重载的方式来进行重载
		```
		function add1() {
			//比如传递的是两个参数
			if(arguments.length == 2) {
				return arguments[0]+arguments[1];

			} else if (arguments.length == 3) {
				return arguments[0]+arguments[1]+arguments[2];

			} else if (arguments.length == 4) {

				return arguments[0]+arguments[1]+arguments[2]+arguments[3];
			} else {
				return 0;
			}
		}
		```
12. js的String对象
	* 创建String对象
		- `var str = "abc";`
	
	* 方法和属性（文档）
		* 属性 length：字符串的长度

		* 方法
		  - 与html相关的方法
			- bold()：加粗
			- fontcolor(): 设置字符串的颜色
			- fontsize(): 设置字体的大小

			- link(): 将字符串显示成超链接
				* `str4.link("hello.html")`
			
			- sub() sup(): 下标和上标

		* 与java相似的方法
			- concat(): 连接字符串 //concat方法
			```
				var str1 = "abc";
				var str2 = "dfg";
				document.write(str1.concat(str2));
			```
			- charAt():返回指定指定位置的字符串
				 `var str3 = "abcdefg";`
				`document.write(str3.charAt(20)); //字符位置不存在，返回空字符串`
			
			- indexOf()： 返回字符串位置
				```
				 var str4 = "poiuyt";
				document.write(str4.indexOf("w")); //字符不存在，返回-1
				```
			- split()：切分字符串，成数组
				```
				 var str5 = "a-b-c-d";
				var arr1 = str5.split("-");
				document.write("length: "+arr1.length);
				```
			- replace() ： 替换字符串
				* 传递两个参数：
					- 第一个参数是原始字符
					- 要替换成的字符
				```
				 var str6 = "abcd";
				document.write(str6);
				document.write("<br/>");
				document.write(str6.replace("a","Q"));
				```	
			- substr()和substring()
				```
				 var str7 = "abcdefghuiop";
				//document.write(str7.substr(5,5));  //fghui  从第五位开始，向后截取五个字符
				```
				* 从第几位开始，向后截取几位
				```
				document.write("<br/>");
				document.write(str7.substring(3,5)); //de  从第几位开始到第几位结束  [3,5)
				```
				* 从第几位开始，到第几位结束，但是不包含最后哪一位
			
13. js的Array对象
	* 创建数组（三种）
		- `var arr1 = [1,2,3];`
		- `var arr2 = new Array(3); //长度是3`
		- `var arr3 = new Array(1,2,3); //数组中的元素是1 2 3`

		- `var arr = [];  //创建一个空数组`
	
		- 属性：length：查看数组的长度

	* 方法
		- concat方法： 数组的连接
		```
			var arr11 = [1,2,3];
			var arr12 = [4,5,6];
			document.write(arr11.concat(arr12));
		```
		- join()：根据指定的字符分割数组
		```
			var arr13 = new Array(3);
			arr13[0] = "a";
			arr13[1] = "b";
			arr13[2] = "c";

			document.write(arr13);
			document.write("<br/>");
			document.write(arr13.join("-"));
		```
		- push():向数组末尾添加元素，返回数组的新的长度
			* 如果添加的是一个数组，这个时候把数组当做一个整体字符串添加进去
		```
			 //push方法
			var arr14 = new Array(3);
			arr14[0] = "tom";
			arr14[1] = "lucy";
			arr14[2] = "jack";
			document.write("old array: "+arr14);

			document.write("<br/>");
			document.write("old length:"+arr14.length);

			document.write("<br/>");
			document.write("new length: "+arr14.push("zhangsan"));

			document.write("<br/>");
			document.write("new array: "+arr14);

			* 		var arr15 = ["aaa","bbb","ccc"];
			var arr16 = ["www","qqq"];

			document.write("old array:"+arr15);
			document.write("<br/>");
			document.write("old length:"+arr15.length);

			document.write("<br/>");
			document.write("new length:"+arr15.push(arr16));
			document.write("<br/>");
			document.write("new array: "+arr15);
			for(var i=0;i<arr15.length;i++) {
				alert(arr15[i]);
			}
		```
		- pop()：表示 删除最后一个元素，返回删除的那个元素
		```
			var arr17 = ["zhangsan","lisi","wangwu","zhaoliu"];
			document.write("old array: "+arr17);
			document.write("<br/>");

			document.write("return: "+arr17.pop());
			document.write("<br/>");
			document.write("new array: "+arr17);
		
		- reverse():颠倒数组中的元素的顺序
			* var arr17 = ["zhangsan","lisi","wangwu","zhaoliu"];
			document.write("old array: "+arr17);
			document.write("<br/>");

			document.write("return: "+arr17.pop());
			document.write("<br/>");
			document.write("new array: "+arr17);

			//reverse方法
			document.write("<hr/>");
			var arr18 = ["zhangsan1","lisi1","zhaoliu1","niuqi1"];
			document.write("old array: "+arr18);
			document.write("<br/>");
			document.write("new array:"+arr18.reverse());
		```

14. js的Date对象
	* 在java里面获取当前时间 
	```
		Date date = new Date();
		//格式化 
		//toLocaleString()  
	```
	* js里面获取当前时间
	```
		var date = new Date();
		//获取当前时间
		var date = new Date();
		document.write(date);  

		//转换成习惯的格式
		document.write("<hr/>");
		document.write(date.toLocaleString());
	```
	* 获取当前的年方法
		- `getFullYear()`：得到当前的年
		```
			 document.write("year: "+date.getFullYear());
		```
	* 获取当前的月方法
		- `getMonth()`：获取当前的月,返回的是 0-11月，如果想要得到准确的值，加1
		```
			var date1 = date.getMonth()+1;
			document.write("month: "+date1);
		```
	* 获取当前的星期
		- `getDay()`：星期,返回的是 (0 ~ 6)外国朋友，把星期日作为一周的第一天，星期日返回的是 0,而星期一到星期六 返回的是 1-6
		- `document.write("week: "+date.getDay());`

	* 获取当前的日
		- `getDate()`：得到当前的天 1-31
		- `document.write("day: "+date.getDate());`
	
	* 获取当前的小时
		- `getHours()`：获取小时
		- `document.write("hour: "+date.getHours());`
	
	* 获取当前的分钟
		- `getMinutes()`：分钟
		- `document.write("minute: "+date.getMinutes());`

	* 获取当前的秒
		- `getSeconds()`: 秒
		- `document.write("second: "+date.getSeconds());`
	
	* 获取毫秒数
		- ` getTime()`:返回的是1970 1 1 至今的毫秒数

		- 应用场景：
			- 使用毫秒数处理缓存的效果（不有缓存）
				`http://www.baidu.com?` 毫秒数
		
15. js的Math对象
	* 数学的运算
	* 里面的都是静态方法，使用可以直接使用 Math.方法()

	* ceil(x): 向上舍人

	* floor(x)：向下舍人

	* round(x)：四舍五入

	* random()：得到随机数（伪随机数）
		- 得到0-9的随机数
			- `Math.random()*10`
			- `Math.floor(Math.random()*10));`
	
16. js的全局函数
	* 由于不属于任何一个对象，直接写名称使用

	* `eval()` ： 执行js代码（如果字符串是一个js代码，使用方法直接执行）
	```
		var str = "alert('1234');";
		//alert(str);
		eval(str);
	```
	* `encodeURI()` ：对字符进行编码 
		- %E6%B5%8B%E8%AF%95%E4%B8%AD%E6%96%87aaa1234
	
	* `decodeURI()`  ：对字符进行解码

	   `encodeURIComponent()` 和 `decodeURIComponent()`
	 
	* `isNaN()`:判断当前字符串是否是数字
	```
		var str2 = "aaaa";
		alert(isNaN(str2));
	```
		- 如果是数字，返回false
		- 如果不是数字，返回true
	
	* `parseInt()`：类型转换
	```
		var str3 = "123";
		document.write(parseInt(str3)+1);
	```

17. js的bom对象
	* bom：broswer object model: 浏览器对象模型

	* 有哪些对象？
		- `navigator`： 获取客户机的信息（浏览器的信息）
			- `navigator.appName`
			- `document.write(navigator.appName);`

		- `screen`: 获取屏幕的信息
		```
			document.write(screen.width);
			document.write("<br/>");
			document.write(screen.height);
		```
		- `location`: 请求url地址
		- `href`属性
			- 获取到请求的url地址
			- `document.write(location.href);`

		- 设置url地址
			- 页面上安置一个按钮，按钮上绑定一个事件，当我点击这个按钮，页面可以跳转到另外一个页面
			- `location.href = "hello.html";`

		- `<input type="button" value="tiaozhuan" onclick="href1();"/>`
			- 鼠标点击事件  `onclick="js的方法;"`
		
	* `history`：请求的url的历史记录
		- 创建三个页面
			- 创建第一个页面 a.html 写一个超链接 到 b.html
			- 创建b.html 超链接 到 c.html
			- 创建c.html

		- 到访问的上一个页面
			- `history.back();`
			- `history.go(-1);`

		- 到访问的下一个页面
			- `history.forward();`
			- `history.go(1);`

	* `window`（重点）
		- 窗口对象
		- 顶层对象（所用的bom对象都是在window里面操作的）

		- 方法
			- `window.alert()` : 页面弹出一个框，显示内容
				- 简写`alert()`
			
			- `confirm()`： 确认框
				- `var flag = window.confirm("显示的内容");`
			
			- `prompt()`： 输入的对话框
				- `window.prompt("please input : ","0");`
				- `window.prompt("在显示的内容","输入框里面的默认值");`
			
			- `open()` :　打开一个新的窗口
				- `open("打开的新窗口的地址url","","窗口特征，比如窗口宽度和高度")` 
				- 创建一个按钮，点击这个按钮，打开一个新的窗口
				- `window.open("hello.html","","width=200,height=100");`
			
			- `close()`: 关闭窗口(浏览器兼容性比较差)
				- `window.close();`
			
			- 做定时器 
				- `setInterval("js代码",毫秒数)`  //1秒=1000毫秒
				- 表示每三秒，执行一次alert方法
				`window.setInterval("alert('123');",3000);`
				
			- `setTimeout("js代码",毫秒数)`
				- 表示在毫秒数之后执行，但是只会执行一次

				- 表示四秒之后执行js代码，只会执行一次
				`window.setTimeout("alert('abc');",4000);`
			
			- `clearInterval()`: 清除setInterval设置的定时器
			```
				var id1 = setInterval("alert('123');",3000);//通过setInterval会有一个返回值
				clearInterval(id1);
			```
			- `clearTimeout() `: 清除setTimeout设置的定时器
			```
				var id2 = setTimeout("alert('abc');",4000);
				clearTimeout(id2);
			```
18. js的dom对象（重点）
	* dom：document object model: 文档对象模型
	* 文档：超文本文档（超文本标记文档） html 、xml
	* 对象：提供了属性和方法
	* 模型：使用属性和方法操作超文本标记型文档
	* 可以使用js里面的dom里面提供的对象，使用这些对象的属性和方法，对标记型文档进行操作
	* 想要对标记型文档进行操作，首先需要 对标记型文档里面的所有内容封装成对象
		- 需要把html里面的标签、属性、文本内容都封装成对象
	
	* 要想对标记型文档进行操作，解析标记型文档
		- 画图分析，如何使用dom解析html

	* 解析过程
		- 根据html的层级结构，在内存中分配一个树形结构,需要把html中的每部分封装成对象，
			- document对象：整个文档
			- element对象：标签对象
			- 属性对象
			- 文本对象

		- Node节点对象：这个对象是这些对象的父对象
			- 如果在对象里面找不到想要的方法，这个时候到Node对象里面去找
	
	* DOM模型有三种：
		- DOM level 1：将html文档封装成对象。
		- DOM level 2：在level 1的基础上添加新的功能，例如：对于事件和css样式的支持。
		- DOM level 3：支持xml1.0的一些新特性。

	* DHTML：是很多技术的简称
		- html: 封装数据
		- css：使用属性和属性值设置样式
		- dom：操作html文档（标记型文档）
		- javascript：专门指的是js的语法语句（ECMAScript）
	
19. document对象
	* 表示整个的文档

	* 常用方法
		- `write()`方法：
			- 向页面输出变量（值）
			- 向页面输出html代码
			```
			var str = "abc";
			document.write(str);
			document.write("<hr/>");
			```
		- `getElementById()`;
			- 通过id得到元素（标签）
			```
			//使用getElementById得到input标签
			var input1 = document.getElementById("nameid");  //传递的参数是标签里面的id的值
			//得到input里面的value值
			alert(input1.name);   //标签对象.属性名称
			//向input里面设置一个值value
			input1.value = "bbbbb";
			```
		- `getElementsByName()`;
			- 通过标签的name的属性值得到标签
			- 返回的是一个集合（数组）
			```
			//使用getElementsByName得到input标签
			var inputs = document.getElementsByName("name1");  //传递的参数是 标签里面的name的值
			//alert(inputs.length);
			//遍历数组
			for(var i=0;i<inputs.length;i++) {   //通过遍历数组，得到每个标签里面的具体的值
				var input1 = inputs[i];  //每次循环得到input对象，赋值到input1里面
				alert(input1.value);    //得到每个input标签里面的value值
			}
			```
		- `getElementsByTagName("标签名称")`;
			- 通过标签名称得到元素
			```
			//演示getElementsByTagName
			var inputs1 = document.getElementsByTagName("input");  //传递的参数，是标签名称
			//alert(inputs1.length);
			//遍历数组，得到每个input标签
			for(var m=0;m<inputs1.length;m++) {
				//得到每个input标签
				var input1 = inputs1[m];
				//得到value值
				alert(input1.value);
			}
			```
		- 注意地方
			- 只有一个标签，这个标签只能使用name获取到，这个使用，使用`getElementsByName`返回的是一个数组，
			但是现在只有一个元素，这个时候不需要遍历，而是可以直接通过数组的下标获取到值
			```
			//通过name得到input标签
			var inputs2 = document.getElementsByName("name11")[0];
			alert(inputs2.value);

			var inputss = document.getElementsByTagName("input")[0];
			alert(inputss.value);
			```
