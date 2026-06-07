# WordPress Production Deployment on AWS
### Date: 07-Jun-2026
### Author: **Htoo Eain Lin**

## Overview

This project deploys a WordPress environment on AWS using:

* Amazon VPC
* Public and Private Subnets
* Internet Gateway
* Security Groups
* Amazon EC2 (Amazon Linux 2023)
* Amazon RDS MySQL 8.4
* Apache HTTP Server
* PHP 8.x
* Let's Encrypt SSL

## Architecture
![](./wordpress-on-aws-with-2-tier-Architecture/images/wordpress-on-aws-2tier-arch.png)


## Components

| Component       | Purpose                        |
| --------------- | ------------------------------ |
| VPC             | Isolated AWS network           |
| Public Subnets  | Host internet-facing resources |
| Private Subnets | Host database resources        |
| EC2             | WordPress Web Server           |
| RDS             | Managed MySQL Database         |
| Security Groups | Network Security               |
| Route Tables    | Traffic Routing                |
| SSL Certificate | HTTPS Encryption               |

## Documentation

* docs/vpc.md
* docs/security-groups.md
* docs/ec2.md
* docs/rds.md
* docs/wordpress.md
* docs/ssl.md

## Domain

app.infrasky.online

## AWS Region

ap-southeast-1 (Singapore)

## Estimated Monthly Cost

| Service         | Cost       |
| --------------- | ---------- |
| EC2 t3.micro    | ~$8        |
| RDS db.t3.micro | ~$18.98    |
| Storage         | ~$4.14     |
| Total           | ~$31/month |

## Deployment Flow

1. Create VPC
2. Create Subnets
3. Configure Route Tables
4. Create Security Groups
5. Launch EC2
6. Create RDS
7. Install Apache/PHP
8. Deploy WordPress
9. Configure Database
10. Configure Domain
11. Install SSL
12. Complete WordPress Setup

## Output
![](./wordpress-on-aws-with-2-tier-Architecture/images/results.png)
