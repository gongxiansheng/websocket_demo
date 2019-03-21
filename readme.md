# web 服务的推送总结

=====================================

## 短轮询

+ 缺点
  > 轮询的间隔过长，会导致用户不能及时接收到更新的数据；轮询的间隔过短，会导致查询请求过多，增加服务器端的负担

## 长轮询

+ 缺点
  > 保持连接会消耗资源; 服务器没有返回有效数据，程序超时

## Websocket

```
    let ws = new Websocket(url)
```

+ ws.readystate

* 0: 表示连接尚未建立。
* 1： 表示连接已建立，可以进行通信
* 2： 表示连接正在进行关闭。
* 3： 表示连接已经关闭或者连接不能打开。

+ ws的监听
* ws.onopen
* ws.onerror
* ws.onmessage
* ws.onclose
