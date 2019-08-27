https://github.com/asuhu/lnamp
1、一键源码编译安装LNMP LAMP 支持CentOS6、CentOS7、RHEL6、RHEL7



01、一键源码编译安装LNMP LAMP 支持CentOS6、CentOS7、RHEL6、RHEL7
02、Nginx/1.12.2 built with OpenSSL 1.1.0g
03、Apache2.2为PreforkMPM,Apache2.4为Event MPM(编译Prefork、Worker和Event三种MPM可以自行切换)
04、MySQL-5.6
05、MySQL-5.7
06、PHP集成了 Zend OPcache、Zend Guard Loader、ionCube Loader、 phpredis等模块
07、PHP集成snmp模块，支持zabbix、cacti、Nagios直接使用snmp协议
08、支持Redis-Server
09、Tomcat8 JDK1.8
10、curl 7.57.0 (x86_64-pc-linux-gnu) libcurl/7.57.0 OpenSSL/1.0.2n zlib/1.2.11 libidn2/2.0.4 nghttp2/1.26.0
11、TLS SNI support enabled
12、多个配置Nginx https和反向代理的例子

安装使用
cd /root
yum -y install wget screen curl python
screen -S lnamp
wget --no-check-certificate https://blog.asuhu.com/sh/lnamp.tar.gz
tar -zxvf lnamp.tar.gz
bash install.sh
一键YUM安装LNMP支持CentOS6、CentOS7、RHEL6、RHEL7

cd /root
yum -y install wget screen curl python
screen -S lnamp
wget --no-check-certificate https://blog.asuhu.com/sh/yum_nginx_php_mysql.sh
chmod +x yum_nginx_php_mysql.sh
./yum_nginx_php_mysql.sh 2>&1 | tee lnmp.log
2、一键安装shadowsocks-libev 支持CentOS6 CentOS7

cd /root
wget --no-check-certificate https://blog.asuhu.com/sh/shadowsocks-libev.sh
chmod +x shadowsocks-libev.sh
./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
ShadowsocksR一键安装脚本 支持CentOS，Debian，Ubuntu

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log
L2TP/IPSec一键安装脚本 支持CentOS6+，Debian7+，Ubuntu12+

如何检测是否支持TUN模块？
执行命令：
cat /dev/net/tun
如果返回信息为：cat: /dev/net/tun: File descriptor in bad state 说明正常
如何检测是否支持ppp模块？
执行命令：
cat /dev/ppp
如果返回信息为：cat: /dev/ppp: No such device or address 说明正常
当然，脚本在安装时也会执行检查，如果不适用于安装，脚本会予以提示。

使用方法：
root 用户登录后，运行以下命令：

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/across/master/l2tp.sh
chmod +x l2tp.sh
./l2tp.sh

使用命令：
ipsec status （查看 IPSec 运行状态）
ipsec verify （查看 IPSec 检查结果）
/etc/init.d/ipsec start|stop|restart|status （CentOS6 下使用）
/etc/init.d/xl2tpd start|stop|restart （CentOS6 下使用）
systemctl start|stop|restart|status ipsec （CentOS7 下使用）
systemctl start|stop|restart xl2tpd （CentOS7 下使用）
service ipsec start|stop|restart|status （Debian/Ubuntu 下使用）
service xl2tpd start|stop|restart （Debian/Ubuntu 下使用）
3、网速硬盘读写测试

wget -qO- http://qiniu.geecdn.com/bench.sh | bash
或者
wget -qO- http://qiniu.geecdn.com/bench2.sh | bash
或者
wget -qO- https://github.com/sivel/speedtest-cli/raw/master/speedtest_cli.py | python
4、linux 服务器性能一键测试脚本（一键unixbench）

wget -qO- http://qiniu.geecdn.com/unixbench.sh | bash
5、大量消耗服务器流量

wget -O /dev/null http://lgsea.catalysthost.com/10240MB.test
wget -O /dev/null http://repos.mia.lax-noc.com/speedtests/100tb.bin
