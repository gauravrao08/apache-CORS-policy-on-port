server status in apache

https://www.tecmint.com/monitor-apache-performance-using-netdata-on-centos/
```
ExtendedStatus On
<Location "/server-status">
   SetHandler server-status
   Require all granted
   Require ip 127.0.0.1
   Require ip 172.30.0.0/16
</Location>
```

```
yum install lynx
lynx http://localhost/server-status 
```
