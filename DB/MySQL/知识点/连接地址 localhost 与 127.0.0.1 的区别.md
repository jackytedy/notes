* `localhot(local)` 不使用 TCP/IP 连接，而使用 Unix socket。它不受网络防火墙和网卡相关的的限制。
* `127.0.0.1` 是通过网卡传输，使用 TCP/IP 连接，依赖网卡，并受到网络防火墙和网卡相关的限制。

一般设置程序时本地服务用`localhost`是最好的，`localhost`不会解析成 IP，也不会占用网卡、网络资源。

有时候用`localhost`可以，但用`127.0.0.1`就不可以的情况就是在于此。猜想`localhost`访问时，系统带的本机当前用户的权限去访问，而用 IP 的时候，等于本机是通过网络再去访问本机，可能涉及到网络用户的权限。



