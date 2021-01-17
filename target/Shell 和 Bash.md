# Shell 和 Bash

​	Shell 是一个程序，给用户提供一个与系统对话的环境。这个环境只有一个命令提示符，让用户从键盘输入命令，所以又称命令行环境。

​	其次，Shell 是一个命令解释器，解释用户输入的命令，它支持变量、条件判断、循环操作等语法，使用 shell 语法可以写出命令脚本。



## Shell 种类





Bash（GNU Bourne-Again SHelll）

https://www.gnu.org/software/bash



```bash
#!/bin/bash

```



环境变量

```shell
# 显示所有
env
#
export
# 
set
#
unset

```



变量在被使用时，前面必须加 `$` 符号才行。



## 变量设置规则



- 变量与变量内容直接用等号=连接；
- 等号两边不能直接接空格；
- 变量名称只能是英文字母和数字



子进程会继承父进程的环境变量，但不会继承父进程的自定义变量。使用 export 可以将自定义变量



```shell
# 查看当前有哪些用户在操作系统
who
# 设置系统别名
alias
# 取消系统别名
unalias
# 查看系统时间
date
# 打印变量 或直接输出指定字符串
echo
# 将结果格式化输出到标准输出
printf
# 判断一个命令是否为内置命令
type

```





