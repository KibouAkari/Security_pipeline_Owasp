# 🔐 CI/CD Security Pipeline with OWASP ZAP & GitHub Actions

This project demonstrates a secure and automated CI/CD pipeline for scanning a vulnerable web application using Docker Compose and GitHub Actions. A key part of the pipeline is the integration of [OWASP ZAP](https://www.zaproxy.org/), an open-source security scanner, which automatically scans the deployed app for common vulnerabilities.

## 🧱 Project Structure

- **OWASP Juice Shop** – A deliberately insecure web application used for security testing.
- **Docker Compose** – Manages the multi-container environment for Juice Shop and ZAP.
- **GitHub Actions** – Automates testing and security scans on every push or pull request.
- **OWASP ZAP** – Performs automated vulnerability scans during the CI/CD process.

## 🚀 How It Works

1. **Development**
   - The app is deployed automatically via GitHub Actions.
   - Source code is managed with Git and hosted on GitHub.

2. **CI/CD Pipeline**
   - On each push or pull request, GitHub Actions triggers two workflows:
      - cicd.yml: Runs basic Python tests and linting.
      - zap_scan.yaml: Starts Juice Shop and ZAP via Docker Compose and performs a security scan.
   - OWASP ZAP scans the Juice Shop instance at http://juice-shop:3000.
   - Scan reports are generated and stored as a zip folder under GitHub Actions artifacts.

3. **Security Scanning**
   - OWASP ZAP checks for:
     - XSS (Cross-Site Scripting)
     - SQL Injection
     - Security headers
     - Other OWASP Top 10 risks

## 📂 Folder Structure
      .
      ├── .github/workflows/     # GitHub Actions pipeline definitions
      │   ├── cicd.yml           # Linting and placeholder test
      │   └── zap_scan.yaml      # Security scan with OWASP ZAP
      ├── docker-compose.yml     # Local container setup for Juice Shop and ZAP
      ├── zap/                   # Folder for storing scan reports
      │   └── reports/
      ├── zap-config/            # ZAP configuration files (e.g., auth.context)
      ├── tests/                 # Placeholder test directory
      │   └── test_example.py
      ├── requirements.txt       # Python dependencies
      ├── README.md              # Project overview
      └── License

    
## 📄 Reports

- ZAP scan results are exported as HTML and JSON.
- Reports are stored in a zip folder under the GitHub Actions "Artifacts" section.
- You can download and inspect them after each workflow run.

## 🛠 Requirements

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- GitHub repository with Actions enabled

## 💡 Goals

This project aims to show how security can be integrated early in the development process, using automation and open-source tools. It provides a hands-on example of DevSecOps principles in action.

## 📌 Notes

- This project is designed for local testing and CI/CD learning purposes.
- The auth.context file exists for future use but is not yet integrated into the scan.
- No cloud deployment is required.

---

