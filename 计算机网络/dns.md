# DNS解析过程

[![DNS](./Assets/Network/dns.png)](https://www.bilibili.com/video/BV1KK4y1i7gD?vd_source=f60330185adabf166359748da895c646)

DNS的基本工作就是把域名转IP。DNS和ARP一样有一个缓存，记录之前查过的域名。假如已经保存，就可以直接返回IP给客户端，没有的话就需要通过递归/迭代查询。以下例子是迭代查询：
	
1. 客户端给最近的DNS服务器发送查询请求
2. 最近的DNS服务器没有www.666.com的缓存记录，所以向根域DNS服务器发送查询
3. 根域也没有www.666.com的记录，但是识别了com域，会返回com域的DNS服务器的IP地址
4. 最近的DNS服务器给com域的DNS服务器发送查询，com域也没有www.666.com，但是识别了666.com，会返回666.com域的DNS服务器的IP地址
5. 最近的DNS服务器给666.com域的DNS服务器发送查询，得到了www.666.com的IP，然后返回给客户端
	
DNS中的域名都用“.”来分隔，越后面阶级越高：

## 根域（.）
其实我们的域名最后都有一个句点（www.666.com.），但是没人写，根域保管的是顶级域的DNS服务器信息

## 顶级域TLDs（com、cn、org）
分为国家顶级域名（ccTLDs）和通用顶级域名（gTLDs）。cn就属于前者，com和org属于后者

## 二级域名（666.com、xx.com）
通常由个人、组织、企业注册