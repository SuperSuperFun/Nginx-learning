# Nginx-learning
主要查看配置文件**nginx.conf**
### 配置了反向代理
```
  #代理web服务  
        server {
        listen       8083;
        server_name  localhost;

        #charset koi8-r;

        #access_log  logs/host.access.log;

        location / {
            root   html;
            index  index.html index.htm index.jsp;
	    proxy_pass http://127.0.0.1:9000/;
        }

        #error_page  404              /404.html;

        # redirect server error pages to the static page /50x.html
        #
        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   html;
        }
```
