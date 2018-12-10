
day03

上节内容回顾
	1、html的表单标签
		<form>:
			** action method enctype
		输入项：
			** type="text"
			** passwrod
			** radio
			** checkbox
			** file
			** submit
			** reset
			** type="image" src=""
			** select
			** textarea
			** type=“button”
			** hidden
	
	2、css	
		** css和html的结合方式（四种）
			（1）在标签里面style
			（2）使用标签<style>
			（3） 使用@import url()
			（4）link头标签实现

		** css的基本选择器（三种）
			（1）标签选择器
			（2）class选择器 .名称
			（3）id选择器  #名称
	
	3、javascript
		** java和javascript区别

		** js原始类型（五个）
			string number  boolean  null  undifined
			使用var
		** js的语句
			if switch while for do-while
		
		** js运算符
			* == 和 === 区别
		
		** js的数组
			** 创建方式（三种）
				var arr1 = [1,2,3,"4"];
				var arr2 = new Array(3);
				var arr3 = new Array(4,5,6);
			** 属性 length：长度
		
		** js的函数
			** 定义方式（三种）
				function add1(){}
				function(){}
		
		** js的全局变量和局部变量
			** 全局变量：在页面的任何js的部分都可以使用
			** 局部变量：在方法内部定义的变量，只是在方法内部使用
		
		** script标签应该放在什么位置 </body>

1、js的String对象
	** 创建String对象
		*** var str = "abc";
	
	** 方法和属性（文档）
		*** 属性 length：字符串的长度

		*** 方法
		（1）与html相关的方法
			- bold()：加粗
			- fontcolor(): 设置字符串的颜色
			- fontsize(): 设置字体的大小

			- link(): 将字符串显示成超链接
				**** str4.link("hello.html")
			
			- sub() sup(): 下标和上标

		（2）与java相似的方法
			- concat(): 连接字符串
				** //concat方法
				var str1 = "abc";
				var str2 = "dfg";
				document.write(str1.concat(str2));

			- charAt():返回指定指定位置的字符串
				** var str3 = "abcdefg";
				document.write(str3.charAt(20)); //字符位置不存在，返回空字符串
			
			- indexOf()： 返回字符串位置
				** var str4 = "poiuyt";
				document.write(str4.indexOf("w")); //字符不存在，返回-1
			
			- split()：切分字符串，成数组
				** var str5 = "a-b-c-d";
				var arr1 = str5.split("-");
				document.write("length: "+arr1.length);
			
			- replace() ： 替换字符串
				* 传递两个参数：
					-- 第一个参数是原始字符
					-- 要替换成的字符
				* var str6 = "abcd";
				document.write(str6);
				document.write("<br/>");
				document.write(str6.replace("a","Q"));
			
			- substr()和substring()
				* var str7 = "abcdefghuiop";
				//document.write(str7.substr(5,5));  //fghui  从第五位开始，向后截取五个字符
					*** 从第几位开始，向后截取几位

				document.write("<br/>");
				document.write(str7.substring(3,5)); //de  从第几位开始到第几位结束  [3,5)
					*** 从第几位开始，到第几位结束，但是不包含最后哪一位
			
2、js的Array对象
	** 创建数组（三种）
		- var arr1 = [1,2,3];
		- var arr2 = new Array(3); //长度是3
		- var arr3 = new Array(1,2,3); //数组中的元素是1 2 3

		- var arr = [];  //创建一个空数组
	
	** 属性：length：查看数组的长度

	** 方法
		- concat方法： 数组的连接
			* var arr11 = [1,2,3];
			var arr12 = [4,5,6];
			document.write(arr11.concat(arr12));

		- join()：根据指定的字符分割数组
			* var arr13 = new Array(3);
			arr13[0] = "a";
			arr13[1] = "b";
			arr13[2] = "c";

			document.write(arr13);
			document.write("<br/>");
			document.write(arr13.join("-"));
		
		- push():向数组末尾添加元素，返回数组的新的长度
			** 如果添加的是一个数组，这个时候把数组当做一个整体字符串添加进去

			* //push方法
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
		
		- pop()：表示 删除最后一个元素，返回删除的那个元素
			* var arr17 = ["zhangsan","lisi","wangwu","zhaoliu"];
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


