# 🚀 Containerized Flask Application on AWS ECS Fargate

A simple Python Flask application containerized using Docker and deployed on AWS using Amazon ECR and Amazon ECS Fargate.

## 📌 Project Overview

This project demonstrates how to:

- Create a Python Flask application
- Containerize the application using Docker
- Build a Docker image
- Store the image in Amazon ECR
- Deploy the container on Amazon ECS Fargate
- Configure environment variables
- Access the application through a public IP

## 🏗️ Architecture

```text
User
  |
  v
Internet
  |
  v
AWS ECS Fargate
  |
  v
Docker Container
  |
  v
Flask Application

Deployment Flow
Flask Application
       ↓
     Docker
       ↓
 Amazon ECR
       ↓
 Amazon ECS
       ↓
  Fargate Task
       ↓
 Public IP
       ↓
     User
🛠️ Technologies Used
| Technology   | Purpose                      |
| ------------ | ---------------------------- |
| Python       | Application development      |
| Flask        | Web framework                |
| Docker       | Containerization             |
| Amazon ECR   | Docker image storage         |
| Amazon ECS   | Container orchestration      |
| AWS Fargate  | Serverless container compute |
| Git & GitHub | Version control              |

📂 Project Structure
project8-containerized-flask/
│
├── app.py
├── Dockerfile
├── requirements.txt
├── index.html
└── README.md
⚙️ Environment Variables
The application uses the following environment variables:
APP_ENV=production
APP_NAME=Containerized Flask Application
These variables are configured in the ECS task definition.

🐳 Docker Configuration

Build the Docker image:
docker build -t flask-app .

Run the container locally:
docker run -p 5000:5000 flask-app

The application can then be accessed at:

http://localhost:5000
📦 Amazon ECR
ECR Repository:
flask-app

AWS Region:
ap-south-1

☁️ Amazon ECS Fargate

The application is deployed using Amazon ECS with AWS Fargate.
ECS Configuration
Cluster: Flask application cluster
Task Definition: flask-app-task
Launch Type: Fargate
Operating System: Linux
Architecture: X86_64
Container Port: 5000
Protocol: TCP
Desired Tasks: 1
Environment: Production

🔐 AWS Configuration

The ECS task uses:

ecsTaskExecutionRole
Amazon ECR
Amazon ECS
AWS Fargate
Security Group
Public IP

❤️ Health Check

The application provides a health endpoint:
/health

Example response:
Example response:

🌐 Application

The deployed Flask application was successfully tested through the ECS Fargate public IP.
http://13.232.250.31:5000

Note: The public IP may change if the ECS task is stopped and a new task is started.

📊 Deployment Status
| Component             | Status         |
| --------------------- | -------------- |
| Flask Application     | ✅ Completed    |
| Docker Image          | ✅ Built        |
| Amazon ECR            | ✅ Image Pushed |
| ECS Cluster           | ✅ Created      |
| ECS Task Definition   | ✅ Created      |
| ECS Fargate Service   | ✅ Running      |
| Environment Variables | ✅ Configured   |
| Health Check          | ✅ Working      |
| GitHub Repository     | ✅ Completed    |

🎯 Project Objective
The main objective of this project is to understand how a containerized Python application can be deployed on AWS using Docker, Amazon ECR, Amazon ECS, and AWS Fargate.
👨‍💻 Author

Rahul Mohite
AWS Cloud Engineer — Aspiring
📚 Key Learning

Through this project, I learned:

Docker containerization
Docker image creation
Amazon ECR image management
Amazon ECS task definitions
ECS Fargate deployment
Environment variable configuration
AWS security group configuration
Container application testing
Git and GitHub version control


