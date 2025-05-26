## 一、Webhostmost在Node.js环境搭建vless-ws-tls脚本

先在本地编辑app.js文件里面的三个环境变量

UUID：你的uuid，在第53行

PORT：服务器可使用的端口，在第56行

DOMAIN：已解析在CF的域名，在第59行

Webhostmost新/老账户，建议使用外部节点保活方式，可以在CF-workers进行部属保活

节点保活及节点信息地址：https://你已解析在CF的域名/你的uuid

账户需要保活吗？请注意：Webhostmost免费账户需要每45天登录一次网页界面，过期会删除数据，请留意！如果直接用谷歌账号登录，应该不用保活

-----------------------------------------------------
二、在面板点击左栏 Website Management➡NodeJs APP➡Create application➡CREATE先看图
现在需要付费才能用，但可以把进入“Node.js App”的地址更改一下就可以进入“Node.js App”，免费创建新应用。例入点击“Node.js App”后的地址是这样的:
https://server6.webhostmost.com:2222/evo/user/plugins/access_router?path=nodejs.raw
把上面的地址修改成以下址即可

https://server6.webhostmost.com:2222/evo/user/plugins/nodejs_selector#/

也就是说在地址的plugins/后面的替换成nodejs_selector#/即可进入“Node.js App”，免费创建新应用。

Node.js version➡22.13.0
Node.js 版本 22.13.0

Application root➡domains/xxx.xxxx.com/public_html (替换自己的完整域名)切记不要填写错误
应用程序根，例如domains/vmq.mqyzf.dedyn.io/public_html

Application startup file➡app.js
应用程序启动文件 app.js

此时创建完成 Node.js 应用后往下翻点击Run NPM install等待执行完毕

等待完毕后点击 Run JS script弹出界面后点击start再点击Run JS script即可

这时输入`你的域名/UUID`即可获取节点信息

如果访问是503请更换端口或检查有无错误换端口请重新点击Run JS script
编辑创建端口时，建议10000-65000之间随便取个数字

这个节点支持优选ip，在域名解析ip时必须打开小云朵才生效