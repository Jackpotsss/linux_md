# SELinux

安全增强Linux ,是Linux内核的一个安全子模块. 

SELinux 支持三种模式:

- 强制模式   enforcing
- 宽容模式  permissive
- 关闭   disabled



使用 sestatus 命令查看 SELinux 的运行状态:

```shell
[root@localhost vsftpd]# sestatus
SELinux status:                 enabled
SELinuxfs mount:                /sys/fs/selinux
SELinux root directory:         /etc/selinux
Loaded policy name:             targeted
Current mode:                   enforcing
Mode from config file:          enforcing
Policy MLS status:              enabled
Policy deny_unknown status:     allowed
Max kernel policy version:      28

```





```shell
# 修改selinux配置文件
cat /etc/selinux/config  
```



## 永久关闭 SELinux

```shell
# 1.修改配置文件内容
vi /etc/selinux/config  
# 2.把 SELINUX 选项修改为 disabled
SELINUX=disabled
# 3.重启服务器
reboot
```



