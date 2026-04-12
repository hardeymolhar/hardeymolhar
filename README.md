# Hello, I’m Emmanuel 

**On Prem & Cloud Database Administrator** with proven experience supporting mission-critical **SQL Server and Oracle** systems in a top-tier Nigerian bank, across  on-prem and Azure environments.I build and maintain the systems that keep data running—secure, available, and efficient. By combining cloud, infrastructure, and automation, I help ensure everything works reliably behind the scenes.


## 🚀 Featured Database Engineering Projects

### 1. Cosmos DB Batch Ingestion Demo

Built a practical test environment to understand how Azure Cosmos DB handles high-volume data ingestion and how to optimize performance and cost.

This project simulates real-world scenarios where large amounts of data need to be written efficiently, helping identify how throughput (RU/s) and system behavior change under load.

#### What I Focused On

- Monitoring how request units (RU) are consumed during heavy data ingestion  
- Testing batch ingestion patterns to improve performance and reduce cost  
- Using Terraform to provision infrastructure in a consistent and repeatable way  
- Using Ansible to configure virtual machines and standardize the environment 

#### Repository

→ [View CosmosDB Project](https://github.com/hardeymolhar/azure-data-platform)
---

#### 🏗 System Architecture
```mermaid
flowchart LR
Terraform --> Azure_VM
Azure_VM --> Ansible
Ansible --> DotNet_App
DotNet_App --> CosmosDB
CosmosDB --> Metrics
```



### 2. Secure Azure SQL PaaS with Cross-Region High Availability (In Progress)

Designed a secure and highly available Azure SQL environment to address common risks in banking and fintech systems, including downtime, data loss, and public exposure.

This project focuses on building a reliable database platform that can continue operating during failures while keeping data secure and accessible.

#### What I Focused On

- Designing for high availability using cross-region failover and data replication  
-  Using Terraform to provision infrastructure in a consistent and repeatable way   
- Securing database access using private endpoints instead of public exposure  
- Implementing encryption using customer-managed keys stored in Azure Key Vault  
- Choosing controlled connectivity (proxy mode) to align with strict enterprise network environments  

#### Repository

→ [View Azure SQL Project](https://github.com/hardeymolhar/azure-sql-automated-infrastructure)
---

## 🏗️ System Architecture

``` mermaid
flowchart LR

    subgraph Client Layer
        P[Python Workload Simulator]
    end

    subgraph Network Layer
        PE_SQL[Private Endpoint SQL]
        PE_KV[Private Endpoint Key Vault]
    end

    subgraph Security Layer
        KV[Key Vault]
    end

    subgraph Primary Region
        FG[Failover Group Endpoint]
        SQLP[SQL Primary]
    end

    subgraph Secondary Region
        SQLS[SQL Secondary]
    end

    subgraph Observability
        AM[Azure Monitor]
        LA[Log Analytics Workspace]
        WB[Workbooks and Alerts]
    end

    P --> PE_SQL
    P --> PE_KV

    PE_SQL --> FG
    FG --> SQLP
    SQLP -->|Geo Replication| SQLS

    SQLP -->|CMK| KV
    PE_KV --> KV

    P --> AM
    SQLP --> AM
    SQLS --> AM
    KV --> AM

    AM --> LA
    LA --> WB

```

## 🧰 Tech Stack

Databases & DBA Tools

![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![SSMS](https://img.shields.io/badge/SSMS-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle_DB-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![Toad for Oracle](https://img.shields.io/badge/Toad_for_Oracle-2E7EEA?style=for-the-badge)



Cloud, OS & Automation

![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white)
![Linux](https://img.shields.io/badge/Linux_Shell-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
