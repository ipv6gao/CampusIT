## 2017-12-07  开始使用github作为日常的日志工具

## 2017-12-08
  
早上白云7点钟断电，发现原来二楼的UPS也不能提供电源，估计也电池也损坏。有3台服务器来电后不能自主启动，8606 和8610 全部断电，白云电源的问题非常严重。

### 8606和8610的错误代码
```
*Dec  7 22:58:25: %TIPC-6-NET_START: Started in network mode
*Dec  7 22:58:25: %TIPC-6-NET_INFO: Own node address <1.1.90>, network identity 4711
*Dec  7 22:58:25: %TIPC-6-ENABLE_BEARER: Enabled bearer <eth:s8696>, discovery domain <0.0.0>, priority 10
*Dec  7 22:58:26: %MODULE-6-INSTALL: Install Module M8600-02XFP24SFP/12GT-E in slot 1.
*Dec  7 22:58:26: %REDUNDANCY-6-INITIALIZING: Initialize as master Supervisor.
*Dec  7 22:58:26: %REDUNDANCY-6-STM_ON_MASTER: State Machine start up on master Supervisor.
*Dec  7 22:58:26: %DP-6-FAN_OK: Fan 1/1 ok.
*Dec  7 22:58:26: %DP-6-FAN_OK: Fan 1/2 ok.
*Dec  7 22:58:26: %DP-6-FAN_OK: Fan 1/3 ok.
*Dec  7 22:58:26: %DP-6-FAN_OK: Fan 1/4 ok.
*Dec  7 22:58:26: %DP-6-FAN_OK: Fan 1/5 ok.
*Dec  7 22:58:26: %DP-6-FAN_OK: Fan 1/6 ok.
*Dec  7 22:58:26: %DP-6-POWER_OK: Power 1 ok.
*Dec  7 22:58:26: %DP-6-POWER_OK: Power 2 ok.
*Dec  7 22:58:29: %TIPC-6-ESTABLISHED_LINK: Established link <1.1.90:s8696-1.1.10:s8696> on network plane A, owner signature 11353, peer session 11353
*Dec  7 22:58:58: %OIR-6-INSCARD: Card inserted in slot 1, interfaces are now online.
*Dec  8 06:59:09: %SYS-6-CLOCKUPDATE: System clock has been updated to 06:59:09 bj Fri Dec  8 2017.
*Dec  8 06:59:11: %LINK-3-UPDOWN: Interface Loopback 0, changed state to up.
```
### 6810风扇错误代码
```
2017-12-08 07:41:51  @4-ENTITYCHANGE:Fan 4 state has translated to work
2017-12-08 07:41:51  @4-ENTITYCHANGE:Fan 4 state has translated to stop
2017-12-08 07:41:53  @4-ENTITYCHANGE:Fan 4 state has translated to work
2017-12-08 07:41:53  @4-ENTITYCHANGE:Fan 4 state has translated to stop
2017-12-08 07:41:55  @4-ENTITYCHANGE:Fan 4 state has translated to work
2017-12-08 07:41:55  @4-ENTITYCHANGE:Fan 4 state has translated to stop
```
		 
## 2017-12-11
白云下午4点多，移动公司在2楼改造电路，造成二楼断电，约5点半恢复正常。

## 2017-12-12
文正楼601 改做校庆办公室，面板号36 37 ，使用一个飞鱼路由器 ssid meetingRome6 ，使用TPLink 八口百兆交换机一个，网线六根约100米

## 2017-12-13
计算中心W2机房更换千兆交换机，协助配置交换机，原来是26.3，现在改为26.5和26.10两台设备。有几个要点：

### 1关闭广播抑制
```
no storm-control broadcast
no storm-control unicast	
```
### 2配置trunk 

### 3配置vlan

### 4设置Telnet密码，配置默认路由网管等。

```
interface VLAN 1
 no ip proxy-arp
 ip address 192.168.26.5 255.255.255.240
 !
 ip route 0.0.0.0 0.0.0.0 192.168.26.1
!

snmp-server community xxx ro 
line con 0
line vty 0 4
 login
 password xxx
!

clock timezone bj 8 0
logging server 222.65.164.132
enable password xxx
```  

高性能计算 修改用户00002475的机时

## 2017-12-18
白云ss区的计费系统彻底瘫痪，无法启动，已经请示LD，准备月底或本周期结束后彻底关闭ss区网络。

![故障的浪潮服务器已经运行十多年了](https://github.com/ipv6gao/CampusIT/blob/master/images/20171219095318.png)

## 2017-12-20
逸夫楼51.2显示离线，但端口依旧有流量，初步怀疑是IP冲突之类的，目前进一步观察。后来重启解决。
BY5号实验楼106报障，老问题，线路老化，无法解决，中午重启设备试试。

## 2017-12-21
个别服务器发现doubleplusar病毒，正在查杀，win自带的查杀没有木马，360查杀63个木马。

## 2017-12-22
by早上4点多断电，今年已经发生多次，实在是无法容忍

## 2017-12-25
高性能计算 修改用户00002625的机时