# Amazon RDS Configuration

## Database Engine

MySQL 8.4.8

---

## Configuration

| Property       | Value         |
| -------------- | ------------- |
| DB Identifier  | wordpress-db  |
| Engine         | MySQL         |
| Version        | 8.4.8         |
| Template       | Dev/Test      |
| Instance Class | db.t3.micro   |
| Storage        | 30 GB         |
| Public Access  | No            |
| VPC            | wordpress-vpc |
| Datbase Name   | wordpress     |
| Password       | Managed by Secret Manager |
---


## Security

RDS should only accept traffic from:

wordpress-sg

Port:

3306

---

## Test Connection from ec2
```sh
sudo dnf install -y mariadb105

mysql -h endpoint of RDS -u admin -p
```