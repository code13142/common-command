## PHP 集成相关说明

### php+nginx+windows配置步骤
1. 【php官方下载地址】(https://www.php.net/downloads.php)
2. 启动php-cgi服务（注意：安装包里如果没有php-cgi.exe 还需要自己单独下载安装）
```
E:\php-8.1.10-Win32-vs16-x64\php-cgi.exe -b 127.0.0.1:9057

```
3. nginx 配置
```

location ~ \.php$ {
	     root E:/phpstomprojects/flarum-ext-auth-keycloak;
		fastcgi_pass   127.0.0.1:9057;
		fastcgi_index  index.php;
		fastcgi_param  SCRIPT_FILENAME  $document_root$fastcgi_script_name;
		include        fastcgi_params;
	}

```
