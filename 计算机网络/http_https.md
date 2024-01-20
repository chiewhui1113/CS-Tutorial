# HTTP和HTTPS的区别

[![http_https](./Assets/Network/http_https.png)](https://www.bilibili.com/video/BV1Pg4y1S7cx?vd_source=f60330185adabf166359748da895c646)

HTTP（超文本传输协议）是浏览器和服务器沟通的一种方法。不过由于HTTP不提供数据加密，黑客可以很容易读取/篡改这些信息。为了解决这个安全问题，引入了HTTPS（超文本传输安全协议），多出的S是secure安全的意思。HTTPS在HTTP的基础上加上了SSL/TLS加密层。在有涉及到支付网站都会使用HTTPS，以避免任何信息被盗。
<br>
以下是HTTP和HTTPS的主要区别：
	
## 加密层
HTTP没有加密层，HTTPS用SSL/TLS加密
	
## 速度
HTTP响应速度快，HTTPS比较慢
因为HTTP省略掉了加密的过程
	
## 安全性
HTTP不安全，HTTPS安全
	
## 端口
HTTP是端口80，HTTPS是端口443
	
## 证书
HTTP不需要证书，HTTPS需要SSL/TLS证书
	
## 搜索引擎优化SEO
HTTP排名比较低，HTTPS排名比较高 <br>
Google的SEO会倾向于HTTPS的网站，因为更安全