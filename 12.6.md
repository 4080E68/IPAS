
## OSI 七層 && 攻擊手法
[維基百科](https://zh.wikipedia.org/wiki/OSI%E6%A8%A1%E5%9E%8B)
[TCP/IP協定](https://zh.wikipedia.org/wiki/TCP/IP%E5%8D%8F%E8%AE%AE%E6%97%8F)
### 第7層 應用層（Application Layer）
```
提供為應用軟體而設計的使用者介面；
存取網路資源服務、管理服務、遠端存取服務
功能：檔案、印表、訊息、資料庫、應用服務等
例如：HTTP、SMTP、SNMP、FTP、Telnet、SIP、SSH、NFS、RTSP、XMPP、Whois、ENRP、TLS
```
```
常見攻擊手法：
DNS Poisoning、Brute force Login、SQL Injection及Cross-Site Scripting
```

### 第6層 表達層（Presentation Layer）
```
將來自本地端應用程式的資料格式轉換(或者是重新編碼)成為網路的標準格式。
例如：編碼語解碼、加解密、字元轉換、資料形態轉換、ASCII、EDCDIC轉換、翻譯
      XDR、ASN.1、SMB、AFP、NCP
```
```
常見攻擊手法：

```
### 第5層 會議層（Session Layer）
```
維護電腦網路中兩台電腦之間的通訊連接
例如：ASAP、ISO 8327 / CCITT X.225、RPC、NetBIOS、ASP、IGMP、Winsock、BSD sockets
```
```
常見攻擊手法：

```
### 第4層 傳輸層（Transport Layer）
```
流量控制、錯誤偵測與修正
例如：TCP、UDP、RTP、SCTP、SPX、ATP、IL
```
```
---- TCP(Transmission Control Protocol) ----
        可靠的一對一連接(三項交握)，確保兩端都有收到每個封包，並且封包被正確的解碼與排序
  
        [在TCP協定上的協定]
            HTTP（Hypertext Transfer Protocol，超文字傳輸協定）
            HTTPS（Hypertext Transfer Protocol over Secure Socket Layer, or HTTP over SSL，安全超文字傳輸協定）
            FTP（File Transfer Protocol，檔案傳輸協定）
            POP3（Post Office Protocol, version 3，郵局協定）
            SMTP（Simple Mail Transfer Protocol，簡單郵件傳輸協定）
            TELNET（Teletype over the Network，網路電傳）
            SSH（Secure Shell，用於替代安全性差的TELNET）
  
---- UDP(User Datagram Protocol) ----
        不可靠的非連接傳輸，速度比TCP快，適合傳輸小封包
  
        [在UDP協定上的協定]
            BOOTP（Boot Protocol，啟動協定）
            NTP（Network Time Protocol，網路時間協定）
            DHCP（Dynamic Host Configuration Protocol，動態主機組態協定）
```
```
常見攻擊手法：
SYN Flood、DDoS及Session Hijacking
```
### 第3層 網路層（Network Layer）
```
負責安排路徑、設定IP位址與封裝
例如：IP、ICMP、IPX、BGP、OSPF、RIP、IGRP、EIGRP、ARP、RARP、X.25、路由器
```
```
常見攻擊手法：
Source Route、Smurf 、Ping of Death 
```
### 第2層 資料連結層（Data Link Layer）
```
[1]邏輯連結控制(Logical Link Control, 簡稱LLC)
  與網路層連接，管理兩端連線並控制資料流動與順序
[2]媒介存取控制(Media Access Control, 簡稱MAC)
  與實體層連接，經過纜線在兩端之間傳送訊框(frame)
  
此層負責轉換網路層的「封包」與實體層的「訊號」，
並透過checksum的機制檢查實體層傳來的訊號日否正確，
若有錯誤則要求重送。

在這一層當中就制訂了 frame 的格式以及通過網路的方式。
包括訊框的資料格式、錯誤控制、流量控制、檢查資料傳輸錯誤的方法，
例如：乙太網路、權杖環、HDLC、ISDN、ATM、IEEE 802.11、FDDI、PPP
      MAC(media accesscontrol)、Physical address、Bridge、Switch
```
```
常見攻擊手法：
封包監聽與ARP Spoofing
```
### 第1層 實體層（Physical Layer）
```
在硬體上傳送數位訊號，各種硬體標準，傳輸時電壓的規範等等
例如：集線器(Repeater 1轉1)、中繼器(Hub 1轉多)、線路、無線電、光纖、針腳、電壓、線纜規範、網卡、主機介面卡
```
```
常見攻擊手法：
線路搭接與線路私接
```

## 常見PORT
|      用途     |                                      名稱                                      |             Port            |
| ------------- | ----------------------------------------------------------------------------- | --------------------------- |
|    檔案傳輸    |                         File Transfer Protocol, FTP                           |              21             | 
|  安全遠端登錄  |                             Secure Shell, SSH                                 |              22             | 
|    遠端登錄    |                                   Telnet                                      |              23             | 
|  簡單郵件傳輸  |                    Simple Mail Transfer Protocol, SMTP                        |              25             | 
|  網域名稱服務  |                          Domain Name Service, DNS                             |              53             | 
|   超文本傳輸   |                      HyperText Transport Protocol, http                       |              80             | 
|    郵件接收    |                     Post Office Protocol Version 3, POP3                      |              110            | 
|    網路時間    |                         Network Time Protocol, NTP                            |              123            | 
| 安全超文本傳輸 |                    Hypertext Transfer Protocol Secure, https                   |             443            | 
|    網路芳鄰    | 使用SMB (Simple Message Block)，<br>用NetBIOS來尋找設備 Linux 的Samba即為SMB軟體 | UDP137,138<br>TCP 139, 445 | 



# 無線網路
```
家用無線電話
衛星電視
行動電話
藍芽 (Bluetooth)
LTE-A
LTE
WCDMA
CDMA2000
EDGE
GSM
Wi-Fi
WiMax
ZigBee
Z-Wave
```
# 無線區域網路
```
無線區域網路 (wireless LAN or WLAN) 的標準為802.11系列，由IEEE在1997年制定
Wired Equivalent Privacy (WEP) 
```
# 無線網路攻擊手法
```
竊聽 (eavesdropping)
開放身分認證 (open authentication)
拒絕服務 (denial of service, DoS)
  身分認證洪水攻擊 (authentication flood attack) 
  解除授權洪水攻擊 (deauthentication flood attack)
  無線干擾攻擊 (network jamming attack) 
欺騙 (spoofing)
  欺騙基地台 (rogue access point) 
  孿生惡魔 (evil twin)
```
