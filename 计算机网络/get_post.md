# GET和POST的区别

![get_post](../Assets/Network/get_post.jpg)

GET和POST是HTTP协议中的两种发送请求方式。GET是从指定的资源请求数据，POST则是向指定的资源提交数据

GET把参数放在URL中，POST把参数放在request body

根据这点我们可以推出：

## 安全性
   POST比GET相对更安全，因为GET直接把参数暴露在URL中。（但是其实他们两个都不安全，因为HTTP是明文传输，HTTPS才是最安全的）

## 参数长度
   URL是有限制的长度的，因为GET把参数放在URL中，所以长度也有限制。POST放在request body，不受限制

## 数据包
   GET只会产生一个数据包，POST两个。因为对于GET浏览器会把header和data一起发送，然后等服务器响应200。POST会先发生header，等浏览器响应100（continue），才会再发送data，然后等服务器响应200

注：但是有些浏览器，像Firefox的POST只发送一次包

## 参数数据类型
   URL只允许ASCII字符，所以GET也是，POST没有限制

## 回退
   GET回退是无害的，POST会再次发送请求。所以我们有时候填表回退的时候会出现要不要重新提交
