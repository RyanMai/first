# first
HTML 与 CSS
HTML 5 与 XHTML
JavaScript 与浏览器脚本
Web Server 和 Web Services（服务器应用程序，Web Server 通常是C/C++/Java写的）、服务器脚本
PHP ，服务器脚本，Web Framework（服务器脚本框架）

一个普通网站访问的过程：
1.	用户操作浏览器访问，浏览器向服务器发出一个 HTTP 请求；
2.	服务器接收到 HTTP 请求，Web Server 进行相应的初步处理，使用服务器脚本生成页面；
3.	服务器脚本（利用Web Framework）调用本地和客户端传来的数据，生成页面；
4.	Web Server 将生成的页面作为 HTTP 响应的 body，根据不同的处理结果生成 HTTP header，发回给客户端；
5.	客户端（浏览器）接收到 HTTP 响应，通常第一个请求得到的 HTTP 响应的 body 里是 HTML 代码，于是对 HTML 代码开始解析；
6.	解析过程中遇到引用的服务器上的资源（额外的 CSS、JS代码，图片、音视频，附件等），再向 Web Server 发送请求，Web Server 找到对应的文件，发送回来；
7.	浏览器解析 HTML 包含的内容，用得到的 CSS 代码进行外观上的进一步渲染，JS 代码也可能会对外观进行一定的处理；
8.	用户与页面交互（点击，悬停等等）时，JS 代码对此作出一定的反应，添加特效与动画；
9.	交互的过程中可能需要向服务器索取或提交额外的数据（局部的刷新，类似微博的新消息通知），一般不是跳转就是通过 JS 代码（响应某个动作或者定时）向 Web Server 发送请求，Web Server 再用服务器脚本进行处理（生成资源or写入数据之类的），把资源返回给客户端，客户端用得到的资源来实现动态效果或其他改变。

几种常见的架构包括：
1.	LAMP = Linux + Apache + MySQL + PHP（P还可能是Python或Perl。有时候L会改成W=Windows。），也就是服务器上的操作系统是 Linux，Web Server 用 Apache，数据库用 MySQL，服务器脚本用 PHP，这些都是开源技术，网站起步时用起来的成本会比较低，所以是普通网站里非常常见的架构（虽然对于发展得很大的网站会遇到很多瓶颈），Facebook就是这种，淘宝也曾经是。
2.	J2EE，Java 世界的架构，通常是企业用的（银行、大型公司,.etc），比较常见地还会搭配一种 UNIX 做操作系统，Apache 做 Web Server，Tomcat 转换 JSP 到 Java 给服务器程序用（其实它也自带 Web Server），Oracle 数据库等等。不一定拿来建站，常常用来提供企业里的各种需要用到网络的业务。我们学校教务系统就是用J2EE做的=。= 淘宝现在也是从LAMP转型到了这个。
3.	ASP.NET，微软家的架构，通常会搭配 Windows Server 操作系统，SQL Server 数据库，IIS 做 Web Server。StackOverflow和京东（曾经）就是这个架构。
4.	神奇的MEAN架构，MongoDB做数据库，Express做 Web Framework，Angular 做前端的 JavaScript 框架，Node.js 用于编写 Web Server。神奇之处在于这几个东西的语言都是 JavaScript （MongoDB的实现不是，但与外界沟通用的语言是）。因为是比较新的架构，还有待时间的考验，不过被很多人（尤其是靠 JavaScript 吃饭的前端程序猿们）热切关注。
5.	一般来说重点不在技术而且在乎成本的新网站比较喜欢用 LAMP，重视安全稳定和速度的企业和机构喜欢 J2EE，想省事的网站喜欢 http://ASP.NET，比较 Geek 的网站和创业公司喜欢折腾各种 Python、Ruby、Node.js世界的东西，Google 这样现成的技术都解决不了需求的超大型网站就自己折腾解决方案。

