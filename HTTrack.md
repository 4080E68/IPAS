# HTTrack
```
[1] 將整個網站下載的工具
使用者可以通過HTTrack把網際網路上的網站頁面下載到本地電腦上。
基本用法
用法也很简洁，总共只有三部分，选项、过滤器规则和目标网址。

httrack [-选项] [+/-规则] 站点网址
例如：
httrack "http://www.all.net/abc/index.html" -O "/tmp/www.all.net" "+*.all.net/*" -v
```
## 指令
```
-w, --mirror

鏡像模式（默認）。

-W, --mirror-wizard

按照嚮導方式開啟鏡像模式。是一種半自動的的鏡像模式，以問答方式填控制參數。

-O, --path

站點鏡像保存的本地路徑，用法例如：
-O 站点镜像文件路径[,缓存及日志路径（可选）]
--continue

斷點續傳。

-P, --proxy

代理方式。不過貌似只支持http代理，如果無法使用socks代理可以使用tsocks用法如：

-P proxy:port or -P user:pass@proxy:port
-F, --user-agent

設置UserAgent，用法例如：

-F "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_4) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/55
```
