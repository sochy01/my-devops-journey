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
