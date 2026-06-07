# EC2 Configuration
### Date: 07-Jun-2026
## Instance Details

| Property       | Value                |
| -------------- | -------------------- |
| Name           | WordPress-Production |
| AMI            | Amazon Linux 2023    |
| Instance Type  | t3.micro             |
| Storage        | 10 GB                |
| Security Group | wordpress-sg         |
| Key Pair       | wordpress-aws-key    |

---

## IAM Role

Role Name:

ec2-ssm-role

Policy:

AmazonSSMManagedInstanceCore

---

## Connect via SSH

chmod 400 wordpress-aws-key.pem

ssh -i wordpress-aws-key.pem ec2-user@PUBLIC_IP

---

## Update System

sudo dnf update -y

---

## Install Apache

sudo dnf install httpd -y

sudo systemctl enable --now httpd

---

## Install PHP

sudo dnf install -y php php-mysqli php-fpm php-xml php-mbstring php-json php-cli php-gd php-intl php-zip

sudo systemctl enable --now php-fpm

---

## Verify Installation

php -v

httpd -v
