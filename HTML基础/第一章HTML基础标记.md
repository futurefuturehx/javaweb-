<body>标记的主要属性：
    bgcolor：设置页面的背景颜色 如：bgcolor="#CCFFCC"
    background:设置页面背景图片 如:background="images/bg.gif"
    bgproperties="fixed":使背景图片不随着滚动条的滚动而滚动
    text:设置文档正文的文字颜色 如：text="#FF6666"

分段标记:<p>段落文字</p>
换行标记:<br>
正文标题：<h1>1号正文标题文字</h1>
注释标记：<!-注释文字->
水平分割线标记:<hr>

文档头部信息：
<head>标记用于标记HTML文档头部信息 主要用于网络搜索引擎使用 而不会显示在网页正文中

<head>主要子标记（子元素）：
<title>设置窗口标题
<link>建立到外部文件（主要是CSS外部样式表）的链接
<stlye>设置网页的内部样式表
<meta>设置当前页面的元数据信息 下面是两个有用的属性：
    <meta name="author" content="sig">表示当前作者信息
    <meta http-equiv="Content-Type" content="text/html;charset=GBK">表示当前编码格式
    <meta http-equiv="refresh" content="5,url=http://www.baidu.com">定时刷新页面到指定网址
     
常用的文本格式:
<b>粗体</b>
<i>斜体</i>
<del>文字中部划线表示删除</del>
<ins>文字下划线表示填充内容</ins>
<sub>下标</sub>
<sup>上标</sup>比如次幂表示
<pre>预设置样式显示 保留空格和换行</pre> 按照原样显示不会自动删除制表符和空格等

文字：
<font>标记用于设置字体的类型 大小和颜色
<font>的几个属性：
    face设置字体类型:<font face="宋体">文字内容</font>
    size设置字体大小:<font size="2">文字内容</font>
    color设置字体颜色:<font color="#FF0000">文字内容</font>

图片：
<img>标记用于在HTML页面中插入图片
<img src="youyou.png">
重要属性:
    width/height:设置图片大小
    align:设置图片的水平和垂直对齐方式
    border:设置图片边框线条宽度

特殊字符显示:
例如:空格符 <> & "等
HTML中可以使用字符实体表示拉丁字符
空格符 &nbsp 
小于号 &lt
大于号 &gt
&符号 &amp
双引号 &quot
版权符号 &copy
注册商标 &reg
乘号 &times
除号 &divide

超链接:
HTML使用<a>标记来实现超链接
<a href="http://www.v512.com">v512工作室</a>
标记的重要属性：
    target:在指定的窗口或新窗口中显示链接页面
    <a href="http://www.v512.com/bbs" target=_blank>论坛</a>
    name:设置锚标记 实现超链接跳转到页面指定位置
    <a name="p1">文本内容</a>这是一个锚
    <a href="p1">跳转到(锚标记p1)指定位置</a>
    title:设置超链接的说明文字(当鼠标悬停在超链接上的时候显示)
    <a href="youyou.png" title="点击可以看到我的照片">悠悠</a>
    链接到email地址:<a href="mailto:360574435@qq.com">联系我们</a>
    图片作为超链接:<a href="..."><img src="youyou.png"></a>

列表：
有序列表：
<ol type="a"> <!--可选属性type用于设置列表符号--><!--type允许取值:"1","a","A","i","I"-->
    <li>列表条目1</li>
    <li>列表条目2</li>
</ol>
无序列表:
<ul type="disc">
    <li>列表条目1</li>
    <li>列表条目2</li>
</ul>
定义列表:
<dl>
    <dt>列表条目1标题</dt><dd>列表条目1正文</dd>
    <dt>列表条目2标题</dt><dd>列表条目2正文</dd>
</dl>

表格：
HTML表格相关标记:<title>,<br>,<td>,<th>,<caption>
表格相关标记的属性:
width/height:指定表格或某一个单元格的宽度/高度
border：指定边框线条的宽度
bordercolor:指定边框线条的颜色
background:指定表格或某一单元格的北京图片
align:设置单元格对齐方式
cellspacing:设置单元格间距
cellpadding:设置单元格内容与单元格边界之间的距离
colspan/rowspan:实现跨列/跨行单元格

表单：
HTML表单用于收集和提交用户输入的信息
基本语法格式:
<form action="http://www.v512.com/bbs/login.jsp method="post">
    用户名:<input type="text" name="username"><br>
    <input type="submit" value="提交">
    <input type="reset" value="重置">
</form>
表单的两种提交方式:method="get"和method="post"
post方式提交表单 不一次性传所有信息 但是相对保密
get方式提交表单  一次性将所有信息传过去 但是相对不保密
表单组件:
单行文本输入框:<input type="text" name="age" value="0">
密码输入框:<input type="password" name="pwd">
单选按钮:<input type="radio" name="gender" value="male"checked>男
        <input type="radio" name="gender" value="female">女
复选框:<input type="checkbox" name="fruit" value="apple">苹果<br>
      <input type="checkbox" name="fruit" value="yintao"checked>樱桃<br>
      <input type="checkbox" name="fruit" value="orange">橘子<br>
下拉列表框:<select name="fruit" size="3" multiple>
                <option value="apple">苹果
                <option value="grap">葡萄
                <option value="orange">橘子
          </select>
多行文本输入框：<textarea name="info" cols="40" rows="5">"请留言："</textarea>
提交按钮：<input type="submit" name="submit1" value="提交">
重置按钮:<input type="reset" value="重置">
图片提交按钮：<input type="image" src="done.gif" alt="提交" name="submit2">
隐藏文本框:<input type="hidden" name="role" value="guest">
文件组件：<form action ="k.jsp" enctype="multipart/form-data" method="post">
    <input type="file" name=" ">
    .....
</form>
name主要是用来给前台处理的

页面框架：
使用页面框架可以将一个浏览器窗口分割成多个窗格 以同时显示多个不同页面
行分割:
<html>
    <frameset rows="25%.*">
        <frame src="a.html">
        <frame src="b.html">
    </frameset>
</html>
列分割：
<html>
    <frameset cols="300,400.*" border="0">
        <frame name="myframe1" noresize src="a.html">
        <frame name="myframe2" src="b.html">
        <frame name="myframe3" src="c.html">
    </frameset>
</html>

嵌入标记：
<applet>标记用于在页面中嵌入Java Applet
<embed>标记用于在页面中嵌入多媒体文件 计算机上需要实现安装好相应的处理程序
<embed src="v512.avi"
            autostart="true"
            loop="true"
            hidden="false"
            controls="CONSOLE"
            width="200"
            height="45"
            >