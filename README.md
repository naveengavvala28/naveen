# AWS DevOps Project Template
This repository contains a collection of project templates designed to streamline the setup and configuration of common AWS DevOps tasks. Each template is accompanied by detailed instructions and scripts to help you quickly deploy and configure essential components on the AWS cloud platform.

# Project-1: AWS EC2 Instance Setup with RDS Integration
Description: This project template guides you through the process of setting up an Amazon EC2 instance running Amazon Linux 2, launching an RDS cluster, and configuring the EC2 instance to connect to the RDS database. It includes steps to install required dependencies, set up the Apache HTTP server, PHP, and MySQL client, and mount an Elastic File System (EFS) to the instance for persistent storage. Additionally, it demonstrates how to create an Application Load Balancer (ALB), configure an Auto Scaling Group (ASG), and implement health checks and alarms for the EC2 instances.

# Features:

 - Launch an EC2 instance and an RDS cluster
 - Configure EC2 to connect to RDS
 - Set up Apache HTTP server with PHP and MySQL
 - Mount an EFS for persistent storage
 - Create an ALB and ASG for scalability
 - Implement health checks and alarms for EC2 instances

Usage:

# Follow the step-by-step instructions provided in the project template.
- Execute the provided scripts and commands on your AWS console or through AWS CLI.
- Access the deployed application using the ALB endpoint and test functionality.
- Note: This template serves as a foundational guide for deploying web applications on AWS infrastructure, ensuring scalability, reliability, and efficient resource management.


# Detailed Implementation Steps
Follow these step-by-step instructions to implement the AWS DevOps project using the provided commands:

# Launch an EC2 Instance and an RDS Cluster:

- Use the AWS Management Console or AWS CLI to launch an EC2 instance running Amazon Linux 2 and an RDS cluster.
- Command: ``` aws ec2 run-instances (for launching EC2), aws rds create-db-cluster ``` (for creating RDS cluster).
- Description: These commands provision the necessary resources on AWS, including EC2 instances and RDS clusters, as specified in the provided commands.

# Configure EC2 to Connect to RDS:

- Install necessary packages on the EC2 instance, such as Apache HTTP server, PHP, and MySQL client.
- Mount an Elastic File System (EFS) to the EC2 instance for persistent storage.
- Command: ``` sudo yum install httpd -y, sudo yum install -y mysql, sudo amazon-linux-extras install -y lamp-mariadb10.2-php7.2 php7.2.```
- Description: These commands install and configure the required software packages on the EC2 instance, ensuring it can communicate with the RDS cluster and serve web content.

# Create an Application Load Balancer (ALB) and Auto Scaling Group (ASG):

- Use the AWS Management Console or AWS CLI to create an ALB and ASG.
- Configure health checks and alarms for the EC2 instances to ensure high availability.
- Command: ``` aws elbv2 create-load-balancer, aws autoscaling create-auto-scaling-group.```
- Description: These commands set up the infrastructure for load balancing and scaling, ensuring the application can handle varying levels of traffic and maintain performance.

# Access and Test the Deployed Application:

- Access the application using the ALB endpoint and test its functionality by submitting data through the web interface.
- Verify data storage in the MySQL database by connecting to the RDS cluster and executing SQL queries.
- Command: ```mysql -h <RDS_ENDPOINT> -P 3306 -u <USERNAME> -p.```
- Description: This step ensures that the deployed application is functioning correctly and data is being stored and retrieved from the database as expected.
