# Automated CI/CD Pipeline for Dockerized Web Application (AWS ECS Fargate)

## Overview
This project is a Dockerized Node.js (Express) web application deployed to AWS ECS Fargate behind an Application Load Balancer.
A CI/CD pipeline using GitHub Actions automatically builds and deploys the application on every push to the main branch.

## Tech Stack
- Node.js + Express
- Docker
- AWS Copilot (ECS Fargate, ECR, ALB, CloudWatch Logs)
- GitHub Actions (CI/CD)

## Endpoints
- `/` : Home route
- `/health` : Health check route used by the load balancer

## How CI/CD Works
1. Developer pushes code to the `main` branch on GitHub
2. GitHub Actions builds a Docker image
3. The image is pushed to Amazon ECR
4. AWS ECS service redeploys and serves the new version via Load Balancer URL
