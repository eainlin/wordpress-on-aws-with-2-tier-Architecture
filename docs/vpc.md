# VPC Configuration

## VPC

| Name          | CIDR        |
| ------------- | ----------- |
| wordpress-vpc | 10.0.0.0/16 |

---

## Public Subnets

| Name                       | CIDR        |
| -------------------------- | ----------- |
| wordpress-public-subnet-01 | 10.0.0.0/24 |
| wordpress-public-subnet-02 | 10.0.1.0/24 |

Enable Auto Assign Public IPv4 Address

---

## Private Subnets

| Name                        | CIDR        |
| --------------------------- | ----------- |
| wordpress-private-subnet-01 | 10.0.2.0/24 |
| wordpress-private-subnet-02 | 10.0.3.0/24 |

---

## Internet Gateway

Name:
wordpress-igw

Attach to:

wordpress-vpc

---

## Public Route Table

Name:
wordpress-pub-rt

Routes:

Destination: 0.0.0.0/0
Target: wordpress-igw

Associated Subnets:

* wordpress-public-subnet-01
* wordpress-public-subnet-02

---

## Private Route Table

Name:
wordpress-private-rt

Associated Subnets:

* wordpress-private-subnet-01
* wordpress-private-subnet-02
