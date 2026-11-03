# AWS Flask App with RDS PostgreSQL & CloudWatch Monitoring

## Project Overview

This project demonstrates deploying a Python Flask web application on an Amazon EC2 instance, connecting it to an Amazon RDS PostgreSQL database in private subnets, and monitoring AWS resources using Amazon CloudWatch.

The project was built as part of my hands-on AWS Cloud Engineering learning journey.

## Architecture

- Amazon VPC for network isolation
- Public subnet for the EC2 instance
- Private subnets for the RDS database
- Internet Gateway for public connectivity
- EC2 hosting the Flask application
- RDS PostgreSQL for database storage
- CloudWatch dashboard and alarms for monitoring

## AWS Services Used

- Amazon EC2
- Amazon VPC
- Amazon RDS (PostgreSQL)
- Amazon CloudWatch
- Internet Gateway
- Security Groups

## Application Features

- Flask web application hosted on EC2
- PostgreSQL database connectivity
- `/` – Main application dashboard
- `/health` – Application health check
- `/db-test` – Database connection test
- Environment variables for database configuration
- Basic HTML and CSS interface

## CloudWatch Monitoring

Created a CloudWatch dashboard named `Project4-Monitoring`.

Monitored metrics include:
- EC2 CPU utilization
- EC2 network packets
- RDS CPU utilization
- RDS database connections
- RDS free storage space

Configured two CloudWatch alarms:
- EC2 CPU utilization above 70%
- RDS CPU utilization above 70%

## Security Practices

- RDS database deployed in private subnets
- Database security group allows PostgreSQL traffic only from the EC2 security group
- Database credentials stored in an environment file
- `.env` excluded from Git using `.gitignore`
- `.env.example` provided with placeholder values

)
## Project Structure

```text
project4/
├── app.py
├── requirements.txt
├── .env.example
├── .gitignore
├── templates/
│   └── index.html
└── static/
    └── style.css
```

## Project Screenshots

### 1. VPC and Subnets
![VPC and Subnets](screenshots/vpc-subnets.png)

### 2. Flask Application
![Flask Application](screenshots/flask-app.png)

### 3. RDS Database Connection
![RDS Connection](screenshots/rds-connection.png)

### 4. CloudWatch Monitoring Dashboard
![CloudWatch Dashboard](screenshots/cloudwatch-dashboard.png)

### 4. CloudWatch Monitoring Dashboard
![CloudWatch Dashboard](cloudwatch-dashboard.png)
