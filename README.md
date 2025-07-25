# my-devops-journey
My personal DevOps learning and project journey
# Project 1: Infrastructure as Code with Terraform on AWS

This project sets up a basic ECS cluster using Terraform on AWS.

## Tools Used
- Terraform
- AWS ECS (Fargate)
- AWS VPC, Subnets, Security Groups
- GitHub for version control

## What It Does
- Creates a VPC, subnets, internet gateway
- Deploys an ECS Fargate cluster
- Runs an Nginx container using ECS service and task definition

## Folder Structure
- `main.tf` – contains all Terraform resources
- `.gitignore` – excludes .terraform and other temp files

## How to Deploy
```bash
terraform init
terraform apply

# Project 2 – CI/CD with GitHub Actions and Docker Hub

This project demonstrates a complete CI/CD pipeline setup for a simple Node.js application using GitHub Actions and Docker Hub.

---

##  Project Overview

* **App Type**: Node.js HTTP server
* **Pipeline Tool**: GitHub Actions
* **Containerization**: Docker
* **Image Hosting**: Docker Hub (`sochy01/node-ci-cd-demo`)
* **Trigger**: Push to `project-2` branch

## Project Structure
project-2-ci-cd/
│
├── .github/
│ └── workflows/
│ └── docker-build.yml # GitHub Actions CI/CD Workflow
│
├── Dockerfile # Docker container configuration
├── .dockerignore # Docker ignore file
├── index.js # Simple Node.js web server
└── package.json # Node.js metadata & dependencies

How It Works
1. GitHub Actions Workflow
Every time code is pushed to the `project-2` branch:

* The GitHub workflow is triggered.
* Docker builds the Node.js app image.
* The image is automatically pushed to [Docker Hub](https://hub.docker.com/repository/docker/sochy01/node-ci-cd-demo).

2. Docker Image

You can pull and run the image locally using:

docker pull sochy01/node-ci-cd-demo:latest
docker run -p 3000:3000 sochy01/node-ci-cd-demo

