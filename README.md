# Continuous Deployment Pipeline using Jenkins, Docker, Amazon ECR & Amazon ECS

## Overview

This repository demonstrates a **Continuous Deployment (CD) pipeline** for automating the delivery of containerized applications to AWS. After the **Continuous Integration (CI)** process, the pipeline moves into **CD**, where the application is packaged, stored, and deployed automatically to the cloud.

---

## 🚀 CD Pipeline Flow

1. **Docker Build & Packaging**

    - After code passes quality checks:
        - A `Dockerfile` is used to define the container image.
        - Docker builds the image.
        - Image is tagged (semantic versioning or commit ID).
    - **Why this matters:**
        - Ensures consistent runtime across all environments.
        - Removes OS and configuration dependencies for apps.

2. **Push Docker Image to Amazon ECR**

    - The Docker image is pushed to Amazon Elastic Container Registry (ECR).
    - **Key Actions:**
        - Authenticate Jenkins with ECR.
        - Tag the Docker image.
        - Push to the ECR repository.
    - **Benefits:**
        - Highly secure storage for images.
        - Version-controlled repository.
        - Seamless integration with ECS.

3. **Deploy to Amazon ECS**

    - Jenkins triggers an ECS deployment when the image is in ECR.
    - ECS pulls the latest image from ECR.
    - The ECS service updates its task definition.
    - ECS performs a rolling update with zero downtime.
    - **ECS Advantages:**
        - Auto-healing of unhealthy tasks.
        - Horizontal scaling.
        - High availability across Availability Zones.

---

## 🧠 Tools Used (CD Phase)

| Tool         | Purpose                              |
|--------------|--------------------------------------|
| Docker       | Containerizes the application        |
| Amazon ECR   | Secure storage for Docker images     |
| Amazon ECS   | Runs the application as containers   |
| Jenkins      | Automates the CI/CD workflow         |

---

## 🧱 Deployment Workflow

A high-level breakdown of the end-to-end flow:

1. Developer pushes code to GitHub.
2. Jenkins fetches the source code.
3. **CI**: Build → Test → Code Analysis → Artifact Upload.
4. **CD:**
    - Build Docker image.
    - Push image to Amazon ECR.
    - Update ECS to run the new version.

---

## 🖼️ CD Architecture Diagram

Visualize the flow: **GitHub → Jenkins → Docker → ECR → ECS**  
_Refer to the architecture diagram in this repository for details._

---

## ✨ Key Benefits

- 🚀 **Fast & automated deployments**
- 🔁 **Zero downtime** via rolling updates
- 📦 **Consistent & portable containers**
- 🔒 **Secure image management** with ECR
- 📈 **Scalable deployments** via ECS services

---

## 🧰 Prerequisites

Ensure the following are configured before running the CD workflow:

- AWS CLI with necessary IAM permissions
- Docker installed on Jenkins agent(s)
- Amazon ECR repository set up
- ECS Cluster and ECS Service configured
- Jenkins credentials for AWS access

---

## 💡 Future Enhancements

- Automate infrastructure using **Terraform**
- Migrate ECS tasks to **AWS Fargate** (serverless containers)
- Implement **Blue/Green Deployments** (CodeDeploy)
- Add **Prometheus & Grafana** for advanced monitoring

---

## 👨‍💻 Author

**Giri**  
DevOps Engineer | CI/CD | AWS Cloud  
📍 India  

_Project: CI/CD with Jenkins, SonarQube, Docker, ECR & ECS_
