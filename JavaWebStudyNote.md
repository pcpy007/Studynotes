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
		文字和字体标签：
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
