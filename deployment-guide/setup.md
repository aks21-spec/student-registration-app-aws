# Deployment Steps

## Launch EC2 Instance

- Create Ubuntu EC2 instance
- Configure Security Group
- Allow ports 22 and 8080

## Install Java

```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
```

## Install Maven

```bash
sudo apt install maven -y
```

## Clone Repository

```bash
git clone https://github.com/shubhamkalsait/cloudblitz-student-app.git
```

## Build Application

```bash
mvn clean package
```

## Run Application

```bash
java -jar target/*.jar
```
