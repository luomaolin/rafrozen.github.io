remote connection

**main problem is internet port not allowed

常用命令介绍
firewall-cmd --state                           ##查看防火墙状态，是否是running
firewall-cmd --reload                          ##重新载入配置，比如添加规则之后，需要执行此命令
firewall-cmd --get-zones                       ##列出支持的zone
firewall-cmd --get-services                    ##列出支持的服务，在列表中的服务是放行的
firewall-cmd --query-service ftp               ##查看ftp服务是否支持，返回yes或者no
firewall-cmd --add-service=ftp                 ##临时开放ftp服务
firewall-cmd --add-service=ftp --permanent     ##永久开放ftp服务
firewall-cmd --remove-service=ftp --permanent  ##永久移除ftp服务
firewall-cmd --add-port=80/tcp --permanent     ##永久添加80端口
iptables -L -n                                 ##查看规则，这个命令是和iptables的相同的
man firewall-cmd                               ##查看帮助

===========================================================

vncserver [:<number>] [-name <desktop-name>] [-depth <depth>]
                 [-geometry <width>x<height>]
                 [-pixelformat rgbNNN|bgrNNN]
                 [-fp <font-path>]
                 [-fg]
                 <Xvnc-options>...


       vncserver -kill <X-display>
       vncserver -list

vncserver[:n] 开服务

vncserver -list 看有几个在运行

vncserver -kill :n   杀掉第几个x-display

vncpasswd           修改密码




=============================================================

RPM 安装操作

命令：

rpm -i 需要安装的包文件名

举例如下：

rpm -i example.rpm 安装 example.rpm 包；

rpm -iv example.rpm 安装 example.rpm 包并在安装过程中显示正在安装的文件信息；

rpm -ivh example.rpm 安装 example.rpm 包并在安装过程中显示正在安装的文件信息及安装进度；

RPM 查询操作

命令：

rpm -q …

附加查询命令：

a 查询所有已经安装的包以下两个附加命令用于查询安装包的信息；

i 显示安装包的信息；

l 显示安装包中的所有文件被安装到哪些目录下；

s 显示安装版中的所有文件状态及被安装到哪些目录下；以下两个附加命令用于指定需要查询的是安装包还是已安装后的文件；

p 查询的是安装包的信息；

f 查询的是已安装的某文件信息；

举例如下：

rpm -qa | grep tomcat4 查看 tomcat4 是否被安装；

rpm -qip example.rpm 查看 example.rpm 安装包的信息；

rpm -qif /bin/df 查看/bin/df 文件所在安装包的信息；

rpm -qlf /bin/df 查看/bin/df 文件所在安装包中的各个文件分别被安装到哪个目录下；

RPM 卸载操作

命令：

rpm -e 需要卸载的安装包

在卸载之前，通常需要使用rpm -q …命令查出需要卸载的安装包名称。

举例如下：

rpm -e tomcat4 卸载 tomcat4 软件包

RPM 升级操作

命令：

rpm -U 需要升级的包

举例如下：

rpm -Uvh example.rpm 升级 example.rpm 软件包

RPM 验证操作

命令：

rpm -V 需要验证的包

举例如下：

rpm -Vf /etc/tomcat4/tomcat4.conf

输出信息类似如下：

S.5....T c /etc/tomcat4/tomcat4.conf

其中，S 表示文件大小修改过，T 表示文件日期修改过。限于篇幅，更多的验证信息请您参考rpm 帮助文件：man rpm

RPM 的其他附加命令

--force 强制操作 如强制安装删除等；

--requires 显示该包的依赖关系；

--nodeps 忽略依赖关系并继续操作；

================================================
立刻关机：
sudo halt
sudo init 0
sudo shutdown -h now
sudo shutdown -h 0

定时/延时关机：
sudo shutdown -h 19:30
sudo shutdown -h +30      ##单位为分钟

重启：
sudo reboot
sudo init 6
sudo shutdown -r now


休眠：

sudo pm-hibernate

待机(挂起)：
sudo pm-suspend
