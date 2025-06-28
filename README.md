Thank you, Aarish. Based on your strict preferences:

* **No emojis**
* **No fluff or informal language**
* **Official and instructional tone**
* **Comprehensive documentation reflecting all your work**

Here is your **final, structured, professional `README.md`**, ready to be copy-pasted or committed directly:

---

```markdown
# Postman API Testing Suite

This repository contains a complete API test automation setup using Postman, Newman CLI, data-driven testing via CSV, HTML report generation, and CI/CD integration with GitHub Actions. The suite tests the PostAir Weather API and follows software testing best practices for maintainability, reusability, and reliability.

---

## Project Objectives

- Validate multiple endpoints of a sample weather API.
- Automate test execution using Newman and GitHub Actions.
- Enhance test maintainability through modular and reusable scripts.
- Support data-driven testing using CSV files.
- Integrate CI to auto-run collections and generate reports.

---

## Repository Structure

```

.
├── .github/workflows/                # GitHub Actions configuration
│   └── newman-ci.yml                 # Workflow file for automated test runs
├── PostAir Weather API - Baseline Test Suite.postman\_collection.json  # Collection file
├── weather\_test\_data.csv            # Input data for multiple test iterations
├── newman-report.html               # HTML report output by Newman
├── reports/                         # Folder to store report artifacts
├── postman-cli-reports/            # Directory for structured report output
├── node\_modules/                    # Node.js dependencies
├── package.json                     # Node.js project configuration
├── package-lock.json                # Dependency lock file
└── README.md                        # Project documentation

````

---

## Features Implemented

### 1. Postman Collection Testing
- Tests for weather data retrieval, error handling, authorization, and performance.
- Uses assertions for status codes, response structure, and execution time.
- Negative test cases such as missing parameters and invalid city names.

### 2. Data-Driven Testing
- Data supplied through `weather_test_data.csv`.
- Tests executed in multiple iterations with different inputs using Collection Runner and Newman.

### 3. Postman Package Library (Reusable Scripts)
- Applied DRY (Don’t Repeat Yourself) principle.
- Exported shared logic using `module.exports`.
- Imported logic in other scripts using `pm.require`.

### 4. HTML Reporting
- Reports generated using `newman-reporter-html`.
- Exported to `newman-report.html` for browser view.

### 5. Continuous Integration (CI)
- CI/CD workflow configured with GitHub Actions.
- Workflow runs tests on every `main` branch push.
- Uses `newman` in CI environment with outputs in CLI and HTML.

---

## Setup Instructions

### Step 1: Clone the Repository

```bash
git clone https://github.com/AarishIrfan/postman-api-testing-suite.git
cd postman-api-testing-suite
````

### Step 2: Install Required Packages

```bash
npm install newman newman-reporter-html
```

### Step 3: Run Tests Locally

```bash
npx newman run "PostAir Weather API - Baseline Test Suite.postman_collection.json" \
  --iteration-data "weather_test_data.csv" \
  --reporters cli,html \
  --reporter-html-export "newman-report.html"
```

### Step 4: View the HTML Report

Open `newman-report.html` in any browser:

```bash
start newman-report.html       # For Windows
open newman-report.html        # For macOS
```

---

## GitHub Actions: CI/CD Workflow

The `.github/workflows/newman-ci.yml` file is configured to:

* Trigger on every push to `main`
* Run Postman tests using Newman
* Use the data file and generate a fresh report
* Ensure consistency across environments

---

## Concepts and Learning Outcomes

| Topic                                            | Status |
| ------------------------------------------------ | ------ |
| Manual API Testing via Postman                   | Done   |
| Collection Runner with Iteration Data            | Done   |
| Postman Test Assertions (Status, Response, Time) | Done   |
| DRY Principle via Package Library                | Done   |
| Exporting and Importing Functions (Node style)   | Done   |
| Newman CLI for Local Test Execution              | Done   |
| HTML Reports using `newman-reporter-html`        | Done   |
| Git Initialization, Commit, and Push             | Done   |
| CI with GitHub Actions for Automation            | Done   |
| Creating Releases via GitHub                     | Done   |

---

## Troubleshooting

### 1. Newman Reporter Not Found

**Error**:

```
newman: could not find "cli,html" reporter
```

**Fix**:

```bash
npm install newman newman-reporter-html
```

---

### 2. PowerShell ExecutionPolicy Error

**Fix**:

```bash
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

---

### 3. Git Push Rejected Due to Remote Changes

**Fix**:

```bash
git pull origin main --rebase
git push origin main
```
