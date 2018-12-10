
1、javascript的简介
	* 是基于对象和事件驱动的语言，应用与客户端。
		- 基于对象：
			** 提供好了很多对象，可以直接拿过来使用
		- 事件驱动：
			** html做网站静态效果，javascript动态效果
		
		- 客户端：专门指的是浏览器

	* js的特点
		（1）交互性
			- 信息的动态交互

		（2）安全性
			- js不能访问本地磁盘的文件

		（3）跨平台性
			- java里面跨平台性，虚拟机
			- 只有能够支持js的浏览器，都可以运行
	
	* javascript和java的区别（雷锋和雷峰塔）
		（1）java是sun公司，现在oracle；js是网景公司
		（2）JavaScript 是基于对象的，java是面向对象
		（3）java是强类型的语言，js是弱类型的语言
			- 比如java里面 int i = "10";
			- js:  var i = 10; var m = "10";
		（4）JavaScript只需解析就可以执行，而java需要先编译成字节码文件，再执行。
	
	* javascript的组成（下面js）
		三部分组成
		（1）ECMAScript
			- ECMA : 欧洲计算机协会
			- 有ECMA组织制定的js的语法，语句.....

		（2）BOM
			- broswer object model: 浏览器对象模型

		（3）DOM
			- document object model：文档对象模型

2、js和html的结合方式（两种）
	第一种：
		- 使用一个标签 <script type="text/javascript">  js代码; </script>
	
	第二种：
		- 使用script标签，引入一个外部的js文件
		*** 创建一个js文件，写js代码
		- 	<script type="text/javascript" src="1.js"></script>
	
	** 使用第二种方式时候，就不要在script标签里面写js代码了，不会执行。

3、js的原始类型和声明变量
	** java的基本数据类型 byte short int long float double char boolean

	** 定义变量 都使用关键字 var

	** js的原始类型（五个）		
		- string: 字符串
			*** var str = "abc";

		- number：数字类型
			*** var m = 123;

		- boolean：true和false
			*** var flag = true;

		- null
			*** var date = new Date();
			*** 获取对象的引用，null表示对象引用为空 ，所有对象的引用也是object				
		- undifined
			*** 定义一个变量，没有赋值
			*** var aa;
	** typeof(); 查看当前变量的数据类型

4、js的语句
	- java里面的语句： 
		** if判断
		** switch语句
		** 循环 for  while do-while
	
	-js里面的这些语句
		** if判断语句
			**** =:表示赋值
			**** ==：表示判断

		** switch语句
			- java里面支持数据类型 string支持吗？在jdk1.7开始支持
			- js里面都支持
			- switch(a) {
				case 5:
					break;
				case 6:
					break;
				default:
				......
			 }
		** 循环语句 for  while    do-while
			- while循环
			**** var i = 5;
			while(i>1) {
				alert(i);
				i--;
			}

			- for循环
			*** for(int i=0;i<=10;i++) { }
			for(var mm=0;mm<=3;mm++) {
				alert(mm);
			}

		** i++ ++i和java里面一样

5、js的运算符
	** +=  ： x+=y;  ===> x=x+y;

	** js里面不区分整数和小数
		var j = 123;
		alert(j/1000*1000);  
		//  j/1000*1000    在java里面得到结果是 0 
		// 在js里面不区分整数和小数，123/1000=0.123 * 1000 = 123

	** 字符串的相加和相减的操作
		var str = "123";

		** 如果相加时候，做是字符串连接
		** 如果相减，做的是相减的运算

		* //字符串的操作
		var str = "456";
		//alert(str+1);   //在java里面操作的结果是 4561 ，在js里面还是 4561
		alert(str-1);    //相减时候，执行减法的运算

		* 提示NaN:表示不是一个数字

	** boolean类型也可以操作
		*** 如果设置成true，相当于这个值是1
		*** 如果设置成false，相当于这个值是0
	
	** == 和 === 区别
		** 做判断

		** == 比较的只是值
		** === 比较的是值和类型
	
	** 引入知识
		直接向页面输出的语句（可以把内容显示在页面上）
		* document.write("aaa");
		document.wirte("<hr/>");
		** 可以向页面输出变量，固定值和html代码

6、实现99乘法表（输出到页面上）
	*	document.write("<table border='1' bordercolor='blue'>");
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

	- document.write里面是双引号，如果设置标签的属性需要使用单引号
	- document.write可以输出变量，还可以输出html代码

7、js的数组
	* 什么是数组？
		- 使用变量，var m = 10;
		- java里面的数组 定义 int[] arr = {1,2,3};

	* 定义方式（三种）
		第一种： var arr = [1,2,3];   var arr = [1,"4",true];
		第二种：使用内置对象 Array对象
			var arr1 = new Array(5);  //定义一个数组，数组的长度是5
			arr1[0] = "1";

		第三种：使用内置对象 Array
			var arr2 = new Array(3,4,5); //定义一个数组，数组里面的元素是3 4 5 
	
	* 数组里面有一个属性  length：获取到数组的长度

	* 数组可以存放不同的数据类型的数据

