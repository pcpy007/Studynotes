JavaWeb Study Note

1.1	B/S 结构

	C/S :客户机/服务器
		eg：QQ
		软件更新，所有客户端都要更新
	B/S：浏览器/服务器 Browser/Server
		eg：京东网上商城
		服务器端的更新对用户无影响，用户直接访问浏览器即可
		
	常见的应用于Web的编程语言：
		1)	CGI：Common Gateway Interface 公共网关接口
		2)	PHP：Hypertext Preprocessor
		3)	JSP：Java Sever Pages
		4)	ASP：Active Server Page动态服务器页面
	Tomcat目录解释：
		bin:可执行文件（startup.bat shutdown.bat )
		conf:配置文件（sever.xml)
		lib:tomcat依赖的jar文件
		log:日志文件(记录出错等信息)
		temp:临时文件
		webapps:可执行的项目，将我们开发的项目放入该目录
		work:存放由jsp翻译成的java,以及编辑成的class(js)
	Tomcat默认端口号8080.此端口号较为常见，建议修改]
	状态码：
		404：资源不存在
		403：权限不足
		200：一切正常
		300/301：页面重定向（跳转）
		500：服务器内部有误（代码写错）
	做好的项目放到webapps文件夹里
		WEB_IF:
				web.xml--在此设置默认的初始访问页面
						<welcome-file-list>
							<welcome-file>index.jsp</welcome-file>
							<welcome-file>index2.jsp</welcome-file>
						</welcome-file-list>
				classes--java编译后生成的class文件
				lib--三方依赖库-jar包
		.jsp
		
	<%
		添加java代码/Java脚本
	%>
	
	
2 HTML基础

	HTML：Hypertext Mark-up Language.超文本标记语言
	
	标签有两种类型：
			单标签:<br>
			双标签:<b>text</b>
				标签围绕的内容就是标签的作用域
			标签具有属性
	HTML基本结构：
		<html>
			<head>
				设置网页相关属性，比如标题
			</head>
			<body>
				浏览器网页中显示的内容
			</body>
		</html>
	<!--内容-->表示注释
	
	HTML中的常见标签：
		1)文字和字体标签：
			标题:<hn>内容</hn><!--n是一个常数,从1到6，n越小字号越大-->
				<h1>一级标题</h1>
				<h2>二级标题</h2>
			换行:<br>
			段落:<p>
				常用属性:align
					<p align="left">:左对齐
							 "center":居中对齐
							 "right":右对齐
			水平线:<hr>
				常用属性:
					size:宽度,单位像素
					width:长,单位像素（默认），或者百分比
					align:对齐方式
					noshade:线段无阴影属性，没有属性值，若设置则为实心线段
					color:线段内部颜色
		2)文字设计标签
			<font></font>用于标记字体
				常用属性：
					size：字体大小
					face：字体类型，默认为宋体
					color：字体颜色
			文字风格标签：
				粗体：<b></b>
				下划线:<u></u>
				斜体：<i></i>
				上标:<sup></sup>
				下标:<sub></sub>
				闪烁:<blink></blink>
		3)列表标签
			两种，有序和无序
				无序：<ul></ul>
				有序：<ol></ol>
			列表中项使用<li></li>表示
		4)表格标签
			定义表格：<table></table>
			定义标题：<caption></caption>
			定义表行：<tr></tr>
			定义表头：<th></th>
			定义表元；<td></td>
			
			表格标签的公共属性:
				align:水平布局方式,left/right/center
				bgcolor:背景颜色
				border:边框宽度,默认为0 没有边框
				width:宽度,单位：像素/百分制
				height:高度,单位:像素/百分制
			表元的背景颜色、对齐方式等属性与它离得最近的相同
			<table>标签的常用属性:
				bordercolor:表格边框的颜色，默认为黑色
				cellpadding:表元边框的宽度
				cellspacing:表元的边框与表格边框之间的宽度
			合并单元格:
				对<td>标签的rowspan、colspan属性进行设置
					rowspan:从该表元起该表元在行上占有的单元格数(结果体现为一列合并)
					colspan:从该表元起该表元在列上占有的单元格数(结果体现为一行合并)
		
			HTML中的颜色：
				1，常用名称表示：
						"red"表示红色
				2，使用"#RRGGBB"表示:
						每个分量取值为00~FF
						#FF0000表示红色
		5)链接和图片标签
			链接标签:<a>内容</a>
				重要属性:href,值表示链接所指向的资源地址
			图片标签:<img src="图片文件路径">
				重要属性:
					src:图片存储的位置
					width、height、border、align
					alt:图片载入失败时的文字说明
	表单标签：
		文本框、密码框
		表单组成：
			<form action="提交地址">
				表单内容(包括按钮、输入框、选择框等0
			<form>
		表单input标签，其type属性决定表单元素类型
			text:文本框
			password:密码框
			radio:单选按钮
			checkbox:复选框
			reset:重置按钮
			button:普通提交按钮
			submit:提交按钮
			image:图片,单击提交表单
			多行文本框：<textarea></textarea> 使用rows属性表示其行数,用cols属性表示其列数
			下拉菜单:其中的选项使用<option>选项内容</option>表示
						multiple属性能将其设置为可多选
						size属性的值为下拉菜单显示的项目数
						selected为默认选项
	框架:将几个页面作为一个页面的几个部分显示，每个窗口都是完整的HTML网页
		写法：
			<frameset cols = "30%,70%">
				<frame src = "left.html" noresixe scrolling = "no" name = "left"></frame>
				<frame src = "right.html" noresixe scrolling = "no" name = "left"></frame>
			</frameset>
		cols属性决定是横向分隔还是纵向分隔
