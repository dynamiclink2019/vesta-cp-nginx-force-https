# vesta-cp-nginx-force-https
VestaCP's template forcing HTTPS on VestaCP &amp; Nginx &amp; PHP-FPM stack

---

This template is modification of default Vesta's template:
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
git clone git@github.com:lookasc/vesta-cp-nginx-force-https.git
cp ./vesta-cp-nginx-force-https/force-https* ./
rm -r ./vesta-cp-nginx-force-https
```
