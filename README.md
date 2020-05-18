# 更新软件源和系统
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
# 安装SS
	1. 下载：
	 wget -N --no-check-certificate "https://raw.githubusercontent.com/fantasy-chn/breakGFW/master/shadowsocks-all.sh"
	2. 赋予执行权限：
	 chmod +x shadowsocks-all.sh
	3. 运行脚本并保存日志：
	 ./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
	4. 运行控制：
	 /etc/init.d/shadowsocks-libev start | stop | restart | status
	 启动，停止，重启，查看状态
	5. 配置文件位置：
	/etc/shadowsocks-**/config.json
# 安装v2ray
	1. 下载：
 	 wget -N --no-check-certificate "https://raw.githubusercontent.com/fantasy-chn/breakGFW/master/v2ray.sh"
	2. 赋予执行权限：
 	 chmod +x v2ray.sh
	3. 运行脚本：
 	 ./v2ray.sh
	4. 重启服务：
	 systemctl restart v2ray
# 安装BBR
	1. 下载：
 	 wget -N --no-check-certificate "https://raw.githubusercontent.com/fantasy-chn/breakGFW/master/bbr.sh"
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
