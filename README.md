# Student Registration App Deployment on AWS EC2

## Project Overview

This project demonstrates the deployment of a Java-based Student Registration Application on AWS using Amazon EC2 and MySQL.

The application was manually deployed by provisioning AWS infrastructure, configuring the application server, setting up the database, and connecting both layers securely.

## Architecture

```text
Users
  |
Internet
  |
EC2 Instance (Student Registration App)
  |
MySQL Database
```

## AWS Services Used

* Amazon EC2
* Security Groups
* Elastic IP
* VPC

## Technology Stack

* Java
* Spring Boot
* MySQL
* Maven
* AWS EC2
* Linux

## Project Structure

```text
student-registration-app-aws/
├── README.md
├── architecture/
├── deployment-guide/
│   └── setup.md
├── screenshots/
└── scripts/
    ├── install-java.sh
    └── install-mysql.sh
```

## Deployment Steps

### Step 1: Launch EC2 Instances

* Create Application Server EC2 Instance
* Create Database Server EC2 Instance
* Configure Security Groups
* Allow SSH access on Port 22
* Allow Application access on Port 8080

### Step 2: Install Java

```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
```

### Step 3: Install Maven

```bash
sudo apt install maven -y
```

### Step 4: Install MySQL

```bash
sudo apt update
sudo apt install mysql-server -y
```

### Step 5: Create Database

```sql
CREATE DATABASE studentapp;
```

### Step 6: Clone Application Repository

```bash
git clone https://github.com/shubhamkalsait/cloudblitz-student-app.git
```

### Step 7: Build Application

```bash
mvn clean package
```

### Step 8: Run Application

```bash
java -jar target/*.jar
```

### Step 9: Verify Deployment

Open the application in a browser using:

```text
http://<EC2-PUBLIC-IP>:8080
```

## Skills Demonstrated

* AWS EC2 Provisioning
* Linux Administration
* MySQL Installation and Configuration
* Java Application Deployment
* Security Group Configuration
* Cloud Networking Basics
* Troubleshooting and Application Setup

## Key Learnings

* Understanding multi-tier architecture
* Deploying applications on AWS EC2
* Managing Linux servers
* Configuring MySQL databases
* Connecting application and database layers securely

## Future Improvements

* Infrastructure Automation using Terraform
* Containerization using Docker
* CI/CD using Jenkins
* Kubernetes Deployment
* Monitoring using Prometheus and Grafana

## Screenshots

Screenshots are currently unavailable because the original lab environment was decommissioned. The project documentation, deployment scripts, and setup guide have been preserved for reference.
