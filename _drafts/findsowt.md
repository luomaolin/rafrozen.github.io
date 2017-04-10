如果我们在Linux 系统上安装了某个软件，我们可以通过如下的三种方式来确定。
一． Which 命令
Shell 的which 命令可以找出相关命令是否已经在搜索路径中。 如：
[root@localhost ~]# which gcc
/usr/bin/gcc
二． Whereis 命令
Whereis 命令搜索更大范围的系统目录，和Shell 的搜索路径无关。 要注意，有些系统上的which 命令不显示用户没有执行权限的文件。
[root@localhost ~]# which ipppd
/sbin/ipppd
[root@localhost ~]# whereis ipppd
ipppd: /sbin/ipppd /usr/sbin/ipppd /usr/share/man/man8/ipppd.8.gz
三． Locate 命令
该命令会先考察预先编译好的一个文件系统的索引，以此确定与特定模式相匹配的文件名。 它搜索的并不特定与命令或者软件包，而是能够找到的任何类型的文件。
Locate 的数据库库通常由updatedb 命令在每天晚上重新生成，这个命令由cron来运行。 因此，执行一次locate 的结果不是总能够反映出文件系统新近的变化。
比如查看头文件signal.h
