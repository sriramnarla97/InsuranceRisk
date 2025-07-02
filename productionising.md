# 📋 Project Notes: Insurance Risk Prediction – Production Readiness

This document outlines key considerations for productionizing the insurance claim prediction model built using XGBoost and SHAP explainability.

---

## 1. What are the next steps to go from a Jupyter Notebook to a productionised service?

- Modularize the code into reusable Python scripts.
- Create Automated EDA and Reporting
- Create test environment for testing each module.
- Create a REST API (e.g., FastAPI or Flask) to expose the model.
- Serialize,load the trained model using `joblib` and version the model.
- Containerize using Docker for consistent deployment.
- Set up CI/CD pipelines (e.g., GitHub Actions).
- Implement monitoring for drift, latency, and schema changes.

---

## 2. What are the considerations for ensuring the business can leverage it?

- Provide SHAP-based explainability plots.
- Make prediction thresholds configurable for underwriters.
- Ensure performance logging and audit trails.
- Build a simple interface or API for business users.
- Maintain compliance with data governance policies.

---

## 3. What are the steps you would take to provide this to the business?

- Build and demo an API that serves real predictions.
- Share SHAP plots and model insights with stakeholders.
- Provide documentation and a usage guide.
- Collaborate with IT for staging and deployment.
- Define retraining cadence and performance review checkpoints.

---

## 4. Which traditional teams in a business would you need to speak to?

| Team                   | Role |
|------------------------|------|
| Business Analysts      | Validate objectives, threshold strategy |
| Data Engineering       | Provide live or batch data feeds |
| DevOps / IT            | Deploy models, monitor uptime |
| Risk / Compliance      | Ensure model meets regulatory standards |
| Underwriting / Actuarial | Use and interpret model output in pricing |

---

## 5. What is in scope vs. out of scope for your responsibility?

| In Scope                        | Out of Scope                       |
|---------------------------------|------------------------------------|
| ✔️ Model training and tuning     | ❌ Cloud/server infrastructure setup |
| ✔️ SHAP explainability          | ❌ Final UI integration or design |
| ✔️ Threshold tuning             | ❌ Ongoing model monitoring scripts |
| ✔️ Handoff-ready documentation  | ❌ External vendor management |
