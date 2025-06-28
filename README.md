Absolutely, Aarish. Here is a **complete, professional, no-fluff `README.md`** for your `postman-api-testing-suite` repository — using *everything you've done and learned so far*, in a clear and structured format:

---

````markdown
# Postman API Testing Suite

This repository contains a complete API test automation setup using [Postman](https://www.postman.com/), [Newman](https://www.npmjs.com/package/newman), data-driven testing, HTML reporting, and CI/CD integration via GitHub Actions.

---

## 📌 Project Overview

This test suite covers the PostAir Weather API using:

- Postman Collection (`.postman_collection.json`)
- CSV-based data for iterations
- Newman CLI to run tests locally
- HTML reporting with `newman-reporter-html`
- CI automation with GitHub Actions
- Package library and reusable test scripts using DRY principles

---

## 📂 Project Structure

```bash
├── .github/workflows/newman-ci.yml       # GitHub Actions workflow for CI
├── PostAir Weather API.postman_collection.json  # Main Postman Collection
├── weather_test_data.csv                 # Data-driven test input
├── newman-report.html                    # Auto-generated HTML report
├── reports/                              # Output folder for reports
├── node_modules/                         # Node.js dependencies
├── package.json                          # Project dependencies and scripts
└── README.md                             # This documentation
````

---

## ✅ Features Covered

### 1. **Manual and Automated API Testing**

* Status code verification
* Response structure and time assertions
* Multiple endpoints and request types
* Regression scenarios

### 2. **Data-Driven Testing**

* Input data supplied via `weather_test_data.csv`
* Test runs for multiple values in one go

### 3. **Reusable Test Scripts (DRY Principle)**

* Used Postman Package Library (experimental)
* Applied `pm.require()` to reuse scripts
* Modular logic to avoid redundancy

### 4. **Error Handling and Edge Cases**

* Invalid city parameter testing
* Missing API key simulation
* Large payload stress tests

### 5. **Performance Assertions**

* Asserted that response time < 1000ms or 1500ms
* Logged slow API responses

### 6. **GitHub Actions CI/CD**

* Configured `.github/workflows/newman-ci.yml`
* Automatically runs collection on every push to `main`
* Generates and uploads `newman-report.html`

---

## 🚀 How to Use This Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/AarishIrfan/postman-api-testing-suite.git
cd postman-api-testing-suite
```

---

### Step 2: Install Dependencies

```bash
npm install newman newman-reporter-html
```

---

### Step 3: Run Tests Locally

```bash
npx newman run "PostAir Weather API - Baseline Test Suite.postman_collection.json" \
  --iteration-data "weather_test_data.csv" \
  --reporters cli,html \
  --reporter-html-export "newman-report.html"
```

---

### Step 4: View HTML Report

Open the generated `newman-report.html` file in any browser:

```bash
start newman-report.html    # Windows
open newman-report.html     # macOS
```

---

### Step 5: Use GitHub Actions

When you push to the `main` branch, GitHub Actions will:

* Trigger the Newman run
* Use the collection and CSV
* Output results in HTML

CI file: `.github/workflows/newman-ci.yml`

---

## 🔁 Learnings Covered From A–Z

| Area                                                            | Covered |
| --------------------------------------------------------------- | ------- |
| Postman Manual Testing                                          | ✅       |
| Postman Collection Runner                                       | ✅       |
| Data Files (.csv) for Test Iterations                           | ✅       |
| Assertions and Scripts                                          | ✅       |
| Reusable Test Scripts (Package Library)                         | ✅       |
| DRY Principle (`Don't Repeat Yourself`)                         | ✅       |
| Export/Import Scripts using `module.exports` and `pm.require()` | ✅       |
| Running Tests via CLI with Newman                               | ✅       |
| Generating Reports in HTML                                      | ✅       |
| GitHub Setup and Push                                           | ✅       |
| GitHub Actions CI/CD Integration                                | ✅       |
| Understanding Test Failures and Reporting                       | ✅       |
| Adding a Release in GitHub                                      | ✅       |
| Professional Project Folder Structure                           | ✅       |

---

## 🔧 Troubleshooting

**Error: `newman: could not find "cli html" reporter`**

> Run: `npm install newman newman-reporter-html`

**Error: `ExecutionPolicy` on PowerShell**

> Run: `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`

**Error: Push rejected due to remote changes**

> Run: `git pull origin main --rebase` then `git push origin main`

---

## 👤 Author

**Aarish Irfan**
Software Quality Assurance Engineer
[LinkedIn](https://www.linkedin.com/in/aarishirfan) | [GitHub](https://github.com/AarishIrfan)

---

## 📄 License

This project is open-sourced for learning and demo purposes.

```

---

Would you like me to:

- Commit this `README.md` to your repo directly via CLI steps?
- Help you write a LinkedIn post about this project now?
```