8、js的函数
	** 在java里面定义方法
		public 返回类型void /int   方法名(参数列表) {
			方法体;
			返回值;
		}

		public int add(int a,int b) {
			int sum = a+b;
			return sum;
		}

	** 在js里面定义函数（方法）有三种方式
		**** 函数的参数列表里面，不需要写var，直接写参数名称
		第一种方式：
			**** 使用到一个关键字 function
			**** function 方法名(参数列表) {
				方法体;
				返回值可有可无（根据实际需要）;
			 }

			**** 代码
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
		
		第二种方式：
			**** 匿名函数
				var add = function(参数列表) {
					方法体和返回值;
				}
			**** 代码
			//第二种方式创建函数
			var add3 = function(m,n) {
				alert(m+n);
			}

			//调用方法
			add3(5,6);
		
		第三种方式：（用的少，了解）
			*** 动态函数
			*** 使用到js里面的一个内置对象 Function
				var add = new Function("参数列表","方法体和返回值");

9、js的全局变量和局部变量
	** 全局变量：在script标签里面定义一个变量，这个变量在页面中js部分都可以使用
		- 在方法外部使用，在方法内部使用，在另外一个script标签使用

	** 局部变量：在方法内部定义一个变量，只能在方法内部使用
		- 如果在方法的外部调用这个变量，提示出错
		- SCRIPT5009: “nn”未定义 
		12-js的局部变量.html, 行18 字符3
	
	** ie自带了一个调试工具，ie8及其以上的版本中，键盘上 F12，在页面下方出现一个条

10、script标签放在的位置
	* 建议把script标签放到 </body>后面
	* 如果现在有这样一个需求：
		在js里面需要获取到input里面的值，如果把script标签放到head里面
		会出现问题。
		html解析是从上到下解析的，script标签放到的是head里面，直接在里面取input里面的值，
		因为页面还没有解析到input那一行，肯定取不到。

11、js的重载
	* 什么是重载？方法名相同，参数列表不同
		- java里面有重载，肯定有

	* js里面是否有重载？

12、今天的内容的总结
	* css
		** css和html的四种结合方式(*******)
			
		** css的基本选择器(********)
			* 标签选择器 div {css代码}
			* class选择器 .名称 {}
			* id选择器   #名称{}
		
		** css的扩展选择器(了解)
			* 关联选择器
				*** 嵌套标签的样式的设置
			* 组合选择器
				*** 不同标签设置相同的样式
			* 伪元素选择器
				** a标签的状态
					lv ha
		** 盒子模型(了解)
			* 边框 border
				上下左右
			* 内边距 padding
				上下左右
			* 外边距 margin
				上下左右
		
		** 漂浮(了解)
			float : left right
		
		** 定位(了解)
			position：absolute  relative
	
	* javascript(*******)
		** 什么是javascript
			- 基于对象和事件驱动的语言，应用与客户端。
			- 特点：
				交互性  安全性  跨平台性

			- javascript和java区别

			- 组成（3部分）
				* ECMAScript
				* bom
				* dom

		** js和html的结合方式（两种）
			第一种 <script type="text/javascript"> js代码; </script>
			第二种 <script type="text/javascript" src="js的路径"> </script>
		
		** js的数据类型
			* 五种原始类型
				string  number boolean null undifined
			* 定义变量使用  var
		
		** js的语句
			* if
			* switch
			* for while do-while
		
		** js的运算符
			* 字符串的操作
				*** 字符串相加：连接
				*** 字符串相减：执行相减运算
			* boolean类型相加
				true： 1
				false：0
			* == 和 === 区别
				** == ： 判断值
				** === ： 判断值和类型
		
		** js的数组
			三种定义方式
			** var arr = [1,2,"3"];
			** var arr1 = new Array(9); //长度9
			** var arr2 = new Array(1,2,3); //元素是 1 2 3

			** 属性 length：数组的长度
		
		** js的函数
			*** function add(a,b) {方法体和返回值;}
			*** var add1 = function(m,n) {方法体和返回值;}
			*** var add2 = new Function("a,b","方法体和返回值");

			**** 不要忘记调用，不然不起作用的
		
		** js的全局变量和局部变量
			** 全局变量：在页面中任何js的部分，都可以使用
			** 局部变量：在方法内部定义一个变量，这个 变量只能在方法内部使用
		
		** script标签位置
			** 建议放在</body>后面
		
		** js的重载（回去思考这个问题）
