# 🔐 Security Policy

Thank you for helping to secure this project!

## 📆 Supported Versions

I currently support and maintain the latest version of this project. Please ensure you are using the most recent version before reporting a vulnerability.

| Version | Supported |
|---------|-----------|
| latest  | ✅        |
| older   | ❌        |

## 📢 Reporting a Vulnerability

If you discover a security vulnerability, please follow these steps:

1. **Do not create a public issue.**
2. create an Issue with:
   - A detailed description of the vulnerability
   - Steps to reproduce
   - Any relevant logs or screenshots

I'll try to respond within **5 business days** and work with you on a fix.

## 🤝 Responsible Disclosure

I ask that you:

- Give us a reasonable amount of time to address the issue before disclosing it publicly.
- Avoid exploiting the vulnerability for any purpose other than testing.
- Act in good faith to avoid privacy violations, data destruction, or service disruption.

## 🛡️ Automated Security Scanning

This project integrates [OWASP ZAP](https://www.zaproxy.org/) into its CI/CD pipeline using GitHub Actions. Every push or pull request triggers an automated scan of the OWASP Juice Shop instance to detect common vulnerabilities such as:

- Cross-Site Scripting (XSS)
- SQL Injection
- Missing security headers
- Other OWASP Top 10 risks

Scan results are uploaded as artifacts and can be reviewed after each workflow run.

Thank you for helping me keep this project secure!
