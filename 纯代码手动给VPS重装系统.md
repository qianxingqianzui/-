前言  
我们在使用VPS的时候避免不了总要重新安装系统，或者从Centos到Debian又或者VPS厂商安装的默认系统有一些限制，不论哪种原因都会经常给VPS安装系统，Linux系统的安装不像Windows系统安装时间那么长而且安装很简单。  
安装限制  
仅适用于KVM，不适合OpenVZ。  
开始安装  
Centos安装Debian  
1、安装所需软件  
```yum install -y gawk sed grep```  
2、下载脚本  
```wget --no-check-certificate -qO DebianNET.sh 'https://moeclub.org/attachment/LinuxShell/DebianNET.sh' && chmod a+x DebianNET.sh```  
3、自动安装  
```bash DebianNET.sh -d 9 -v 64 -a -p WalterlvPwd```  
其中64是64位的意思 -a是自动安装 -m 手动安装 手动安装需要VNC界面操作。-p后面的是root密码 可自定义  
4、VNC界面  
![baidu](https://gitee.com/qingyu520/imgs/raw/master/qingyu520/imgs/014544qqtupian20201116.png "安装进度图")  
在VPS控制台中有VNC控制，如果没有的话也没关系，等待10分钟左右自动安装完成就可以SSH连接了  
其他安装脚本（收集未测试，不断更新）  
Debian/Ubuntu  
一、安装软件  
```apt-get update```  
```apt-get install -y xz-utils openssl gawk file```  
###RedHat/CentOS  
```yum update```  
```yum install -y xz openssl gawk file```  
二、下载脚本  
```wget --no-check-certificate https://zhujiwiki.com/wp-content/uploads/2018/04/InstallNET.sh```  
```chmod -x InstallNET.sh```  
三、安装系统  
1、安装Debian 9 x64  
```bash InstallNET.sh -d 9 -v 64 -a```  
###安装Ubuntu各版本  
2、安装Ubuntu 17.04 x64  
```bash InstallNET.sh -u zesty -v 64 -a```  
###安装CentOS各版本  
3、安装CentOS 6.9 64位  
```bash InstallNET.sh -c 6.9 -v 64 -a --mirror 'http://vault.centos.org'```  
安装Windows Server2012 R2 data center 这个建议在Debian9下DD安装。  
```bash InstallNET.sh -dd 'https://down.zhujiwiki.com/windows-dd/S2012R2DATA2018410.vhd.gz'```  
四、用户名密码  
```默认root密码为 MoeClub.org```  
#[我的博客原文地址](https://www.qxqianzui.tk/2020/11/%e8%87%aa%e5%b7%b1%e6%89%8b%e5%8a%a8%e7%ba%af%e4%bb%a3%e7%a0%81%e7%bb%99vps%e9%87%8d%e8%a3%85%e7%b3%bb%e7%bb%9f%e6%95%99%e7%a8%8b.html)
