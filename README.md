# Reference of Vehicle Security

### In-vehicle Wireless Security
- 2020,NDSS,[Hold the Door! Fingerprinting Your Car Key to Prevent Keyless Entry Car Theft](https://www.ndss-symposium.org/ndss-paper/hold-the-door-fingerprinting-your-car-key-to-prevent-keyless-entry-car-theft/)
**Keyless Entry Security**
- 2019,USENIX Security,,[Losing the Car Keys: Wireless PHY-Layer Insecurity in EV Charging](https://www.usenix.org/conference/usenixsecurity19/presentation/baker)
CCS(电动汽车充电的主要标准)安全，充电侧信道。
- 2016,USENIX Security, [Lock It and Still Lose It —on the (In)Security of Automotive Remote Keyless Entry Systems](https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/garcia)
**Keyless Entry Security**
- 2013,USENIX Security, [Dismantling Megamos Crypto: Wirelessly Lockpicking a Vehicle Immobilizer](https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/verdult-dnp)
车载防盗装置安全。
- 2011,NDSS,[Relay Attacks on Passive Keyless Entry and Start Systems in Modern Cars](https://www.ndss-symposium.org/ndss2011/relay-attacks-on-passive-keyless-entry-and-start-systems-in-modern-cars)
**Keyless Entry Security**
-2010,USENIX Security,[Security and Privacy Vulnerabilities of In-Car Wireless Networks: A Tire Pressure Monitoring System Case Study](https://www.usenix.org/legacy/events/sec10/tech/full_papers/Rouf.pdf)
无线轮胎压力监测系统的隐私和安全

### Robotic Vehicles Security
RVs包括无人机，无人汽车等。
- 2019, Usenix Security, [RVFuzzer: Finding Input Validation Bugs in Robotic Vehicles through Control-Guided Testing](https://www.usenix.org/system/files/sec19-kim.pdf)
- 2018,CCS,[Detecting Attacks Against Robotic Vehicles: A Control Invariant Approach](https://dl.acm.org/doi/10.1145/3243734.3243752)
提出了一种新的攻击检测框架，通过派生和监控控制不变量(CI)来识别动态的对RVs的外部物理攻击。更具体地说，提出了一种通过联合建模车辆的物理特性、控制算法和物理定律来提取这些不变量的方法。这些不变量以状态空间的形式表示，然后可以实现并插入车辆的控制程序二进制进行运行时不变量检查。我们将CI框架应用于11个RVs，包括四旋翼、六旋翼和地面探测车，并证明了不变检查可以检测三种常见的物理攻击类型——包括传感器攻击、驱动信号攻击和参数攻击

### CAN Bus & ECU Security
现主要研究是逆向CAN协议(车辆生产商)，CAN IDS两个热点。
- 2020,NDSS,[Automated Cross-Platform Reverse Engineering of CAN Bus Commands From Mobile Apps](http://secpaper.cn/download?type=pdf&name=2060814796_NDSS_20_Automated_Cross_Platform_Reverse_Engineering_of_CAN_Bus_Commands_From_Mobile_Apps)
**Reverse CAN**
主要从In-Vehicle Infotainment (IVI) apps.和OBD-II dongle apps.进行自动化逆向分析CAN。
Backward program slicing.
![](https://raw.githubusercontent.com/ReAbout/Reference-Vehicle-Security/main/img/2020_1.png?token=ACHGSPLXOZKAMJUZJ3OE3HC73GB3G)    
车辆逆向网站：https://vehicle-reverse-engineering.fandom.com/wiki/Vehicle_Reverse_Engineering_Wiki     
- 2020,NDSS,[EASI: Edge-Based Sender Identification on Resource-Constrained Platforms for Automotive Networks](https://www.ndss-symposium.org/ndss-paper/easi-edge-based-sender-identification-on-resource-constrained-platforms-for-automotive-networks/)
识别CAN bus中的发送者。
- 2020,S&P, [Automated Reverse Engineering and Privacy Analysis of Modern Cars](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9152789)
提出汽车隐私和安全分析工具AutoCAN，它通过接入车内网络，提取时间序列数据，自动分析汽车所收集的数据。研究结果显示，汽车制造商可以追踪GPS定位系统的位置、乘客人数、他们的体重、门、灯和空调的使用统计数据。还发现了隐藏功能，原始设备制造商嵌入了远程禁用汽车或在司机超速时收到警报的功能。
- 2019,CCS,[LibreCAN: Automated CAN Message Translator](https://doi.org/10.1145/3319535.3363190)
**Reverse CAN**。LibreCAN逆向CAN协议工具。
- 2019,USENIX Security,[CANvas: Fast and Inexpensive Automotive Network Mapping](https://www.usenix.org/conference/usenixsecurity19/presentation/kulandaivel)
CAN网络识别。
- ,2018, CCS,[Scission: Signal Characteristic-Based Sender Identification and Intrusion Detection in Automotive Networks](https://dl.acm.org/doi/abs/10.1145/3243734.3243751)
**CAN IDS**。它使用从CAN帧中提取的指纹来实现对发送ecu的识别。
-2017，ACM CCS， [Viden: Attacker Identification on In-Vehicle Networks ](http://secpaper.cn/download?type=pdf&name=1610073715_CCS17_Viden__Attacker_Identification_on_In_Vehicle_Networks)
识别攻击ECU。
-2016，ACM CCS，[Error Handling of In-vehicle Networks Makes Them Vulnerable](http://secpaper.cn/download?type=pdf&name=3662890634_CCS16_Error_Handling_of_In_vehicle_Networks_Makes_Them_Vulnerable)
**CAN Attack**
- 2016,USENIX Security,[Fingerprinting Electronic Control Units for Vehicle Intrusion Detection](https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/cho)
**CAN IDS**。基于时钟的入侵检测系统(CIDS)。它测量并利用周期性车内信息的间隔来进行指纹识别ecu。通过递归最小二乘(RLS)算法，将提取的指纹用于构建ECUs时钟行为的基线。基于这一基线，CIDS使用累积和(CUSUM)来检测识别错误中的任何异常偏移，这是入侵的明显迹象。

### Roadside(V2R) Security
- 2018,USENIX Security,[All Your GPS Are Belong To Us: Towards Stealthy Manipulation of Road Navigation Systems](https://www.usenix.org/conference/usenixsecurity18/presentation/zeng)    
-  2018,NDSS,[Exposing Congestion Attack on Emerging Connected Vehicle based Traffic Signal Control.](http://wp.internetsociety.org/ndss/wp-content/uploads/sites/25/2018/02/ndss2018_01B-2_Chen_paper.pdf)   
目标：美国运输部（USDOT）赞助的基于CV的交通控制系统 
- 2011,USENIX Security,[The Phantom Tollbooth: Privacy-Preserving Electronic Toll Collection in the Presence of Driver Collusion](http://static.usenix.org/events/sec11/tech/full_papers/Meiklejohn.pdf)    
收费站
- 2010,USENIX Security,[PrETP: Privacy-Preserving Electronic Toll Pricing](http://www.usenix.org/events/sec10/tech/full_papers/Balasch.pdf)   


###  Autonomous Driving
- 2020,USENIX Security ,[Stealthy Tracking of Autonomous Vehicles with Cache Side Channels](https://www.usenix.org/conference/usenixsecurity20/presentation/luo)
- 2020,USENIX Security ,[SAVIOR: Securing Autonomous Vehicles with Robust Physical Invariants](https://www.usenix.org/conference/usenixsecurity20/presentation/quinonez)
- 2019,CCS,[Adversarial Sensor Attack on LiDAR-based Perception in Autonomous Driving](https://doi.org/10.1145/3319535.3339815)


### Survey
 - [智能网联汽车报告 2016](http://beijing.xstore.qihu.com/360report/2016%E6%99%BA%E8%83%BD%E7%BD%91%E8%81%94%E6%B1%BD%E8%BD%A6%E4%BF%A1%E6%81%AF%E5%AE%89%E5%85%A8%E5%B9%B4%E5%BA%A6%E6%8A%A5%E5%91%8A.pdf?response-content-disposition=attachment%3B%20filename%3D2016%E6%99%BA%E8%83%BD%E7%BD%91%E8%81%94%E6%B1%BD%E8%BD%A6%E4%BF%A1%E6%81%AF%E5%AE%89%E5%85%A8%E5%B9%B4%E5%BA%A6%E6%8A%A5%E5%91%8A.pdf&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=c45cea910ed26c418079beef529f2f2b%2F20201208%2Fbeijing%2Fs3%2Faws4_request&X-Amz-Date=20201208T001044Z&X-Amz-SignedHeaders=host&X-Amz-Expires=43200&X-Amz-Signature=db283fd770b28437613cd7b20172161aaff69f8f4eec179eac53d15ea06e94e2)
- 2019,信息安全学报， [车联网安全综述](http://jcs.iie.ac.cn/xxaqxb/ch/reader/create_pdf.aspx?file_no=20190302&year_id=2019&quarter_id=3&falg=1)
- [Security and Privacy in the Internet of Vehicles](https://ieeexplore.ieee.org/abstract/document/7428337)
- [Internet of Vehicles: Architecture, Protocols, and Security](https://ieeexplore.ieee.org/abstract/document/7892008)
- 2011 ,USENIX Security,[Comprehensive Experimental Analyses of Automotive Attack Surfaces](http://static.usenix.org/events/sec11/tech/full_papers/Checkoway.pdf)
- 2010 ,S&P ,[Experimental Security Analysis of a Modern Automobile](https://doi.org/10.1109/SP.2010.34)


### Technology Blog
- [车联网安全系列——特斯拉 NFC 中继攻击（CVE-2020-15912）](https://www.anquanke.com/post/id/213885)
- [腾讯科恩实验室：雷克萨斯汽车安全研究综述报告](https://keenlab.tencent.com/zh/2020/03/30/Tencent-Keen-Security-Lab-Experimental-Security-Assessment-on-Lexus-Cars/)
利用蓝牙协议栈漏洞获取shell
-  [在Tesla Model S上实现Wi-Fi协议栈漏洞的利用](https://keenlab.tencent.com/zh/2020/01/02/exploiting-wifi-stack-on-tesla-model-s/)
利用中控wifi协议栈获取shell，渗透汽车内部网络
- [黑客是如何从T-Box接入车厂内网的？](https://skygo.360.cn/2018/10/16/penetrate-intranet-via-tbox/)
- https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=tesla


