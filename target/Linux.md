# Linux

​	1991年芬兰赫尔辛基大学的 Linus Torvalds 开发了 Linux 操作系统（当时22岁）。



## Linus Torvalds

Linux之父：Linus Torvalds

<img src="https://gitee.com/Jackpotsss/pic_go/raw/master/img/image-20200913180131604.png" alt="image-20200913180131604" style="zoom:80%;" />



## Linux 标志

Linux 的标志是一只小企鹅，由 Linus Torvalds 设计。

<img src="https://gitee.com/Jackpotsss/pic_go/raw/master/img/image-20200915120454484.png" alt="image-20200915120454484" style="zoom:67%;" />



## 内核

Linux内核官网：kernel.org

<img src="https://gitee.com/Jackpotsss/pic_go/raw/master/img/image-20200829212737318.png" alt="image-20200829212737318" style="zoom:80%;" />



## 发行版

几个主流的Linux发行版官网：

- CentOS官网：centos.org 

- RedHat官网：redhat.com/zh 

- Ubuntu官网 ：cn.ubuntu.com 

本文基于**CentOS 7.x** 进行研究和学习，更多发行版请在  https://mirrors.kernel.org 网址查看。



## 常用热键与帮助



### man	操作手册

​	几乎每个软件在发布时都会将操作手册（manual）一起发布，使用 man 命令可以查看命令的操作手册，

```bash
# 查看 java 命令的操作手册
man	java
```

man 命令会以 



### help	寻求帮助

​	绝大多数的命令都可以使用 `--help` 选项查看帮助文档，当你忘记命令的相关选项时，使用 help 选项可以快速查看和确认。当你想查看该命令的详细介绍时，使用 man 命令打开操作说明。



### tab键 	快速联想

Tab键 可以快速补齐，枚举出相关的内容。



### whereis 查看命令位置

​	`whereis` 用于查看命令的二进制文件，源文件和操作手册文件的位置。

常用选项

```bash
# 只查看命令的二进制文件的位置
-b
# 只查看命令的源文件的位置
-s
# 只查看命令的操作手册文件的位置
-m
```

示例:

```bash
# 查看命令的二进制文件，源文件和操作手册文件的位置
[root@iz2ze98 ~]# whereis java
java: /usr/bin/java /usr/java/jdk1.8.0_131/bin/java /usr/share/man/man1/java.1
[root@iz2ze98 ~]# whereis -b java
java: /usr/bin/java /usr/java/jdk1.8.0_131/bin/java
[root@iz2ze98 ~]# whereis -m java
java: /usr/share/man/man1/java.1
```

which

​	查看命令的可执行文件的完整路径

```bash
# 查看命令的可执行文件的完整路径
[root@iz2ze98 ~]# which java
/usr/java/jdk1.8.0_131/bin/java
```





## 命令总览



| 命令     | 描述                   |
| -------- | ---------------------- |
| cd       | 切换目录               |
| ls /  ll | 查看当前目录的文件列表 |
| pwd      | 查看当前目录的绝对路径 |
| chmod    | 修改文件基本权限       |
| chown    | 修改文件所属用户       |
| chgrp    | 修改文件所属用户组     |
|          |                        |
| su       |                        |
| sudo     |                        |
| find     | 查找文件               |
| grep     |                        |
| gzip     | 解压缩文件             |
| gunzip   | 解压文件               |
| zip      | 压缩文件               |
| unzip    | 解压文件               |
| tar      | 打包/压缩文件          |
| top      | 查看系统硬件运行状态   |
| free     | 查看内存使用情况       |

注：

​	Linux 命令的选项普遍有一个特点，单横杠 - 表示缩写，双横杠 -- 表示全拼，如 -h 等价于 --help， -l 等价于 --list，- a 等价于 --all 等；但单横杠的缩写选项只能代替一部分双横杠的全拼选项，稍微复杂或指定参数值的选项还是得用全拼形式。



| 命令 | 描述 |
| ---- | ---- |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |





