# 🚀 Deployment Risk Assessment & Rollback Prediction

This project is an AI-powered system designed to analyze software deployment risks and automatically trigger rollbacks if necessary. It helps ensure stable deployments in complex environments by combining machine learning predictions with real-time performance metrics.

---

## 🔍 Problem Statement

In real-world DevOps workflows, failed deployments can result in critical outages and financial losses. This project predicts the likelihood of failure during a deployment based on:

- Size of code changes
- Number of impacted services
- Timing of deployment (e.g., weekend)

Additionally, it monitors simulated live performance metrics such as:
- Latency
- Error rate

Based on the risk or detected anomalies, it can trigger an **automated rollback**.

---

## 💡 Features

- ✅ ML-based deployment success/failure prediction
- ✅ Real-time anomaly detection (latency, error rate)
- ✅ FastAPI backend with a `/deploy` endpoint
- ✅ Swagger UI for easy testing
- ✅ Exposed via `ngrok` for public access
- ✅ Auto rollback trigger on high risk or anomalies

---

## ⚙️ Technologies Used

- **Python**
- **Scikit-learn** – ML model (Random Forest)
- **FastAPI** – Web API framework
- **Uvicorn** – ASGI server
- **Ngrok** – Public tunnel for Colab
- **Google Colab** – Development environment

---

## 📈 Input Parameters

The API accepts:
- `lines_changed`: Number of lines of code changed in this deployment
- `services_impacted`: Number of microservices affected
- `weekend_deploy`: Whether deployment is happening on a weekend (1 = Yes, 0 = No)

---

## 📤 API Endpoint

