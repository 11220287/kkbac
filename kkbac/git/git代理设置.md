git 克隆 github上的地址时，报错如下：

C:\Users\Administrator>git clone https://github.com/*****/****.git
Cloning into 'rest-client'...
fatal: unable to access 'https://github.com/******.git/': F
ailed to connect to github.com port 443: Timed out

原因：根本原因是本地电脑使用的公司内网，用了代理，而git没有设置
解决办法：
参考[url]https://blog.csdn.net/lizhihaoweiwei/article/details/76849755[/url]

设置全局代理
git config --global http.proxy 172.17.18.80:8080

查看是否成功
git config --get http.proxy
172.17.18.80:8080
————————————————
版权声明：本文为CSDN博主「a_haideyanlei」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/a_haideyanlei/article/details/84922833