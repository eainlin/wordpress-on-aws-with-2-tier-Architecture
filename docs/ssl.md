# SSL Configuration

## Install Certbot

```sh
sudo dnf install -y certbot python3-certbot-apache

```
---

## Generate SSL Certificate
```sh
sudo certbot --apache -d example.com
```
---

## Verify

https://example.com

---

## Auto Renewal Test

sudo certbot renew --dry-run
