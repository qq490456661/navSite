# 免费开源目录网站搭建
**开源免费的导航网站，目录网站，外链网站，站长目录，中文目录，站长收录，收录目录。**
*相信大家也都了解过，目前网上有非常多的目录网站，他们大多数高快审的方式来盈利。由于许多开源项目都是php语言写的，有些开源的CMS还存在很多蛋疼的漏洞，一不小心shell就没了，于是作者决定自己用java开发一个免费开源的目录网站。如果你有好的点子，可以随时联系我*
测试链接：[点我传送门](http://www.562783.com/ "免费目录网站")

## 截图预览


## 1.安装环境
JDK1.6或1.8
tomcat6或8
Mysql5.6
Nginx
Linux或windows服务器
Maven3.3

## 2.安装步骤
使用maven对源代码进行编译打包war，然后复制war到tomcat的webapps目录，启动tomcat即可。

## 3.nginx映射
然后复制网站的前端页面代码到/usr/local/www/nav_site/目录下
nginx的配置如下：
```
server {
    listen       80;
    server_name  www.562783.com;
    location / {
        root   /usr/local/www/nav_site/;
        index  index.html;
    }
}

server {
    listen          80;
    server_name     562783.com;
    rewrite ^(.*)$  http://www.$host$1 permanent;
}
```
这样子就大功告成了。项目中的模板代码在/resources/template目录下。如果需要修改模板则需要替换这里的模板页面。

# 免责声明
目前这一套模板并不能商用，只供学习使用。
如有违反法律，与本人无关。
在下载后24小时后，请及时删除。
如因本人发布的作品内容涉及版权或存在其他问题，请联系我进行删除。