# aws-bootcamp-week6-metabase-rds
“Metabase on ECS Fargate connected to RDS PostgreSQL | AWS Bootcamp Week 6”

# AWS Bootcamp Week 6 — Deploying Metabase on ECS Fargate with RDS PostgreSQL

This project demonstrates how I deployed **Metabase**, an open-source business intelligence platform, on **Amazon ECS** using the **Fargate** launch type and connected it to a **PostgreSQL** database hosted on **Amazon RDS**.

---

## 🎯 Objective
The objective of this exercise was to deploy and configure a containerized analytics application (Metabase) using ECS Fargate, while securely integrating it with an RDS PostgreSQL database within a shared VPC.

---

## ⚙️ Steps Completed

1. **Created an RDS PostgreSQL Database**
   - Launched an Amazon RDS instance running PostgreSQL.
   - Configured the RDS Security Group to allow inbound traffic on port **5432**.

2. **Configured Network and Security**
   - Ensured both ECS and RDS were deployed within the same VPC and subnets for private communication.
   - Updated security group rules to allow ECS tasks to connect to RDS.

3. **Created an ECS Cluster**
   - Set up an **ECS Cluster** using the **Fargate** launch type.

4. **Defined a Task Definition**
   - Used the official **Metabase Docker image** from Docker Hub.
   - Set environment variables for database connectivity:
     - `MB_DB_TYPE=postgres`
     - `MB_DB_DBNAME=<database_name>`
     - `MB_DB_PORT=5432`
     - `MB_DB_USER=<username>`
     - `MB_DB_PASS=<password>`
     - `MB_DB_HOST=<rds-endpoint>`

5. **Deployed Metabase as a Service**
   - Launched the ECS service to continuously run the Metabase container.
   - Verified communication between ECS and RDS through configured security groups.

6. **Accessed Metabase Setup**
   - Opened Metabase in the browser using the public service endpoint.
   - Successfully connected to the PostgreSQL database and completed the setup screen.

---

## 📸 Screenshots
Screenshots provided include:
- ECS Cluster with running Metabase service  
- Task Definition showing Metabase configuration  
- RDS Instance details  
- Security Group inbound rules for port 5432  
- Metabase setup screen confirming successful connection  

All screenshots are stored in the [`/screenshots`](./screenshots) folder.

---

## ✅ Outcome
Metabase was successfully deployed on **Amazon ECS Fargate** and integrated with **Amazon RDS PostgreSQL** for persistent data storage.  
This deployment showcases secure inter-service communication within AWS and highlights scalable cloud architecture principles.

---

## 🧠 Skills Demonstrated
- ECS & Fargate configuration  
- RDS database management  
- Security group and VPC networking  
- Docker image deployment  
- Application integration in AWS cloud infrastructure

---

**LinkedIn:** [www.linkedin.com/in/mpendulo-mabaso-50a1b8315](https://www.linkedin.com/in/mpendulo-mabaso-50a1b8315)  
**GitHub:** [https://github.com/zibonelemabaso-jpg](https://github.com/zibonelemabaso-jpg)
