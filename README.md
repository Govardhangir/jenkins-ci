## 🧩 Continuous Integration Pipeline using Jenkins, SonarQube & Nexus Repository

## 📘 Overview

This project demonstrates a **Continuous Integration (CI)** workflow using **Jenkins**, **SonarQube**, and **Nexus Repository**.  
It automates the process of **building, testing, analyzing, and storing artifacts** for a software project.

---

## 🚀 CI Pipeline Flow

### 1. Code Commit
- Developers commit code changes to the **GitHub repository**.
- Each commit triggers an **automated Jenkins build** via a webhook or polling.

### 2. Jenkins Pipeline Execution
Jenkins performs several stages as part of the CI pipeline:

| Stage | Description |
|--------|-------------|
| **Fetch** | Jenkins fetches the latest code from GitHub. |
| **Build** | The code is compiled or built using tools like Maven or Gradle. |
| **Unit Testing** | Runs automated test cases to validate the build. |
| **Code Analysis** | The built code is sent to **SonarQube** for static code analysis. |
| **Quality Gates** | SonarQube checks code quality against predefined metrics (bugs, vulnerabilities, coverage). |
| **Upload Artifact** | If the build passes all tests and quality gates, the artifact (JAR/WAR) is uploaded to **Nexus Repository**. |

---

## 🧠 Tools Used

| Tool | Purpose |
|------|----------|
| **GitHub** | Source code management and version control |
| **Jenkins** | Automation server for building and integrating code |
| **SonarQube** | Code quality and static analysis |
| **Nexus Repository** | Artifact repository for storing build outputs (e.g., JAR/WAR files) |
| **Email Notification** | Sends build and test results to the team |

---

## 🧱 Nexus Artifact Workflow

Below image represents the **artifact management workflow** in Nexus Repository:

📸 *Add your artifact workflow image here:*

![Artifact Workflow](./images/artifact-workflow.png)

**Example Repository Structure:**
nexus-repository/
│
├── releases/
│ ├── app-1.0.0.jar
│ ├── app-1.0.1.jar
│
└── snapshots/
├── app-1.0.2-SNAPSHOT.jar


---

## 🧩 SonarQube Quality Metrics

The following key metrics are evaluated in **SonarQube**:

- 🧩 Code Smells  
- 🐞 Bugs  
- 🔒 Vulnerabilities  
- 🧪 Test Coverage  
- 🔁 Duplicated Lines  

If thresholds fail, Jenkins halts the pipeline to **maintain high-quality code**.

---

## 📢 Notifications

Jenkins sends notifications at critical points such as:
- Build start
- Build success or failure
- Quality Gate pass or fail

Notifications can be sent via:
- 📧 **Email**
- 💬 **Slack**

---

## 🖼️ CI Architecture Diagram

📸 *Add your CI Pipeline/Architecture Diagram here:*

![CI Pipeline Architecture](./images/ci-pipeline-architecture.png)

This diagram represents the **CI process from code commit to artifact storage in Nexus Repository**.

---

## 🧾 Sample Jenkins Pipeline Output

Below are some screenshots from the working Jenkins pipeline:

### ✅ Jenkins Build Success
![Jenkins Build Success](./outputs/jenkins-build-success.png)

### 🧪 SonarQube Quality Gate Pass
![SonarQube Quality Gate](./outputs/sonarqube-quality-gate.png)

### 📦 Nexus Artifact Upload
![Nexus Artifact Upload](./outputs/nexus-artifact-upload.png)

---

## ✅ Benefits

- ⚙️ Automated build and testing workflow  
- 🧩 Consistent code quality enforcement  
- 📦 Centralized and versioned artifact management  
- 🐞 Early detection of bugs and vulnerabilities  
- 🤝 Improved team collaboration through notifications  

---

## 🧰 Prerequisites

Before running the CI pipeline, ensure:
- ✅ Jenkins is installed and configured  
- ✅ SonarQube server is up and integrated with Jenkins  
- ✅ Nexus Repository is accessible and credentials are configured  
- ✅ Maven is installed and configured in Jenkins  

---

## 💡 Future Enhancements

- 🐳 Integrate **Docker** for containerized builds  
- ☸️ Add **Kubernetes** for deployment automation  
- 🔔 Include **Slack notifications** for real-time build updates  

---

## 👨‍💻 Author

**Giri**  
💼 *DevOps Enthusiast | CI/CD Automation Learner*  
📍 *India*  
📘 *Project: Continuous Integration Pipeline with Jenkins, SonarQube & Nexus*  

---



