# vpn
## openvz 加速
net-speeder可以适应多个系统，例如知名的搬瓦工、Virmach都能使用这个加速器，不过该加速器的原理暴力简单，就是双倍发包，这样可以减少丢包数量，但是发包过多容易被严格的主机商察觉封机，还有就是相当于流量少了一半，有些流氓但是确实很有效。

net-speeder支持主流Linux系统，同时支持OVZ、Xen、KVM多个架构。

### centos
```
wget --no-check-certificate https://gist.github.com/LazyZhu/dc3f2f84c336a08fd6a5/raw/d8aa4bcf955409e28a262ccf52921a65fe49da99/net_speeder_lazyinstall.sh
sh net_speeder_lazyinstall.sh

```
### Debian：
```
wget --no-check-certificate https://raw.githubusercontent.com/tennfy/debian_netspeeder_tennfy/master/debian_netspeeder_tennfy.sh
chmod a+x debian_netspeeder_tennfy.sh
bash debian_netspeeder_tennfy.sh

```

安装后执行：

```
nohup /usr/local/net_speeder/net_speeder venet0 "ip" >/dev/null 2>&1 &
```

加入开机启动：
```
echo 'nohup /usr/local/net_speeder/net_speeder venet0 "ip" >/dev/n

```
## shadowsocks
 ```
 apt-get install shadowsocks
 vi /etc/shadowsocks/config.json
 ssserver -c /etc/shadowsocks/config.json

 ```
