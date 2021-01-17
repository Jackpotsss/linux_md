# FTP 服务

FTP （）文件传输协议基于20端口和21端口：

- 21端口用于传输FTP控制信息
- 20端口用于传输数据



​	在实际的FTP传输过程中，是否用到 20端口与FTP客户端设置的传输模式有关，主动模式使用20端口传输，被动模式使用哪个端口是协商决定的。

- 主动模式：客户端想FTP服务器发送端口信息，由服务器主动连接客户端的端口；
- 被动模式：FTP服务器开启并发送端口给客户端，由客户端主动连接服务器端口；





## vsftp

​	在Linux上比较常用的FTP服务软件是 vsftp  (目前版本3.0.2) ,

官网地址: 

vsftp 的配置文件在 /etc/vsftpd 目录下,主要有三个配置文件

```
ftpusers
user_list
vsftpd.conf
```



ftpusers:

​	不让登陆的用户配置在这个文件里,一行一个;







vsftpd.conf :

(使用 man vsftpd.conf 可以获得更详细的介绍)

```shell
# 允许匿名用户登陆
anonymous_enable=YES 
# 允许使用本地用户账号登陆
local_enable=YES 
#允许用户写数据
write_enable=YES 
# 通过20端口传输数据
connect_from_port_20=YES 
```



## 白名单 | 黑名单 (userlist)

​	user_list 配置文件中的内容要配合 vsftpd.conf 配置文件里的两个参数一起使用, userlist_enable 表示启用 userlist ; userlist_deny 表示 userlist 是允许登录ftp的白名单用户还是黑名单用户, YES 选项表示黑名单, 即加入文件列表的用户不允许登录ftp服务器, NO 选项表示白名单, 只有加入白名单的用户才能登录ftp服务器.

```shell
# 
userlist_enable=YES
userlist_deny=NO
userlist_file=/etc/vsftpd.user_list
```







## 严格的 chroot 功能

​	chroot 就是 change root ,也就是改变程序执行时所参考的根目录位置. Chroot 可以增强系统安全性,限制使用者的操作.

大多数的 FTP 服务器软件都提供 chroot 的功能，将实体用户的访问权限限制在他的家目录内；

```shell
chroot_local_user=YES
chroot_list_enable=YES
chroot_list_file=/etc/vsftpd/chroot_list
```

注:

​	chroot_list 文件默认是不存在的, 需要自行手动创建,



限制最大上线人数

max_clients=10

限制同一IP的来源数

max_per_ip=1





## 客户端访问FTP服务器

首先可以在linux 上使用 ftp 客户端工具访问 ftp 服务器, 如果本地没有  ftp 客户端,需要事先安装:

```shell
yum install ftp -y
```





客户端的浏览器可以访问

客户端编码:(以java为例)

sun.net.ftp 包提供了访问ftp服务器的相关工具类

```
FtpClient
```





