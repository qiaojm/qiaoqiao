>##什么是Ajax？
>AJAX即“Asynchronous Javascript And XML”（异步JavaScript和XML）。它可以发送及接收各种格式的信息，
>包括JSON、XML、HTML和文本文件。AJAX最为吸引人的就是它的“异步”特性，这意味着AJAX可以无需刷新页面而
>与服务器端进行通信。允许你根据用户事件来更新部分页面内容。
<br/><br/>
>Ajax不是一种技术。实际上，它由几种蓬勃发展的技术以新的强大方式组合而成。Ajax包含：
>- 基于XHTML和CSS标准的表示；
>- 使用Document Object Model进行动态显示和交互；
>- 使用XMLHttpRequest与服务器进行异步通信；
>- 使用JavaScript绑定一切。
>##利用原生Ajax改变内容
>- 通过XMLHttpRequest实现使用JavaScript向服务器端发送一个HTTP请求（学会兼容个浏览器的写法）
>- 当接收到服务器端响应时，需要告诉HTTP请求对象使用JavaScript函数来处理响应。将XMLHttpRequest对象的onreadystatechange属性设置为该函数的名称，当请求的状态变化时，该函数会被调用。
>- 调用XMLHttpRequest对象的open()和send()方法向服务器端发送请求了,更多资源如下
>- http://mp.weixin.qq.com/s/l3mZudmc4NiCT13bJeURlQ
>- http://mp.weixin.qq.com/s/NUMEhgmWTVt_gdwoaRM2Aw
>- http://mp.weixin.qq.com/s/WZF4dJbqKwUHGOe4Pu7FoA
>- http://mp.weixin.qq.com/s/aKAsyDF9hq560DIXIcd2kg
>- http://www.w3school.com.cn/ajax/ajax_xmlhttprequest_onreadystatechange.asp
>###在实现上面内容时遇到一个跨域（cross origin）问题:
>(qq.html:25 XMLHttpRequest cannot load file:///C:/Users/iqiao.cc/ajax-practice/test.txt. Cross origin requests are only supported for >protocol schemes: http, data, chrome, chrome-extension, https, chrome-extension-resource.)<br/>
>解决方案：利用本地的node.js npm 安装http-server [详情](https://segmentfault.com/q/1010000003926981)
