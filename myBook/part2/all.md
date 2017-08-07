# 整体架构

nginx springcloud elk redis mysql

#### nginx
```
#mac 环境安装
brew install nginx
```

配置文件:/usr/local/etc/nginx/nginx.conf 
配置日志文件参考https://www.nginx.com/resources/admin-guide/logging-and-monitoring/
```
cp /usr/local/etc/nginx/nginx.conf ~/Desktop/    
cp ~/Desktop/nginx.conf /usr/local/etc/nginx/nginx.conf
#"/usr/local/Cellar/nginx/1.12.1/logs/access.log" failed
mkdir /usr/local/Cellar/nginx/1.12.1/logs
nginx -s reload

#/usr/local/var/log/nginx或上文    
```

#### ELK

> 
安装和使用    
下载安装包，修改配置文件    
启动：./bin/elasticsearch ./bin/kibana


将nginx日志通过logstash导入es
配置参考:https://qbox.io/blog/elasticsearch-logstash-kibana-manage-nginx-logs

显示地理位置
```
./bin/elasticsearch-plugin install ingest-geoip
```
使用kibana显示日志
参考http://liubenlong.github.io/2016/11/29/ELK/ELK%20%E4%B9%8B%20nginx%E6%97%A5%E5%BF%97%E5%88%86%E6%9E%90/