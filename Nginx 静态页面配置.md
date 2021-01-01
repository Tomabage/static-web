当前配置
server {
  listen 80;
  server_name www.verbego.com; 
  root /www/static-web; 
  location / {
    index index.html; 
    root /www/static-web;
  } 
}

参考
server {  
    listen 80;
    server_name www.verbego.com;
    root /root/www/static-web;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}

中文文档参考
server {
 listen          80;
 server_name     www.verbego.com;
 access_log      logs/domain1.access.log main;
 location / {
 index index.html;
 root  /var/www/domain1.com/htdocs;
 }
}