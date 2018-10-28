the server is CentOS 7
use ssh to connect to server
and the code is shown blow
```
wget --no-check-certificate -O shadowsocks-libev.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh
chmod +x shadowsocks-libev.sh
./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
```
the code shown below is not necessary, it's used to speed up ss.
```
yum -y install wget
wget -N --no-check-certificate https://raw.githubusercontent.com/wn789/serverspeeder/master/serverspeeder.sh
bash serverspeeder.sh
```
if error occurs, use this to change the kernel
```
//step 1
rpm -ivh http://xz.wn789.com/CentOSkernel/kernel-firmware-2.6.32-504.3.3.el6.noarch.rpm
rpm -ivh http://xz.wn789.com/CentOSkernel/kernel-2.6.32-504.3.3.el6.x86_64.rpm --force
//step 2
rpm -qa | grep kernel
//step 3
reboot
//step 4
//do the installation again
