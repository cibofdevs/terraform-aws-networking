# 🌐 Networking Module

[![Published on Terraform Registry](https://img.shields.io/badge/Published%20on-Terraform%20Registry-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://registry.terraform.io/modules/cibofdevs/networking/aws/latest)

Terraform module for managing **VPC** and **Subnet** infrastructure on AWS.  
Supports flexible configuration for both **public** and **private subnets**.

---

## 🚀 Features

- Create VPC with custom CIDR block
- Support multiple subnets
- Public & private subnet configuration
- Availability Zone distribution
- Simple and reusable structure

---

## 📦 Usage

```hcl
module "networking" {
  source  = "cibofdevs/networking/aws"
  version = "0.1.1"

  vpc_config = {
    cidr_block = "10.0.0.0/16"
    name       = "your_vpc_name"
  }

  subnet_config = {
    subnet_1 = {
      cidr_block = "10.0.0.0/24"
      az         = "eu-west-1a"
    }

    subnet_2 = {
      cidr_block = "10.0.1.0/24"
      public     = true
      az         = "eu-west-1b"
    }
  }
}
```
