
Apache Web Server, PHP Engine, Apache Proxy modules and IP2Location module
--------------------------------  

Apache Web Server and PHP Engine from *apache-php* image  
https://github.com/fabio-particles/apache-php

Apache Proxy modules from *apache-php-proxy* image  
https://github.com/fabio-particles/apache-php-proxy

**IP2Location module**  
Requires BIN file with GEO-IP information:  
https://www.ip2location.com/  

**Test files with sample BIN included**  
copy example ip2location folder which includes php scripts and a sample database in BIN format

    cp -r ip2location /app/apache2/www

Check IP geographical information:  
http://hostname-ip/ip2location/example.php

Issues with IP2Location?
Check if IP2Location module is loaded:

    docker exec apache /usr/sbin/apachectl -t -D DUMP_MODULES | grep IP2Location

> Written with [StackEdit](https://stackedit.io/).