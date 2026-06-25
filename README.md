# Student Registration App Deployment on AWS EC2

## Project Overview

This project demonstrates the deployment of a Java-based Student Management Application on AWS using Amazon EC2 and MySQL.

The application was manually deployed by provisioning AWS infrastructure, configuring the application server, setting up the database, and connecting both layers securely.

## Architecture

```text
Internet
    |
Application EC2
    |
MySQL EC2
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

## Deployment Steps

### Launch EC2 Instances

* Application Server EC2
* Database Server EC2

### Install Java

```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
```

### Install MySQL

```bash
sudo apt update
sudo apt install mysql-server -y
```

### Create Database

```sql
CREATE DATABASE studentapp;
```

### Clone Repository

```bash
git clone https://github.com/shubhamkalsait/cloudblitz-student-app.git
```

### Build Application

```bash
mvn clean package
```

### Run Application

```bash
java -jar target/*.jar
```

## Key Learnings

* AWS EC2 provisioning
* Linux administration
* MySQL configuration
* Java application deployment
* Security Group management

## Future Improvements

* Terraform automation
* Docker containerization
* Jenkins CI/CD
* Kubernetes deployment
* Monitoring with Prometheus and Grafana
