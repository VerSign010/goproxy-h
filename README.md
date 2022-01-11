## goproxy-heroku

### Heroku 是一个支持多种编程语言的云平台即服务，goproxy-heroku 则是可部署在 Heroku 平台的 goproxy 服务。goproxy-heroku 使用的 WebSocket 代替原本的 sockets 作为底层传输。


## 部署方法

一、在heroku上的部署

1、登陆heroku https://dashboard.heroku.com/login

2、登陆好后，点击

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/fgdx/goproxy-heroku)

3、执行以下四个步骤，见下图：

（1）App name: 输入App名字

（2）Choose a region: 选择一个地区.例如United States或Europe

（3）PASSWORD: 输入密码，可用大小写字母+数字，建议30位以上

（4）点击部署app: Deploy app

<img src="/doc/1.png" width="500px" height="auto">

4、执行完成以后，这是就完成了部署。

<img src="/doc/2.png" width="400px" height="auto">

点View <img src="/doc/111.png" width="80px" height="auto">,把地址栏中的账号复制下来。

二、在客户端上执行

`proxy.exe http -t tcp -p :1080 -T wss -P xxx.herokuapp.com:443 --parent-ws-password goproxy123456 -q 8.8.8.8:53 --timeout 30000`

或者用批处理脚本proxy-heroku.bat生成客户端配置文件。



goproxy使用文档参考：https://snail007.github.io/goproxy/posts/http_cdn_ws/
