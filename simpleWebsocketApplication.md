# 构建一个简单的Websocket应用

## 什么是Websocket

传统的HTTP协议的工作方式是“请求-响应”的形式，请求只能由客户端发起，由服务端响应。在复杂场景中，如果要实现服务端发送信息`->`客户端接受信息的功能，最简单的方法是采用“轮询”，即客户端定时向服务端请求数据，从而“比较及时”得到最新的信息。这样一来会带来实时性和资源友好之间的权衡（过于频繁的连接导致大量无用流量的出现）。

![img](image/Connect Comparison.png)

Websocket用于解决上述问题，它在2008年诞生，2011年成为国际标准。所有浏览器都已经支持了<sup>[1]</sup>。Websocket建立在TCP协议上，与HTTP有良好的兼容性（使用端口相同），实质上是复用了HTTP的握手通道，客户端可以通过HTTP协议与服务端协商，以将协议从HTTP升级到Websocket<sup>[2]</sup>。更详细的Websocket协议和具体的数据帧定义见[WebSocket协议：5分钟从入门到精通](https://www.cnblogs.com/chyingp/p/websocket-deep-in.html)。

PS: Websocket 没有同源限制（CROS， Cross-Origin Resource Sharing），在初次尝试的时候可以少踩一个坑。

## 技术选型

服务端选择可以快速构建原型（调包<sup>[3]</sup>）的Python，客户端分别用Python和JavaScript构建。

Python版客户端侧重于对python中Websocket技术实现内部的探索，JavaScript版客户端侧重于构建Web页面与后端的交互过程。

## 基于Python的Websocket库初步了解





## 参考文献

[1] [WebSocket 教程. 阮一峰的网络日志](http://www.ruanyifeng.com/blog/2017/05/websocket.html)

[2] [WebSocket协议：5分钟从入门到精通](https://www.cnblogs.com/chyingp/p/websocket-deep-in.html)

[3] [Websocket官方文档](https://websockets.readthedocs.io/en/stable/)