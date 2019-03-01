一般 CentOS 系统默认自带 python(系统要用，比如 yum 工具就是 python 写的)，但是经验看一般都不带 pip 工具，需要手动安装。

虽然这里介绍的是用 yum 方式安装 pip ，其实如果通常可以用一种更简单的方式可以安装 pip ，直接 sudo easy_install pip 就好了。（Mac也适用哦）

1. 安装扩展源EPEL
CentOS yum源 中默认没有 pip，需要安装 扩展源EPEL
`sudo yum -y install epel-release`

2. 安装 pip
`sudo yum -y install python-pip`

3. 检查是否安装成功
 `pip -V`