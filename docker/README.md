## docker-compose：

  使用V2.0

  服务器环境使用docker分离redis和MySQL服务

  连接redis和MySQL请使用hostname连接

  redis hostname：redis_server port：6379

  MySQL hostname：db_server port：3306

  bbs_web_server hostname：bbs_server port:8080

  Nginx反向代 hostname：proxy port：80

## 域名规划：

  www.xysmxh.com  xysmxh.com 数模协会官网
  
  bbs.xysmxh.com  论坛
 
 
## 监控：
 
  软件：zabbix
  
  server监控端口：10051
  
  agent回传端口：10050
  
  监控web端口：8888
  
  监控模式：常规监控
  
  警报触发方式：SMTP
  
## 网络拓扑
![](https://hzlslm.org.cn/img/top.jpg)

