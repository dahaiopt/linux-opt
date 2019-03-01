##  xxx不在 sudoers 文件中。此事将被报告。
	问题描述

登录centos的时候，默认使用的是非root账号，在sudo命令时收到centos如下的警告：不在 sudoers 文件中。此事将被报告
**sudo**
命令的含义是：使用sudo命令的账号，将拥有root账户的权限来执行某项命令或者程序。但是不是所有的账号都可以使用sudo命令的。对此centos系统采用了一个办法，利用一个专门的文件来管理某些账号是否能使用sudo命令。显然，这个文件只有root账号才能修改和管理的。这个文件就是/etc/sudoers。
问题决绝

我们要做的就是切换到root账号，然后将平常用的非root账号添加到这个文件中。

现在我们使用su命令，切换到root账号，然后再调用visudo命令来添加账号。
`[gz@localhost ~]#su root`

在visudo命令调出的vim编辑窗口中，

`[root@localhost ~]#vim /etc/sudoers找到如下行：root ALL=(ALL:ALL) ALL ，向里面添加gz ALL=(ALL:ALL) ALL 保存`

