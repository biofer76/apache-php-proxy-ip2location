
Apache Web Server, PHP Engine, Apache Proxy modules and IP2Location module
--------------------------------  

Apache Web Server and PHP Engine from *apache-php* image  
https://github.com/fabio-particles/apache-php

Apache Proxy modules from *apache-php-proxy* image  
https://github.com/fabio-particles/apache-php-proxy

**IP2Location module**  
IP2Location™ is a non-intrusive geo IP solution to help you to identify visitor's geographical location, i.e. country, region, city, latitude & longitude of city, ZIP code, time zone, connection speed, ISP, domain name, IDD country code, area code, weather station code and name, mobile carrier, elevation and usage type information using a proprietary IP address lookup database and technology without invading the Internet user's privacy.

**Requires BIN** file with GEO-IP information:  
https://www.ip2location.com/  

**Test files with sample BIN included**  
copy example ip2location folder which includes php scripts and a sample BIN database in document root

    cp -r ip2location /app/apache2/www

Check IP geographical information:  
http://hostname-ip/ip2location/example.php

**Issues with IP2Location?**  
Check if IP2Location module is loaded:

    docker exec apache /usr/sbin/apachectl -t -D DUMP_MODULES | grep IP2Location

> Written with [StackEdit](https://stackedit.io/).