# 更新软件源和系统

	<h1>yum update </h1>
yum update  
yum upgrade
# 安装wget
yum -y install wget
# 时区设置
1. 更改为中国上海时区：  
 cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime  
  提示 cp: overwrite ‘/etc/localtime’?  输入 y 按回车确认  
2. 安装ntpdate工具：  
 yum install -y ntp  
3. 设置系统时间与网络时间同步：  
 ntpdate us.pool.ntp.org  
4. 将系统时间写入硬件时间：  
 hwclock --systohc  
5. 查看时间：  
 系统时间date  
 硬件时间hwclock
# 安装v2ray
1. 下载：  
 wget -N --no-check-certificate "https://raw.githubusercontent.com/fantasy-chn/v2ray/master/v2ray.sh"  
2. 赋予执行权限：  
 chmod +x v2ray.sh  
3. 运行脚本：  
 ./v2ray.sh  
# 安装BBR
1. 下载：  
 wget -N --no-check-certificate "https://raw.githubusercontent.com/fantasy-chn/v2ray/master/bbr.sh"  
2. 赋予执行权限：  
 chmod +x bbr.sh  
3. 运行脚本：  
 ./bbr.sh  
# BestTrace查看路由回程
1. 下载：  
 wget https://cdn.ipip.net/17mon/besttrace4linux.zip  
2. 解压：  
 yum -y install wget zip  
 unzip besttrace*  
3. 赋予执行权限：  
 chmod +x besttrace  
4. 运行查询：  
 ./besttrace 8.8.8.8