3、js的Date对象
	** 在java里面获取当前时间 
		Date date = new Date();
		//格式化 
		//toLocaleString()   //2015年4月17日 11:17:12
	
	** js里面获取当前时间
		var date = new Date();
		//获取当前时间
		var date = new Date();
		document.write(date);  // Fri Apr 17 10:47:46 UTC+0800 2015 

		//转换成习惯的格式
		document.write("<hr/>");
		document.write(date.toLocaleString());
	
	** 获取当前的年方法
		getFullYear()：得到当前的年
			**** document.write("year: "+date.getFullYear());
	
	** 获取当前的月方法
		getMonth()：获取当前的月
			*** 返回的是 0-11月，如果想要得到准确的值，加1
			**** var date1 = date.getMonth()+1;
			document.write("month: "+date1);
	
	** 获取当前的星期
		getDay()：星期,返回的是 (0 ~ 6)
		** 外国朋友，把星期日作为一周的第一天，星期日返回的是 0
		   而星期一到星期六 返回的是 1-6
		** document.write("week: "+date.getDay());

	** 获取当前的日
		getDate()：得到当前的天 1-31
		** document.write("day: "+date.getDate());
	
	** 获取当前的小时
		getHours()：获取小时
		** document.write("hour: "+date.getHours());
	
	** 获取当前的分钟
		getMinutes()：分钟
		** document.write("minute: "+date.getMinutes());

	** 获取当前的秒
		getSeconds(): 秒
		** document.write("second: "+date.getSeconds());
	
	** 获取毫秒数
		getTime()
		返回的是1970 1 1 至今的毫秒数

		** 应用场景：
			*** 使用毫秒数处理缓存的效果（不有缓存）
				http://www.baidu.com?毫秒数
		
4、js的Math对象
	* 数学的运算
	** 里面的都是静态方法，使用可以直接使用 Math.方法()

	** ceil(x): 向上舍人

	** floor(x)：向下舍人

	** round(x)：四舍五入

	** random()：得到随机数（伪随机数）
		- 得到0-9的随机数
			Math.random()*10
			Math.floor(Math.random()*10));
	
5、js的全局函数
	* 由于不属于任何一个对象，直接写名称使用

	** eval() ： 执行js代码（如果字符串是一个js代码，使用方法直接执行）
		**** var str = "alert('1234');";
		//alert(str);
		eval(str);

	** encodeURI() ：对字符进行编码 
		- %E6%B5%8B%E8%AF%95%E4%B8%AD%E6%96%87aaa1234
	
	   decodeURI()  ：对字符进行解码

	   encodeURIComponent() 和 decodeURIComponent()
	 
	** isNaN():判断当前字符串是否是数字
		-- var str2 = "aaaa";
		alert(isNaN(str2));
		*** 如果是数字，返回false
		*** 如果不是数字，返回true
	
	** parseInt()：类型转换
		** var str3 = "123";
		document.write(parseInt(str3)+1);
	
