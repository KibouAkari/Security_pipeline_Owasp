# 🔐 CI/CD Security Pipeline with OWASP ZAP & GitHub ActionsAdd commentMore actions

This project demonstrates a simple and secure CI/CD pipeline for a web application using Docker Compose and GitHub Actions. A key part of the pipeline is the integration of [OWASP ZAP](https://www.zaproxy.org/), an open-source security scanner, which automatically scans the deployed app for common vulnerabilities.

## 🧱 Project Structure

- **Web Application** – A lightweight sample app running in a container.
- **Docker Compose** – Manages the local multi-container environment.
- **GitHub Actions** – Automates build, test, and security scans.
- **OWASP ZAP** – Performs automated vulnerability scans during the CI/CD process.

## 🚀 How It Works






1. **Development**
   - The app is developed and tested locally using Docker Compose.
   - Source code is managed with Git and hosted on GitHub.

2. **CI/CD Pipeline**
   - On each `push` or `pull request`, GitHub Actions triggers a pipeline.
   - The pipeline builds the Docker containers and starts the app.
   - OWASP ZAP runs a security scan against the app endpoint.
   - A scan report is generated and stored as an artifact in the workflow.

3. **Security Scanning**
   - OWASP ZAP checks for:
     - XSS (Cross-Site Scripting)
     - SQL Injection
     - Security headers
     - Other OWASP Top 10 risks

## 📂 Folder Structure
    .
    ├── .github/workflows/ # GitHub Actions pipeline definition
    ├── docker-compose.yml # Local container setup
    ├── zap-config/ # ZAP configuration files
    ├── app/ # Web application source code
    └── README.md # Project overview


    
## 📄 Reports


- ZAP scan results are exported as HTML and attached to the GitHub Actions run.
- Reports can be downloaded directly from the GitHub Actions artifacts section.

## 🛠 Requirements

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- GitHub repository with Actions enabled
