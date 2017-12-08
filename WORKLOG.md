## 2017-12-07  开始使用github作为日常的日志工具
------

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
		 
## 2017-12-09