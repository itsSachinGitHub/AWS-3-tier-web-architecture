# AWS Three-Tier Web Architecture

## Description: 
This is a three-tier web architecture in AWS. I have manually created the necessary network, security, app, and database components and configurations to run this architecture in an available and scalable manner. Some foundational AWS knowledge around VPC, EC2, RDS, S3, ELB, and the AWS Console.  

## Architecture Overview
![Architecture Diagram](https://github.com/itsSachinGitHub/AWS-3-tier-web-architecture/blob/main/Screenshot%202024-07-30%20150959.png)

A public-facing Application Load Balancer forwards client traffic to our web-tier EC2 instances in this architecture. The web tier is running Nginx web servers that are configured to serve a React.js website and redirect our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks, and autoscaling groups are created at each layer to maintain the availability of this architecture.