6、js的函数的重载
	** 什么是重载？方法名相同，参数不同

	** js的重载是否存在？ 不存在
		** 调用最后一个方法
		** 把传递的参数保存到 arguments数组里面

	** js里面是否存在重载？(面试题目)
		（1）js里面不存在重载。
		（2）但是可以通过其他方式模拟重载的效果 （通过aruguments数组来实现）

		*** function add1() {
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

7、js的bom对象
	** bom：broswer object model: 浏览器对象模型

	** 有哪些对象？
	*** navigator： 获取客户机的信息（浏览器的信息）
		- navigator.appName
		- document.write(navigator.appName);

	*** screen: 获取屏幕的信息
		- document.write(screen.width);
		document.write("<br/>");
		document.write(screen.height);

	*** location: 请求url地址
		- href属性
		**** 获取到请求的url地址
			- document.write(location.href);

		**** 设置url地址
			- 页面上安置一个按钮，按钮上绑定一个事件，当我点击这个按钮，页面可以跳转到另外一个页面
			- location.href = "hello.html";

		**** <input type="button" value="tiaozhuan" onclick="href1();"/>
			- 鼠标点击事件  onclick="js的方法;"
		
	*** history：请求的url的历史记录
		- 创建三个页面
			1、创建第一个页面 a.html 写一个超链接 到 b.html
			2、创建b.html 超链接 到 c.html
			3、创建c.html

		- 到访问的上一个页面
			history.back();
			history.go(-1);

		- 到访问的下一个页面
			history.forward();
			history.go(1);

	**** window（****）
		* 窗口对象
		* 顶层对象（所用的bom对象都是在window里面操作的）

		** 方法
			- window.alert() : 页面弹出一个框，显示内容
				** 简写alert()
			
			- confirm()： 确认框
				- var flag = window.confirm("显示的内容");
			
			- prompt()： 输入的对话框
				- window.prompt("please input : ","0");
				- window.prompt("在显示的内容","输入框里面的默认值");
			
			- open() :　打开一个新的窗口
				** open("打开的新窗口的地址url","","窗口特征，比如窗口宽度和高度") 
				- 创建一个按钮，点击这个按钮，打开一个新的窗口
				- window.open("hello.html","","width=200,height=100");
			
			- close(): 关闭窗口(浏览器兼容性比较差)
				- window.close();
			
			- 做定时器 
			** setInterval("js代码",毫秒数)  1秒=1000毫秒
				- 表示每三秒，执行一次alert方法
				window.setInterval("alert('123');",3000);
				
			** setTimeout("js代码",毫秒数)
				- 表示在毫秒数之后执行，但是只会执行一次

				- 表示四秒之后执行js代码，只会执行一次
				window.setTimeout("alert('abc');",4000);
			
			** clearInterval(): 清除setInterval设置的定时器
				var id1 = setInterval("alert('123');",3000);//通过setInterval会有一个返回值
				clearInterval(id1);

			** clearTimeout() : 清除setTimeout设置的定时器
				var id2 = setTimeout("alert('abc');",4000);
				clearTimeout(id2);

8、js的dom对象（****）
	* dom：document object model: 文档对象模型
	** 文档：
		超文本文档（超文本标记文档） html 、xml
	** 对象：
		提供了属性和方法
	** 模型：使用属性和方法操作超文本标记型文档

	*** 可以使用js里面的dom里面提供的对象，使用这些对象的属性和方法，对标记型文档进行操作

	*** 想要对标记型文档进行操作，首先需要 对标记型文档里面的所有内容封装成对象
		-- 需要把html里面的标签、属性、文本内容都封装成对象
	
	*** 要想对标记型文档进行操作，解析标记型文档
		- 画图分析，如何使用dom解析html

	*** 解析过程
		根据html的层级结构，在内存中分配一个树形结构，需要把html中的每部分封装成对象，
		- document对象：整个文档
		- element对象：标签对象
		- 属性对象
		- 文本对象

		-- Node节点对象：这个对象是这些对象的父对象
			*** 如果在对象里面找不到想要的方法，这个时候到Node对象里面去找
	
	DOM模型有三种：
		DOM level 1：将html文档封装成对象。
		DOM level 2：在level 1的基础上添加新的功能，例如：对于事件和css样式的支持。
		DOM level 3：支持xml1.0的一些新特性。

	* DHTML：是很多技术的简称
		** html: 封装数据
		** css：使用属性和属性值设置样式
		** dom：操作html文档（标记型文档）
		** javascript：专门指的是js的语法语句（ECMAScript）
	
9、document对象
	* 表示整个的文档

	** 常用方法
		**** write()方法：
			（1）向页面输出变量（值）
			（2）向页面输出html代码
			- var str = "abc";
			document.write(str);
			document.write("<hr/>");
		
		**** getElementById();
			- 通过id得到元素（标签）
			- //使用getElementById得到input标签
			var input1 = document.getElementById("nameid");  //传递的参数是标签里面的id的值
			//得到input里面的value值
			alert(input1.name);   //标签对象.属性名称
			//向input里面设置一个值value
			input1.value = "bbbbb";
		
		**** getElementsByName();
			- 通过标签的name的属性值得到标签
			- 返回的是一个集合（数组）
			- //使用getElementsByName得到input标签
			var inputs = document.getElementsByName("name1");  //传递的参数是 标签里面的name的值
			//alert(inputs.length);
			//遍历数组
			for(var i=0;i<inputs.length;i++) {   //通过遍历数组，得到每个标签里面的具体的值
				var input1 = inputs[i];  //每次循环得到input对象，赋值到input1里面
				alert(input1.value);    //得到每个input标签里面的value值
			}
		
		**** getElementsByTagName("标签名称");
			- 通过标签名称得到元素
			- //演示getElementsByTagName
			var inputs1 = document.getElementsByTagName("input");  //传递的参数，是标签名称
			//alert(inputs1.length);
			//遍历数组，得到每个input标签
			for(var m=0;m<inputs1.length;m++) {
				//得到每个input标签
				var input1 = inputs1[m];
				//得到value值
				alert(input1.value);
			}

		**** 注意地方
			**** 只有一个标签，这个标签只能使用name获取到，这个使用，使用getElementsByName返回的是一个数组，
			但是现在只有一个元素，这个时候不需要遍历，而是可以直接通过数组的下标获取到值
			//通过name得到input标签
			var inputs2 = document.getElementsByName("name11")[0];
			alert(inputs2.value);

			var inputss = document.getElementsByTagName("input")[0];
			alert(inputss.value);

10、案例：window弹窗案例
	- 实现过程
		1、创建一个页面
			** 有两个输入项和一个按钮
			** 按钮上面有一个事件：弹出一个新窗口 open

		2、创建弹出页面
			** 表格
			** 每一行有一个按钮和编号和姓名
			** 按钮上有一个事件：把当前的编号和姓名，赋值到第一个页面相应的位置

			****//实现s1方法
			function s1(num1,name1) {
				//需要把num1和name1赋值到window页面
				//跨页面的操作  opener：得到创建这个窗口的窗口 得到window页面
				var pwin = window.opener; //得到window页面
				pwin.document.getElementById("numid").value = num1;
				pwin.document.getElementById("nameid").value = name1;
				//关闭窗口
				window.close();
			}

			－　opener:属性，获取创建当前窗口的窗口

	- 做这个案例时候会有一个问题
		*** 由于我们现在访问的是本地文件，js安全性，谷歌浏览器安全级别很高，不允许访问本地文件
		*** 在实际开发中，没有这样的问题，实际中不可能访问本地的文件。
		*** http://www.baidu.com

