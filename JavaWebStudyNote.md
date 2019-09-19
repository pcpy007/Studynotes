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
	
		