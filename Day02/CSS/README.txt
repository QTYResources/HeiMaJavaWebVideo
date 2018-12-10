
day02

昨天内容回顾
	1、html的操作思想
		** 使用标签把要操作的数据包起来，通过修改标签的属性值来实现标签内数据样式的变化
		*** <font size="5"></font>
	
	2、图像标签
		<img src="图片的路径"/>
		** 通过html访问本地图片，使用绝对路径，目前有问题
	
	3、超链接标签
		<a href="" target="_blank"></a>

	4、表格标签
		** 技巧：数里面有多少行，每行里面有多少个单元格
		** <table></table>
			<tr>  <td>  <th>

	5、表单标签
		** <form></form>
			- action  method  enctype
			- method: get post

		** 输入项
			*** 有name属性
			* 普通输入项 type="text"
			* 密码： password
			* 单选：radio	
				- name值相同
				- value值
			* 复选框：checkbox
				- name值相同
				- value值
			
			* 下拉框 select option
			* 文本域 textarea
			* 隐藏项：type="hidden"
			* 文件： type="file"

			* 提交按钮 type="submit"
			* 重置 ： reset
			* 使用图片提交： <input type="image" src=""/>
			* 普通按钮 type="button"

	6、div和span
		* div: 自动换行
		* span：在一行显示


CSS

1、css的简介
	* css： 层叠样式表
		** 层叠：一层一层的

		** 样式表：
			很多的属性和属性值
	* 是页面显示效果更加好
	* CSS将网页内容和显示样式进行分离，提高了显示功能。

2、css和html的结合方式（四种结合方式）
	（1）在每个html标签上面都有一个属性 style，把css和html结合在一起
		- <div style="background-color:red;color:green;">

	（2）使用html的一个标签实现 <style>标签，写在head里面
		* <style type="text/css">
			css代码;
		</style>

		*   <style type="text/css">	
			div {
				background-color:blue;
				color: red;
			}		
		 </style>

	（3）在style标签里面 使用语句（在某些浏览器下不起作用）
		@import url(css文件的路径);

		- 第一步，创建一个css文件

		  <style type="text/css">
				@import url(div.css);
		  </style>

	（4）使用头标签 link，引入外部css文件
		- 第一步 ，创建一个css文件

		- <link rel="stylesheet" type="text/css" href="css文件的路径" />
	
	*** 第三种结合方式，缺点：在某些浏览器下不起作用，一般使用第四种方式

	*** 优先级（一般情况）
		由上到下，由外到内。优先级由低到高。
		*** 后加载的优先级高

	*** 格式  选择器名称 { 属性名：属性值；属性名：属性值；…….}

3、css的基本选择器（三种）
	** 要对哪个标签里面的数据进行操作
	
	（1）标签选择器
		* 使用标签名作为选择器的名称 
			div {
	
				background-color:gray;
				
				color:white;
			}

	（2）class选择器
		* 每个html标签都有一个属性 class 
		- <div class="haha">aaaaaaa</div>
		- .haha {
			background-color: orange;
		 }
	
	（3）id选择器
		* 每个html标签上面有一个属性 id
		- <div id="hehe">bbbbb</div>
		- #hehe {
			background-color: #333300;
		}
	*** 优先级
		style > id选择器 > class选择器 > 标签选择器

4、css的扩展选择器
	（1）关联选择器
		* <div><p>wwwwwwww</p></div>
		* 设置div标签里面p标签的样式，嵌套标签里面的样式
		* div p {	
			background-color: green;
		}
	
	（2）组合选择器
		* <div>1111</div>
		  <p>22222</p>
		* 把div和p标签设置成相同的样式，把不同的标签设置成相同的样式
		* div,p {
			background-color: orange;
		}
	
	（3）伪元素选择器(了解，浏览器的兼容性比较差)
		* css里面提供了一些定义好的样式，可以拿过来使用
		* 比如超链接 
			** 超链接的状态
			原始状态   鼠标放上去状态  点击           点击之后
			 :link         :hover        :active        :visited

			 ** 记忆的方法
				lv  ha

5、css的盒子模型
	** 在进行布局前需要把数据封装到一块一块的区域内（div）
	（1）边框
		border: 2px solid blue;
		border：统一设置
		上 border-top
		下 border-bottom
		左 border-left
		右 border-right

	（2）内边距
		padding:20px;
		使用padding统一设置
		也可以分别设置
		上下左右四个内边距

	（3）外边距
		margin: 20px;
		可以使用margin统一设置
		也可以分别设置
		上下左右四个外边距

6、css的布局的漂浮(了解)
	float： 
		** 属性值 
		left  :　 文本流向对象的右边 
		right  :　 文本流向对象的左边

7、css的布局的定位（了解）
	position：
		** 属性值
			- absolute ：
				 *** 将对象从文档流中拖出
				 *** 可以是top、bottom等属性进行定位
			- relative ：
				*** 不会把对象从文档流中拖出
				*** 可以使用top、bottom等属性进行定位

8、案例 图文混排案例
	** 图片和文字在一起显示

9、案例 图像签名
	** 在图片上面显示文字

10、上午内容总结
	1、css和html的四种结合方式（****）

	2、css的基本选择器（****）
		* 标签选择器 使用标签名
		* class选择器 .名称
		* id选择器  #名称

		** 优先级
			style > id > class > 标签
	
	3、css的扩展选择器(了解)
		* 关联选择器
			- 设置嵌套标签的样式  div p {}
		* 组合选择器
			- 不同的标签具有相同的样式 div,p{}
		* 伪元素选择器
			* 超链接的状态
				- 原始 :link
				- 悬停 :hover
				- 点击 :active
				- 点击之后 :visited

	4、盒子模型(了解)
		* 边框 border:2px solid red;
		上下左右  border-top  border-bottom  border-left  border-right

		* 内边距 padding:20px
		上下左右

		* 外边距 margin:20px
		上下左右
		
		* 对数据进行操作，需要把数据放到一个区域里面（div）
	
	5、布局的漂浮(了解)
		float
			- left: 后面的div到右边
			- right：后面的div到左边
	
	6、布局的定位(了解)
		position
			- absolute
				** 从文档流中拖出
			- relative
				** 不会从文档流中拖出

一般在目录里面，标出符号
	（********）：重点，代码看懂，代码会写，代码理解
		- （****重点中的重点***）
	（了解）：代码看懂
	（理解）：能够把原理讲清楚

