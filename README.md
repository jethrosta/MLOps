# ⚙️ Machine Learning Operations (MLOps)
## What are Developer, DevOps, and MLOps?
In the past, software development and IT operations worked separately. Developers focused on writing new features, while Operations handled deployment and maintenance. This gap led to miscommunication, slow releases, and unstable systems. Manual deployments caused delays, and poor collaboration led to errors and finger-pointing.

In general, application development involves two main teams: **Developers** (who design, write, and test the code) and **IT Operations** (who deploy and monitor it). While they share the same goal, delivering a reliable product, differences in tools, priorities, and workflows often create conflicts. Developers want speed, sometimes at the cost of stability. Operations aim for stability, but rapid code changes can disrupt that.
These differences lead to bottlenecks, poor user experiences, and business losses. To fix this, the concept of DevOps emerged. DevOps is a set of cultural philosophies, practices, and tools that aims to improve collaboration between development and operations teams. It focuses on breaking down silos, sharing responsibilities, and automating repetitive tasks. DevOps unifies both teams, enabling faster innovation, better user feedback, and higher business value. Inspired by the success of DevOps, MLOps applies similar principles to Machine Learning systems. It bridges the gap between ML Engineers and Operations teams to ensure scalable, reliable, and maintainable ML deployment. Imagine an ML model as a recipe created by a chef, the job doesn’t stop there. MLOps ensures the dish is served consistently every time (in production).

<div align="center"> <img src="https://assets.cdn.dicoding.com/original/academy/dos-a10ab3b55e97e7b2810c27353a1a463c20250326150424.jpeg"> </div>

## 🌀 Machine Learning Lifecycle
In real-world ML systems, many teams are involved, each with different skills and responsibilities. Ideally, they collaborate using MLOps practices to build systems that are reliable, scalable, and easy to maintain.

In mature companies, data scientists build ML models, which are then handed off to ML engineers and software developers for deployment. However, this hand-off process often involves waiting, unclear responsibilities, and misalignment of priorities.

<div align="center"> <img src="https://github.com/user-attachments/assets/17d3b636-c781-44b7-82f1-5b9255109c65"> </div>

## 🚀 MLOps Maturity
MLOps Maturity refers to how advanced an organization is in automating and structuring its ML workflows. It helps companies evaluate their capabilities and find areas for improvement, from development to deployment.

Maturity levels consider human/cultural aspects, process structure, and technology. The higher the level, the more advanced and impactful the system, but also more complex.

There’s no single standard for maturity levels. Some companies (like Google or Microsoft) use 3–5 levels depending on their use cases. The key is adopting the approach that fits the team’s needs.

## ✅ Building Reliable ML Models
Start with a Solid Data Pipeline
Many ML developers focus too much on models and ignore the data pipeline. But data is the foundation. Building a model without a good pipeline is like building a house on sand. Most ML projects fail due to poor data quality, not bad algorithms.

Good data = good model.

## 🔁 ML Workflow Steps
A good ML workflow includes the following steps:
1. Data Collection
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Model Selection
5. Evaluation
6. Deployment
7. Monitoring

This process is iterative. You may need to revisit earlier steps to improve performance.

## 👥 Team Roles
ML system development usually involves multiple roles:
1. Data Engineers / Analysts: Handle raw data, ETL, and feature stores.
2. ML Engineers: Use clean, structured data to build, train, and evaluate models.
3. Even with clean data, ML Engineers may still perform data wrangling to fit the model’s needs.

## ⚠️ Common Problem
If you repeat data loading and preprocessing manually, you risk inconsistency and wasted time.

Solution: Automate this by wrapping data loading/preprocessing into a single function. This avoids duplication, improves consistency, and makes automation easier.

## 🛠️ Continuous Training Automation
This module introduces GitHub Actions to automate data validation and preprocessing before training, making your ML pipeline more robust and efficient.

