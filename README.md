# OA介绍
名称FSSOA , 自动办公系统，采用thinkphp5.1+mysql开发，目前已经在单位内部使用，运行很顺畅。
较适合规模比较小的公司、学校、小型企业、企事业单位等。

# 运行架构
在php5.6以上，apache,mysql5.6下配置，建议使用phpstudy,宝塔面板，wamp这样的php套件，减少配置的难度

<<<<<<< HEAD
# 配置环境
Apache下，在public目录.htaccess内容（仅供参考）

```php
<IfModule mod_rewrite.c>
Options +FollowSymlinks -Multiviews
RewriteEngine on
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^(.*)$ index.php [L,E=PATH_INFO:$1]
</IfModule>
```
nginx 环境下，nginx.conf的配置（仅供参考）
```php
server
{
    #ServerName-Start
    server_name test.com;
    #ServerName-End

    #ListenHttp-Start
    listen 80;
    listen 88;
    #ListenHttp-End

    #Index-START
    index index.php default.php index.html index.htm default.html default.htm;
    #Index-End

    location / {
        index  index.htm index.html index.php;
        #如果文件不存在则尝试TP解析
        try_files  $uri  /index.php$uri;
    }
    #Root-Start
    root D:/phpStudy_64/WWW/www.test.com/FSSCMS/public;
    #Root-End

    #SslCert-Start
    #SslCert-End

    #PhpFastCgi-Start
    location ~ \.php($|/) {
        fastcgi_pass   127.0.0.1:6473;
        fastcgi_keep_conn on;
        fastcgi_index  index.php;
        fastcgi_split_path_info ^(.+\.php)(.*)$;
        include    fastcgi_php.conf;
    }
    #PhpFastCgi-End

    #AccessLog-Start
    access_log d:/phpts/logs/nginx/access.log main;
    #AccessLog-End
}
```

# 内容模块
内部收文，外部发文，新闻，文件共享，通讯录，公告，个人日程，日常印章使用，固定资产管理，请休假管理等。
完整版本，包括以上全部；
开源版有部分模块缺失。

# 优缺点
- 缺点：跟目前市面的OA相比，FSSOA功能比较单一，无法自定义审批流程，因为是个人开发，代码相对质量不高，
代码较为臃肿，后续继续优化。

- 优点：开源，比较灵活，后续开发定制度较容易。

# 联系方式
QQ: 316 7411 308
***
Mail: pearphp@qq.com
***
欢迎大家clone，交流使用。。。 

本文本来自markdown编辑器：https://www.mdeditor.com
=======
# 包括模块
内部收文，外部发文，新闻，文件共享，通讯录，公告，个人日程，日常印章使用，固定资产管理，请休假管理。

# 联系方式
QQ: 316 7411 308
Mail: pearphp@qq.com
>>>>>>> 02799709bf20d751bd38b524652907b4779f07e5
