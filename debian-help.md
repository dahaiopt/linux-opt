

| 命令| 作用
| --------- | -------- 
| `/etc/motd`   | 用户默认登陆信息文件
| `su -l`       | 保存当前用户的环境设定
| `su`          | 会保存当前用户的一些环境设定
| `chvt 1`      | 切换到控制台1
| `shutdown -h now`| 普通多用户模式模式下，可以使用命令行关闭系统
| `poweroff -i -f` | 单用户模式下，可以使用命令行关闭系统
|   如果在“`/etc/inittab`”中含有“`ca:12345:ctrlaltdel:/sbin/shutdown -t1 -a -h now`”，那么你可以按下`Ctrl-Alt-Delete`（同时按下`左 Ctrl 键`、`左 Alt 键`和`Delete`）来关机        |  
| 恢复一个正常的控制台 |  当做了一些滑稽的事（例如“`cat<二进制文件>`”）后，屏幕会发狂，你可以在命令行输入“`reset`”。你可能无法在屏幕上看到你输入的命令。你也可以输入“`clear`”来清屏
| `apt-get install package_name`| 安装这些包
| `adduser fish`   |  创建一个用户名为 `fish` 的账号         
 ### sudo 配置    
  对于典型的单用户工作站，例如运行在笔记本电脑上的桌面Debian系统，通常简单地配置sudo(8)来使为非特权用户（例如用户`penguin`）只需输入用户密码而非root密码就能获得管理员权限。

```language
echo "penguin  ALL=(ALL) ALL" >> /etc/sudoers
```
 

另外，可以使用下列命令使非特权用户（例如用户`penguin`）无需密码就获得管理员权限。

```language
echo "penguin  ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
```
## 查询你的 CentOS 安装
rpm -qd (packagename)

| 快捷键| 作用
| --------- | -------- 
|  `Ctrl-D`    | 用户默认登陆信息文件
| `su -l`      | 保存当前用户的环境设定
| `su`         | 会保存当前用户的一些环境设定
| `chvt 1`     | 切换到控制台1


 **重要目录的用途列表**

| 目录 | 目录用途 |
| --- | --- |
| `/` | 根目录 |
| `/etc/` | 系统范围的配置文件 |
| `/var/log/` | 系统日志文件 |
| `/home/` | 所有非特权用户的用户目录 |

|          
