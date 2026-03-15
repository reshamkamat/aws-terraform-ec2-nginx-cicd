# AWS Terraform EC2 Nginx CI/CD Pipeline

This project demonstrates how to deploy a static website on AWS EC2 using Terraform and automate the deployment using GitHub Actions CI/CD.

The website is hosted on an EC2 instance running Nginx and automatically updates whenever code is pushed to GitHub.

---

## Architecture

Developer → GitHub → GitHub Actions → EC2 → Nginx → Website

---

## Technologies Used

- AWS EC2
- Terraform
- Nginx
- GitHub Actions
- Linux
- Git

---

## Infrastructure as Code

Terraform is used to provision the AWS infrastructure.

Files used:

provider.tf  
main.tf  
variables.tf  
outputs.tf  

These files create and configure the EC2 instance where the website will run.

---

## CI/CD Pipeline

GitHub Actions automatically deploys the website when code is pushed to the repository.

Pipeline workflow:

1. Code pushed to GitHub
2. GitHub Actions pipeline triggers
3. Workflow connects to EC2 using SSH
4. Website files copied to Nginx directory
5. Nginx restarts and website updates automatically

Workflow file location:

.github/workflows/deploy.yml

---

## Screenshots

### GitHub Actions CI/CD Pipeline

![CI/CD Pipeline](screenshots/pipeline.png)

### Deployment Logs

![Deployment Logs](screenshots/deploy.png)

### Live Website

![Website](screenshots/website.png)

---

## Project Highlights

- Infrastructure provisioning using Terraform
- Automated deployment using GitHub Actions
- Secure SSH connection using GitHub Secrets
- Static website hosted using Nginx
- Fully automated CI/CD pipeline

---

## Author

Resham Kamat

GitHub: https://github.com/reshamkamat