## 🔄 MLFlow: Managing the ML Lifecycle
MLflow is an open-source platform that helps manage the end-to-end ML workflow, from tracking experiments to deploying models. It keeps everything, parameters, metrics, models, in one place.

<div align="center"> <img src="https://assets.cdn.dicoding.com/original/academy/dos-03fdb97d263203c84a96e772408312bf20250318124211.png"> </div>
It works with libraries like TensorFlow, PyTorch, Scikit-learn, and XGBoost.

<div align="center"> <img src="https://assets.cdn.dicoding.com/original/academy/dos-617d1438bb19061a33e93933abb489f420250318123301.jpeg"> </div>
MLflow’s Key Components
- Tracking – Logs experiments, parameters, metrics, and artifacts.
- Projects – Packages projects for reproducibility across environments.
- Models – Standardizes model storage and sharing.
- Model Registry – Manages versions and stages of deployed models.
- Pipelines (Experimental) – Structured pipelines for end-to-end ML processes (available from version 1.30.1).

## 🔁 GitHub Actions
<div align="center"> <img src="https://images.ctfassets.net/8aevphvgewt8/KiQBgcnMQg6dALaS6erGk/f8d49c0cc5a461b903e52d08c3c3b8f6/actions-hero.webp?w=2496&fm=webp&q=90"> </div>
GitHub Actions lets you automate development workflows like CI/CD (build, test, deploy) based on triggers such as code push or pull requests. You can also automate tasks like code formatting, security checks, or deploying Docker images.

Workflows are defined using YAML files under .github/workflows/.
<div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2017.26.12.png"> </div>
<div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2017.26.21.png"> </div>

This reduces manual work, speeds up development, and improves code quality.

## 🐳 Docker
<div align="center"> <img src="https://www.docker.com/app/uploads/2025/04/pny-dbc-docker-desktop-home.png"> </div>
Docker is a platform that helps you package applications into lightweight containers. A container includes everything the app needs—code, runtime, libraries, so it runs the same anywhere: dev laptop, staging, or production. This eliminates the classic "it works on my machine" issue.

## 📊 Prometheus
<div align="center"> <img src="https://prometheus.io/_next/static/media/prometheus-logo.7aa022e5.svg"> </div>
Prometheus is a monitoring and alerting tool that collects time-series metrics. It scrapes data from /metrics endpoints and stores it for querying using PromQL. It's ideal for observing system health, detecting anomalies, and triggering alerts.

## 📈 Grafana
<div align="center"> <img src="https://grafana.com/media/home/workflows/workflow_2.png?w=1920"> </div>
Grafana is a visualization tool for metrics and logs. It works well with Prometheus, displaying real-time dashboards. Grafana supports many data sources and helps teams understand performance trends, resource usage, and system issues clearly.

## 🔗 Why Docker + Prometheus + Grafana?
When combined, these three tools create an efficient and observable system:
1. Docker ensures consistent environments from dev to prod
2. Prometheus monitors APIs and system performance
3. Grafana displays it all in one place with easy-to-read dashboards

Together, they provide:
- Faster debugging and reduced downtime
- Easier and faster testing with Docker
- Automated alerts for early issue detection
- Complete visibility—from ML performance to resource usage

They make the whole development-to-production pipeline automated, reliable, and scalable.

## 📊 My Monitoring Dashboard & Alerts
I created a custom Grafana dashboard to monitor CPU, RAM, API request count, and latency.

<div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2016.25.13.png"> </div>
Each metric is useful and shown in real time. I also set up an alert: when the ML model is used more than 4,000 times, Grafana sends an email alert suggesting retraining, to prevent model drift.

<div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2017.13.50.png"> </div>
Once the threshold is reached, the alert triggers after 1 minute (configurable), then sends an email:

<div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2017.14.16.png"> </div> <div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2017.14.35.png"> </div>
The alert lands in the configured inbox, with clear and actionable information:

<div align="center"> <img src="https://github.com/jethrosta/MLOps/blob/main/images/Screenshot%202025-07-07%20at%2017.29.10.png"> </div>
