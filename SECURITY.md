# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

蓝眼云盘（3.1.3）

## Reporting a Vulnerability

The vulnerability was discovered through the table of contents below.
1. Log in through https://tank.eyeblue.cn/user/login.

2. After login https://tank.eyeblue.cn/matter/list?page=0&pageSize=500&orderCreateTime=DESC&puuid=root&deleted=false&orderDir=DESC
Upload after accessing the site.

3. Upload the test.svg file.

4. Click File info for the uploaded test.svg.

5. After that, if you click preview and access the image address, XSS occurs.
URL: https://tank.eyeblue.cn/api/alien/preview/5a273d39-d431-4dce-46e1-d2527b28853d/test.svg

It is recommended to filter special characters when uploading files.
Alternatively, it is recommended to use only Content-Type: text/plain when previewing.

In addition, it is recommended to modify the preview so that it is possible through reliable verification that it is an image file.
https://github.com/eyebluecn/tank/blob/329751350d6534fb2d970c9093de77fad2e8b475/code/rest/alien_controller.go#L342
