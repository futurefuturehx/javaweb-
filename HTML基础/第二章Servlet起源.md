Internet:网络的网络

TCP/IP的四层结构:
Network Interface层
Internet层
Transport层
Application层

Application层常用协议:
HTTP Telnet FTP SMTP POP3

WWW：World Wibe Web 描述的是一个资料空间

URL：
例如:http://www.v512.com/bbs/index.htm
http:// 代表超文本传输协议 通常这部分可以省略 
www 代表这是一个www服务
v512.com 这是保存网页的服务器的域名 也可以是IP地址或Web服务器的名称
/bbs Web服务器上的子目录名称
/index.htm index.htm是一个HTML网页的名称

超文本标记语言(HTML)
作用是定义超文本文档的结构和格式
HTML告诉浏览器如何把内容显示给用户看到

HTTP协议:
HTTP是用于从Web服务器传输HTML文件到本地浏览器的通信协议
该协议是基于请求/响应形式的结构(相当于客户机/服务器结构)
HTTP协议是无状态的协议

Web服务器(Server端):
用来专门提供WWW服务的服务器软件就叫Web服务器
常用的Web服务器:
Apache
IIS
Tomcat
常用的应用服务器:
Tomcat
Resin
WebLogic Server
WebSphere
JBoss

浏览器(Client端)
浏览器和Web服务器之间是一个C/S的结构
Internet Explorer 
Firefox 
Opera

Web动态编程技术
Servlet：CGI的Java版本技术Servlet(Sun公司推出)

编写Java Socket程序的几种结构:
1.直接使用Socket编程实现
2.使用Socket 再结合Java的多线程编程
3.使用NIO中的非阻塞 Socket再结合Java的多线程编程
4.使用JDK自带的或者第三方的线程池技术对线程进行管理 提高多线程
5.使用开源的Java Socket开发框架

