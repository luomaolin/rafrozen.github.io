# Linux上挂载mtp设备
查看是否能检测到mtp设备
```
lsusb
```
编辑文件 /etc/fuse.conf ，去掉 user_allow_other 一行前面的注释。
编辑文件 /etc/udev/rules.d/xxxo.rules
在里面添加一行：
```
SUBSYSTEM==”usb”, ATTR{idVendor}==”xxxxx″, ATTR{idProduct}==”xxxx″, MODE=”0666″


```
挂载设备： (注：挂载时，设备必须处于亮屏状态）
```
gvfs-mount -o allow_other /mnt/mtp
```