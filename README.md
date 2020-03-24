# vesta-cp-nginx-force-https
VestaCP's template forcing HTTPS on VestaCP &amp; Nginx &amp; PHP-FPM stack

---
Tested on Ubuntu 18.04.2 LTS.

This template is modification of default Vesta's templates:
```sh
/usr/local/vesta/data/templates/web/nginx/php-fpm/default.tpl
/usr/local/vesta/data/templates/web/nginx/php-fpm/default.stpl
```
and is **only** valid for stack: **VestaCP + Nginx + PHP-FPM**

Template redirect any HTTP requests (to domain and its aliases) to HTTPS:
```sh
http://domain.com          -->   https://domain.com
http://www.domain.com      -->   https://domain.com
http://alias.domain.com    -->   https://domain.com
```

### Usage example
Place `force-https.tpl` and `force-https.stpl` in `/usr/local/vesta/data/templates/web/nginx/php-fpm`.

or

```sh
cd /usr/local/vesta/data/templates/web/nginx/php-fpm
wget -O vesta-cp-nginx-force-https-master.zip https://github.com/lookasc/vesta-cp-nginx-force-https/archive/master.zip
unzip vesta-cp-nginx-force-https-master.zip
cp ./vesta-cp-nginx-force-https-master/force-https.* ./
rm -r ./vesta-cp-nginx-force-https-master*
```
