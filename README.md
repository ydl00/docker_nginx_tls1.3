Nginx 1.15.6 + OpenSSL 1.1.1 (支持 TLSv1.3)


# 启动
    nginx_path="/usr/local/nginx"
    docker run --name nginx_tls3 \
    -p443:443 \
    -p80:80 \
    --restart=always \
    -v ~/nginx/conf/nginx.conf:${nginx_path}/conf/nginx.conf \
    -v ~/nginx/conf/cert:${nginx_path}/conf/cert  \
    -v ~/nginx/logs/:${nginx_path}/logs \
    -d yindl/nginx_tls1.3


# 编译镜像
    docker build -t yindl/nginx_tls1.3 .

