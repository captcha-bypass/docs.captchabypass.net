# reCAPTCHA

`reCAPTCHA`最常见的版本包括以下：

+ reCAPTCHA v2
+ reCAPTCHA v2 Enterprise
+ reCAPTCHA v2 Invisible
+ reCAPTCHA v3
+ reCAPTCHA v3 Enterprise

### 如何判断我遇到的验证类型？

遇到以下挑战内容大概率是`v2`的通用版或企业版

![reCAPTCHA-001.jpg](img%2FreCAPTCHA-001.jpg ":size=20%")

![reCAPTCHA-002.jpg](img%2FreCAPTCHA-002.jpg ":size=20%")

`v2 Invisible`以及`v3`版本均为隐形验证，只能看到以下内容

![reCAPTCHA-003.jpg](img%2FreCAPTCHA-003.jpg)

[filename](header.md ':include')

#### 请求参数 <!-- {docsify-ignore} -->

| 参数      | 必须                                   | 支持版本 | 类型       | 默认值 | 描述                                                                                                                    | 
|---------|--------------------------------------|------|----------|-----|-----------------------------------------------------------------------------------------------------------------------|
| sitekey | ![yes.svg](img%2Fyes.svg ":no-zoom") |      | `String` |     | 用于调用`reCAPTCHA服务`的客户端密钥，可在调用`reCAPTCHA服务`的客户端代码中获取。                                                                   |    
| referer | ![yes.svg](img%2Fyes.svg ":no-zoom") |      | `String` |     | 触发`reCAPTCHA验证组件`的页面地址。                                                                                               |    
| size    | ![yes.svg](img%2Fyes.svg ":no-zoom") |      | `String` |     | 只有`invisible`和`normal`两种，`v3`固定为`invisible`。                                                                          |    
| title   | ![yes.svg](img%2Fyes.svg ":no-zoom") |      | `String` |     | 触发`reCAPTCHA验证组件`的页面标题，可以在控制台通过`document.title`命令获取。                                                                  |    
| action  |                                      | `v3` | `String` |     | 调用`reCAPTCHA服务`时，配置的参数。                                                                                               |    
| proxy   |                                      |      | `String` |     | 自定义代理。<br />支持http、socks5协议，如：http://proxy.com:8080 或 http://username:password:proxy.com:8080。<br />协议头可选填，不填默认为http。 |    

<!-- | ubd     |                                      |   `企业版`    | `Boolean` | `false` |                                                     |
| sa      |                                      |       | `String` |    | 极个别网站会出现的参数，一般不用填写。                                 |   
| s       |                                      | `企业版` | `String` |    |     
-->

### reCAPTCHA 通用版 :id=universal <!-- {docsify-ignore} -->

#### 请求URL <!-- {docsify-ignore} -->

POST `https://api.captchabypass.net/recaptcha/universal`

[filename](response.md ':include')

### reCAPTCHA 企业版 :id=enterprise <!-- {docsify-ignore} -->

#### 请求URL <!-- {docsify-ignore} -->

POST `https://api.captchabypass.net/recaptcha/enterprise`

[filename](response.md ':include')

