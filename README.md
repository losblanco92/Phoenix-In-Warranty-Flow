# 🚀 Postman API Automation with GitHub Actions

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-blue?logo=githubactions)
![Postman](https://img.shields.io/badge/Postman-API%20Testing-orange?logo=postman)
![Newman](https://img.shields.io/badge/Newman-Test%20Runner-green)
![Node.js](https://img.shields.io/badge/Node.js-v22-brightgreen?logo=node.js)
![AWS EC2](https://img.shields.io/badge/AWS-EC2-orange?logo=amazonaws)

A complete **API Test Automation CI/CD pipeline** built using **Postman**, **Newman**, and **GitHub Actions**.

The project automatically executes Postman collections on a **self-hosted AWS EC2 GitHub Runner**, generates rich HTML reports using **newman-reporter-htmlextra**, publishes the latest report to **GitHub Pages**, archives reports as workflow artifacts, and emails execution reports to the team using **Gmail SMTP**.

---

# 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Architecture](#-architecture)
-  [About Me](#about-me)
- [Test Coverage](#-test-coverage)
- [Tech Stack](#-tech-stack)
- [CI/CD Workflow](#-cicd-workflow)
- [Live HTML Report](#-live-html-report)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Generated Report](#-generated-report)

---

# 📖 Project Overview

### Supported Triggers

- ✅ Push to `main`
- ✅ Manual execution using **workflow_dispatch**
- ✅ Scheduled execution using **Cron Jobs**

### Features

- Execute Postman collections using Newman
- Self-hosted GitHub Runner on AWS EC2
- Rich HTML reports using htmlextra
- Publish latest report to GitHub Pages
- Archive reports as GitHub Artifacts
- Email reports using Gmail SMTP
- Secure credential management with GitHub Secrets
- Data-driven API testing using CSV

---

# 🏗 Architecture

```text
                 Developer Push
                        │
                        ▼
               GitHub Actions Workflow
                        │
                        ▼
        Self-Hosted GitHub Runner (AWS EC2)
                        │
                        ▼
             Execute Newman Collection
                        │
        ┌───────────────┼─────────────────┐
        ▼               ▼                 ▼
 HTML Report      GitHub Artifact    Email Report
        │
        ▼
 GitHub Pages Deployment
```

---

# 👨‍💻 About Me

Hi, I'm **Neeraj Joshi**.

I have **7 years of experience in Software Testing**, including **3 years in Automation Testing**.

My primary skills include:
  Manual Testing (Functional, Regression, Smoke, Sanity, Accessibility & API Testing)
- Selenium WebDriver (Java)
- REST Assured
- Postman API Automation
- TestNG
- GitHub Actions
- CI/CD Automation
- API Testing
- Automation Framework Development

I enjoy building scalable automation frameworks and integrating them into modern CI/CD pipelines.

---

# ✅ Test Coverage

This project demonstrates:

- Happy Path Testing
- Negative Testing
- Edge Case Testing
- Token Validation
- Schema Validation
- Data-Driven Testing using CSV
- Environment Management
- Secure Secrets Management using GitHub Secrets

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| Postman | API Testing |
| Newman | Command Line Execution |
| Newman Reporter HTML Extra | HTML Reporting |
| Node.js v22 | Runtime Environment |
| GitHub Actions | CI/CD |
| GitHub Pages | Report Hosting |
| Gmail SMTP | Email Notifications |
| AWS EC2 | Self-Hosted Runner |
| CSV | Data-Driven Testing |

---

# ⚙ CI/CD Workflow

The automation pipeline performs the following steps:

1. Trigger workflow on Push, Manual Dispatch, or Scheduled Cron
2. Execute Postman collections using Newman
3. Generate HTML execution report
4. Archive report as GitHub Artifact
5. Publish latest report to GitHub Pages
6. Email latest report to team members

---

# 📄 Live HTML Report

The latest execution report is available here:

🔗 **GitHub Pages**

https://losblanco92.github.io/Phoenix-In-Warranty-Flow/

---

## Sample Report

<img width="943" alt="Postman Report" src="https://github.com/user-attachments/assets/0fa1ca28-a308-4ed7-85c4-2b1f19b2ba16"/>

---

# 📂 Project Structure

```text
Phoenix-In-Warranty-Flow
│
├── Inwarranty-flow Collection.postman_collection.json
├── QA.postman_environment.json
├── testData.csv

```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/losblanco92/Phoenix-In-Warranty-Flow.git
```

---

## 2. Install Node.js

Download Node.js:

https://nodejs.org/en/download

---

## 3. Install Newman

```bash
npm install -g newman
```

---

## 4. Install HTML Reporter

```bash
npm install -g newman-reporter-htmlextra
```

---

## 5. Execute the Collection

```bash
newman run "Inwarranty-flow Collection.postman_collection.json" \
-e "QA.postman_environment.json" \
-d "testData.csv" \
-r cli,htmlextra \
--reporter-htmlextra-export ./newman/index.html
```

---

# 📊 Generated Report

After execution, the HTML report will be generated in:

```text
newman/index.html
```

---

# ⭐ Highlights

- CI/CD implementation using GitHub Actions
- Self-hosted GitHub Runner on AWS EC2
- Automated API Testing using Newman
- HTML Reporting using htmlextra
- Live report hosting with GitHub Pages
- Scheduled execution using Cron
- Manual workflow execution
- Email notifications using Gmail SMTP
- Secure GitHub Secrets integration
- Data-driven testing using CSV
- Artifact storage for historical reports

---

