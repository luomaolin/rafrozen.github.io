sudo vi /etc/vsftpd/vsftpd.conf 
local_enable=<YES/NO> :设置是否支持本地用户帐号访问
guest_enable=<YES/NO> :设置是否支持虚拟用户帐号访问
write_enable=<YES/NO> :是否开放本地用户的写权限
local_umask=<nnn> :设置本地用户上传的文件的生成掩码，默认为077
local_root=<file> :设置本地用户登陆后的目录，默认为本地用户的主目录
chroot_list_file=<filename> :当chroot_local_user=NO 且 chroot_list_enable=YES时，只有filename文件指定的用户可以执行chroot
anonymous_enable=<YES/NO> :设置是否支持匿名用户访问
anon_world_readable_only=<YES/NO> 是否开放匿名用户的浏览权限
anon_upload_enable=<YES/NO> 设置是否允许匿名用户上传
anon_mkdir_write_enable=<YES/NO> :设置是否允许匿名用户创建目录
anon_other_write_enable=<YES/NO> :设置是否允许匿名用户其他的写权限（注意，这个在安全上比较重要，一般不建议开，不过关闭会不支持续传）
anon_umask=<nnn> :设置匿名用户上传的文件的生成掩码，默认为022
＃允许匿名用户登录FTP
anonymous_enable=YES
＃设置匿名用户的登录目录（如需要，需自己添加并修改）
anon_root=/var/ftp/pub
＃打开匿名用户的上传权限
anon_upload_enable=YES
＃打开匿名用户创建目录的权限
anon_mkdir_write_enable=YES
＃打开匿名用户删除和重命名的权限（如需要，需自己添加）
anon_other_write_enable=YES
#匿名用户的掩码（如需要，需自己添加，含义：如umask是022,这时创建一个权限为666的文件，文件的实际权限为666-022=644）
anon_umask=022


ftp [hostname| ip-address]

下载
get [remote-file] [local-file]

ftp> get /rose/1.bmp 1.bmp

mget [remote-files]

ftp> mget *.* 

上传
put local-file [remote-file]
ftp> put 1.bmp /rose/333.bmp

mput local-files
ftp> mput *.bmp

