# tcpa
腾讯tcpa单边加速
1、首先我们使用下面命令下载并启用TCPA定制的内核。过程很简单，依次输入下面命令即可。TCPA定制的内核腾讯官方下载链接：https://share.weiyun.com/5AeyuFg 密码：d1swc1。大家可以使用下面命令直接下载到服务器操作即可。

#安装wget
yum -y install wget

#下载TCPA定制的内核到自己服务器
wget https://xz.wn789.com/TCPA/kernel-3.10.0-693.5.2.tcpa06.tl2.x86_64.rpm

#安装TCPA定制的内核
rpm -ivh kernel-3.10.0-693.5.2.tcpa06.tl2.x86_64.rpm --force

#重启服务器
reboot

#重启后查看内核是否为TCPA定制的内核
uname -a
使用uname -a命令查到到启用的内核是TCPA定制的内核我们的第一步就完成了。



2、下载TCPA安装包。TCPA安装包腾讯官方下载链接：https://share.weiyun.com/5RAyh7c密码：qeetzp。大家也可通过蜗牛下面的服务器下载命令直接下载到自己的服务器。

wget https://xz.wn789.com/TCPA/tcpa_packets_180619_1151.tar.bz2
3、安装TCPA。依次执行下面命令即可，会自动安装到/usr/local/storage/tcpav2下面。

#安装bzip2
yum -y install bzip2
#解压安装包
tar jxvf tcpa_packets_180619_1151.tar.bz2
#进入程序安装文件夹
cd tcpa_packets
#执行安装
sh install.sh
4、启用TCPA。这是最后一步了。

#进入启用TCPA程序所在目录
cd /usr/local/storage/tcpav2
#执行启动命令
sh start.sh
