# Security Groups

## EC2 Security Group

Name:
wordpress-sg

### Inbound Rules

| Type  | Port | Source    |
| ----- | ---- | --------- |
| SSH   | 22   | My IP     |
| HTTP  | 80   | 0.0.0.0/0 |
| HTTPS | 443  | 0.0.0.0/0 |

### Outbound Rules

Allow All

---

## RDS Security Group

Name:
wordpress-db-sg

### Inbound Rules

| Type         | Port | Source       |
| ------------ | ---- | ------------ |
| MySQL/Aurora | 3306 | wordpress-sg |

### Outbound Rules

Allow All

This configuration ensures that only the WordPress EC2 instance can connect to the database.
