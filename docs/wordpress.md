# WordPress Installation

## Download WordPress

```sh
cd /var/www/html

sudo wget https://wordpress.org/latest.tar.gz

sudo tar -xzf latest.tar.gz

sudo mv wordpress/* .

sudo rm -rf wordpress latest.tar.gz
```

---

## Configure Permissions
```sh

sudo chown -R ec2-user:apache /var/www/html

sudo chmod 2775 /var/www/html

find /var/www/html -type d -exec sudo chmod 2775 {} ;

find /var/www/html -type f -exec sudo chmod 0664 {} ;
```

---

## SELinux Configuration
```sh

sudo setsebool -P httpd_can_network_connect_db 1

sudo setsebool -P httpd_can_sendmail 1

sudo chcon -R -t httpd_sys_content_t /var/www/html

sudo chcon -R -t httpd_sys_rw_content_t /var/www/html/wp-content
```

---

## Configure WordPress
```sh

cp wp-config-sample.php wp-config.php

Edit:

sudo nano wp-config.php

Update:

define('DB_NAME', 'wordpress');
define('DB_USER', 'admin');
define('DB_PASSWORD', 'YOUR_PASSWORD');
define('DB_HOST', 'endpoint of RDS');
```
