# secure-2tier-aws-architecture
Secure two-tier AWS architecture with Public EC2 bastion and Private MariaDB server using VPC, subnets, NAT Gateway, and security groups.
# 🚀 AWS Two-Tier Architecture: Public EC2 → Private MariaDB

![AWS](https://img.shields.io/badge/AWS-EC2%20%7C%20MariaDB-orange)

![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

![Security](https://img.shields.io/badge/Security-Private%20Subnet-blue)

## 📌 Project Overview

This project demonstrates how to securely access a MariaDB database
hosted in a private EC2 instance using a public EC2 bastion host within
an AWS VPC.

------------------------------------------------------------------------

## 🏗️ Architecture Flow

    Internet → Public EC2 (Bastion) → Private EC2 (MariaDB)

------------------------------------------------------------------------

## 🚀 Implementation Steps

### Step 1: Configuration step

![Step 1](ec2/Screenshot%202026-02-15%20223348.png)

### Step 2: Configuration step

![Step 2](ec2/Screenshot%202026-02-15%20223435.png)

### Step 3:  Configuration step

![Step 3](ec2/Screenshot%202026-02-15%20223459.png)

### Step 4:  Configuration step

![Step 4](ec2/Screenshot%202026-02-15%20223511.png)

### Step 5:  Configuration step

![Step 5](ec2/Screenshot%202026-02-15%20223522.png)

### Step 6: Configuration step

![Step 6](ec2/Screenshot%202026-02-15%20223534.png)

### Step 7:  Configuration step
![Step 7](ec2/Screenshot%202026-02-15%20223610.png)

### Step 8:  Configuration step

![Step 8](ec2/Screenshot%202026-02-15%20223710.png)

### Step 9:  Configuration step

![Step 9](ec2/Screenshot%202026-02-15%20223719.png)

### Step 10:  Configuration step

![Step 10](ec2/Screenshot%202026-02-15%20223805.png)

### Step 11: Configuration Step

![Step 11](ec2/Screenshot%202026-02-15%20223815.png)

### Step 12: Configuration Step

![Step 12](ec2/Screenshot%202026-02-15%20223837.png)

### Step 13: Configuration Step

![Step 13](ec2/Screenshot%202026-02-15%20223853.png)

### Step 14: Configuration Step

![Step 14](ec2/Screenshot%202026-02-15%20223914.png)

### Step 15: Configuration Step

![Step 15](ec2/Screenshot%202026-02-15%20224115.png)

### Step 16: Configuration Step

![Step 16](ec2/Screenshot%202026-02-15%20224131.png)

### Step 17: Configuration Step

![Step 17](ec2/Screenshot%202026-02-15%20224137.png)

### Step 18: Configuration Step

![Step 18](ec2/Screenshot%202026-02-15%20224210.png)

### Step 19: Configuration Step

![Step 19](ec2/Screenshot%202026-02-15%20224220.png)

### Step 20: Configuration Step

![Step 20](ec2/Screenshot%202026-02-15%20224244.png)

### Step 21: Configuration Step

![Step 21](ec2/Screenshot%202026-02-15%20224306.png)

### Step 22: Configuration Step

![Step 22](ec2/Screenshot%202026-02-15%20224314.png)

### Step 23: Configuration Step

![Step 23](ec2/Screenshot%202026-02-15%20224419.png)

### Step 24: Configuration Step

![Step 24](ec2/Screenshot%202026-02-15%20224540.png)

### Step 25: Configuration Step

![Step 25](ec2/Screenshot%202026-02-15%20224558.png)

### Step 26: Configuration Step

![Step 26](ec2/Screenshot%202026-02-15%20224620.png)

### Step 27: Configuration Step

![Step 27](ec2/Screenshot%202026-02-15%20225101.png)

### Step 28: Configuration Step

![Step 28](ec2/Screenshot%202026-02-15%20225213.png)

### Step 29: Configuration Step

![Step 29](ec2/Screenshot%202026-02-15%20225240.png)

### Step 30: Configuration Step

![Step 30](ec2/Screenshot%202026-02-15%20225343.png)

### Step 31: Configuration Step

![Step 31](ec2/Screenshot%202026-02-15%20225405.png)

### Step 32: Configuration Step

![Step 32](ec2/Screenshot%202026-02-15%20225555.png)

### Step 33: Configuration Step

![Step 33](ec2/Screenshot%202026-02-15%20225643.png)

### Step 34: Configuration Step

![Step 34](ec2/Screenshot%202026-02-15%20225945.png)

### Step 35: Configuration Step

![Step 35](ec2/Screenshot%202026-02-15%20230435.png)

### Step 36: Configuration Step

![Step 36](ec2/Screenshot%202026-02-15%20230719.png)

### Step 37: Configuration Step

![Step 37](ec2/Screenshot%202026-02-15%20231152.png)

### Step 38: Configuration Step

![Step 38](ec2/Screenshot%202026-02-15%20231209.png)

### Step 39: Configuration Step

![Step 39](ec2/Screenshot%202026-02-16%20140528.png)

------------------------------------------------------------------------

## 🔒 Security Best Practices

-   Database deployed in private subnet

-   Access restricted via bastion host

-   Security groups limit MySQL port (3306)

-   No direct public exposure of database

## 🎯 Result

✔ Successfully connected from public EC2 to private MariaDB instance.

## 🧑‍💻 Author

**Ravi Dhande**

---

## 🏗️ Architecture Diagram

```mermaid
flowchart LR
    A[User Browser] --> B[Public EC2 - WordPress]
    B -->|Private Network| C[Private EC2 - MariaDB]
    B --> D[Internet Gateway]
    C --> E[NAT Gateway]
    E --> D

    subgraph VPC
        B
        C
        E
    end
```

### 🔍 Architecture Explanation

- **Public Subnet:** Hosts WordPress EC2 with public access  
- **Private Subnet:** Hosts MariaDB EC2 (no public IP)  
- **Internet Gateway:** Allows inbound/outbound internet for public subnet  
- **NAT Gateway:** Allows private subnet outbound internet access only  
- **Security Groups:** Control SSH and MySQL access securely  

---
