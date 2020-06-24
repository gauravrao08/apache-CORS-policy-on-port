# apache-CORS-policy-on-port
apache CORS policy on port

vim /etc/httpd/conf/httpd.conf 

http://IP:8081/server-status

```
<IfModule mod_status.c>
#
# Allow server status reports generated by mod_status,
# with the URL of http://servername/server-status
# Uncomment and change the ".example.com" to allow
# access from other hosts.
#

Listen 8081
ExtendedStatus On
<VirtualHost *:8081>
    <Location /server-status>
        SetHandler server-status
        #Order deny,allow
        Require all granted
        #Deny from all
        Allow from all
        #Allow from .example.com
        #Require  host IP
    </Location>
</VirtualHost>
</IfModule>

```
