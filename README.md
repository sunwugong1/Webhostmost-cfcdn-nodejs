
两款永久免费web主机，轻松搭建节点，可优选ip加速，无限流量，是serv00节点功能的最佳平替！
饭奇骏
2025-05-10
2025-05-11

两款永久免费Web主机介绍
欢迎来到我的博客！今天我将为大家介绍两款永久免费的Web主机服务，分别是 Webhostmost 和 Webfreecloud。这两款服务都非常适合轻量级项目或节点搭建，尽管它们各有优缺点。以下是详细的使用指南和对比分析。

注册地址
webhostmost虚拟机，用谷歌帐号直接登录就不用每45天继期一次

https://www.webhostmost.com/free-web-hosting

webfreecloud虚拟机

https://web.freecloud.ltd/

Webhostmost：无限流量的免费Web主机
特点
永久免费：无广告，数据安全，提供无限SSL证书。
磁盘空间：125MB，适合小型项目或节点。
高可用性：99.9%的正常运行时间，良好的安全性和速度。
注册与设置步骤
注册账号：

访问注册页面，选择一个国家（不建议日本）。
输入一个域名（不需要归属验证，但不能是二级域名，系统会检查是否已被占用）。
填写个人信息，可以使用真实信息或通过身份生成器生成虚拟信息（邮箱需真实）。
选择服务器所在地（如日本），勾选条款并点击“Checkout”。
邮箱验证：

注册后会收到一封确认邮件，点击链接完成邮箱验证。

域名设置：
复制服务器IP地址。
在域名管理页面添加DNS记录，设置子域名并绑定IP。
启用IP代理状态并保存。
将系统中的默认域名更改为自定义域名，等待设置生效。

安装节点：
将界面语言切换为中文（可选）。
打开开发工具中的终端，进入项目目录。 搭建节点项目: node-ws

https://github.com/frankiejun/node-ws

使用提供的安装命令，将域名替换为自定义域名后执行。例如

curl -Ls https://raw.githubusercontent.com/frankiejun/node-ws/refs/heads/main/setup.sh | bash -s yourdomain

curl -Ls https://raw.githubusercontent.com/frankiejun/node-ws/refs/heads/main/setup.sh | bash -s webhost.cfjs.dpdns.org

也可以本地把index.js和package.json这两个文件上传至域名根目录
在index.js里的第9行修改UUID和第13行修改成你所绑定服务器的域名，把第17行的3000端口修改为没用过的端口如31262


配置Node.js应用：

进入“Website管理”页面，选择“Node.js App”，创建新应用。

Node.js version➡20.18.1
Node.js 版本 20.18.1

Application root➡domains/xxx.xxxx.com/public_html (替换自己的完整域名)切记不要填写错误
应用程序根，例如domains/webhost.cfjs.dpdns.org/public_html

Application startup file➡index.js
应用程序启动文件 index.js

添加环境变量（如UUID），若仅搭建节点则无需额外探针配置。
点击“创建”完成应用部署。

输入子域名（如sub.你的域名），获取节点链接。
将链接导入到V2Ray客户端，测试延迟和速度。
如果节点不通，可访问你的域名/SUB激活后再测试。

测试结果
延迟：节点连接稳定，延迟正常。
速度：作为免费无限流量节点，速度表现不错，可作为serv00的替代品（仅限节点功能）。
如果服务器绑定的是托管到cloudflare的域名并打开小云朵，那么所生成的节点可以通过优选ip来加速科学上网


Webfreecloud：轻量级免费Web主机
特点
系统相似：与Webhostmost几乎相同的系统界面和操作流程。
磁盘空间：仅64MB，适合极小型项目。
带宽限制：每月200GB流量，需手动续约。
续约要求：
加入官方Telegram群，最早可提前7天续约。
在“产品服务”页面查看详情，刷新后生成0元账单，手动支付完成续期。
网速：相较Webhostmost稍慢，且有流量限制。
注册与节点安装
注册流程：与Webhostmost完全一致，参考上述步骤。
节点安装：操作与Webhostmost相同，无需额外演示。
注意事项：每月需主动续约，否则服务会中断。
对比分析
特性	Webhostmost	Webfreecloud
磁盘空间	125MB	64MB
流量	无限	200GB/月
续约	无需续约	每月手动续约
网速	较快	稍慢
节点支持	支持，稳定	支持，但受限于流量和速度
其他功能	99.9% uptime，无广告，SSL证书	类似功能，但需续约
搭建节点项目
node-ws

总结
Webhostmost 适合需要无限流量和长期稳定节点的场景，尽管磁盘空间有限，但性能和易用性较优。
Webfreecloud 更适合短期或轻量项目，但每月续约和流量限制可能带来不便。
如果你需要一个完全免费且无需频繁维护的节点，Webhostmost是更好的选择；若磁盘空间需求极小且能接受续约操作，Webfreecloud也可考虑。
希望这篇博文对你有帮助！如果喜欢，请点赞并关注我的博客，更多实用教程等你探索！下期再见！

Webhostmost帐号保活

github保活项目地址

https://github.com/banfeng-git/webhost

转到你 fork 的仓库页面。

点击 Settings，然后在左侧菜单中选择 Secrets。

添加以下变量：

名称: WEBHOST
 
值: 邮箱号:密码

如rg5201@outlook.com:Huagongzi1@
