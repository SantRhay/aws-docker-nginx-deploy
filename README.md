# 🚀 Deploy Nginx with Docker on AWS EC2

## Project Overview

This project demonstrates how to deploy a containerized Nginx web server on an AWS EC2 instance using Docker.

The goal is to simulate a real DevOps deployment scenario using cloud infrastructure and containerization.

---

## Technologies Used

- AWS EC2
- Docker
- Linux
- Nginx

---

## Architecture

User → Internet → AWS EC2 → Docker Container → Nginx Web Server

---

## Implementation Steps

1. Create an EC2 instance in AWS
2. Configure Security Group to allow:
   - SSH (port 22)
   - HTTP (port 80)

3. Connect to the instance using EC2 Instance Connect

4. Install Docker

sudo yum update -y  
sudo yum install docker -y  
sudo systemctl start docker  

5. Run Nginx container

sudo docker run -d -p 80:80 nginx

6. Access the application

Open your browser and access:

http://YOUR-EC2-PUBLIC-IP

You should see the Nginx Welcome Page.

---

## Result

The Nginx container was successfully deployed on AWS EC2 and exposed to the internet.

This project demonstrates basic DevOps practices including container deployment, cloud infrastructure configuration, and networking.
