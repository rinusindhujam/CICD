# CICD
CICD Challenge 3
XOps Microchallenge #3 – CI/CD Pipeline to EC2
This repository contains a simple web app that is deployed automatically to an AWS EC2 instance using GitHub Actions.

Project Structure
index.html — Simple HTML page deployed on EC2's NGINX web server.
.github/workflows/deploy.yml — GitHub Actions workflow to automate deployment.
How it works
You push code changes to the main branch on GitHub.
GitHub Actions workflow triggers, connects to the EC2 instance via SSH.
It copies the latest code to the EC2 server.
It restarts the web server (NGINX) to reflect the new changes.
The updated website is available at your EC2 instance’s public IP.
Setup
Create an EC2 instance (Ubuntu 22.04) with NGINX installed.
Open ports 22 (SSH) and 80 (HTTP) in the Security Group.
Add GitHub Secrets:
EC2_PUBLIC_IP — Your EC2 instance’s public IP.
SSH_USERNAME — Usually ubuntu for Ubuntu instances.
SSH_PRIVATE_KEY — Contents of your .pem file.
Notes
Remember to terminate your EC2 instance after testing to avoid charges.
Keep your SSH private key secure; do not share publicly.
