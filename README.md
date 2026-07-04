# NeuralGuard — AI-Powered Fraud Detection Platform
 
> Real-time fraud detection combining ML ensembles, LLM-generated insights, and SHAP explainability — analyzing 240,000+ transactions with 99.96% accuracy.

 
 
![Dashboard](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-dashboard.png)
 
---
 
## Key Stats
 
| Metric | Value |
|---|---|
| Transactions Analyzed | 240,000+ |
| Overall Accuracy | 99.96% |
| Precision | 94.05% |
| Recall | 80.61% |
| F1 Score | 86.81% |
| ROC-AUC Score | 0.9529 |
| Transaction Value Protected | $2,417,716 |
 
---
 
## Features
 
- **Live Dashboard** — real-time transaction feed, fraud rate tracking, and risk scoring
- **Dynamic ML Pipeline** — upload any dataset and all dashboard tabs update instantly
- **Dual Model Strategy** — RF + Isolation Forest for smaller datasets; XGBoost + One-Class SVM for large-scale data
- **SHAP Explainability** — every fraud prediction comes with human-readable AI justification
- **Case Review System** — confirm fraud or mark false positives; labels feed back to improve the model
- **Manual Check** — verify any transaction against the live ML model with instant risk score
- **Analytics Hub** — fraud density by amount, average transaction value, anomaly breakdown
- **CSV Batch Inference** — upload transaction CSVs for bulk fraud analysis across 160,000+ records
---
 
## Screenshots

### Login Page
![Login Page](https://raw.githubusercontent.com/AdwitiyaS/CapstoneProject/main/assets1-login_page.png)
### Main Dashboard
![Main Dashboard](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-dashboard1.png)
 
### Model Performance
![Model Stats](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-model_stats.png)
 
### Manual Check with SHAP Explainer
![Manual Check](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-manual_check.png)
 
### Analytics Hub
![Analytics](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-analytics.png)
 
### Case Review System
![Case Review](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-case_Review.png)
 
### Transaction History
![Transactions](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-transactions.png)
 
### CSV Batch Upload
![Upload Data](https://github.com/CapstoneTeam38/CapstoneProject/raw/main/assets1-upload_data.png)
 
---
 
## Tech Stack
 
**Frontend:** React, Chart.js, Tailwind CSS
 
**Backend:** Node.js (Express), Python (Flask)
 
**ML & AI:** Random Forest, Isolation Forest, XGBoost, One-Class SVM, SHAP, LLM prompt pipeline
 
**Database:** MongoDB Atlas
 
**Deployment:** Currently configured for local deployment. Cloud deployment requires a live MongoDB Atlas backend.
 
---
 
## Machine Learning Approach
 
NeuralGuard uses a hybrid modeling strategy based on dataset size:
 
- **Standard Pipeline (RF + IF):** Random Forest + Isolation Forest — optimized for smaller, structured datasets with high precision
- **Large-Scale Pipeline (XGBoost + OCSVM):** XGBoost + One-Class SVM — handles high-volume imbalanced transaction data
All predictions include SHAP-based explainability — showing exactly which features drove the fraud classification, making every decision interpretable and auditable.
 
---
 
## Datasets Used
 
- IEEE Fraud Detection Dataset
- Credit Card Fraud Detection Dataset
- PaySim Dataset
---
 
## System Workflow
 
1. Transaction data ingested via live feed or CSV upload
2. Data passed through the appropriate ML pipeline based on volume
3. Model assigns fraud probability + anomaly score
4. SHAP explainer generates human-readable risk justification
5. Results displayed on dashboard with visual insights
6. Flagged transactions sent to Case Review for human-in-the-loop labeling
---
 
## Run Locally
 
```bash
git clone https://github.com/CapstoneTeam38/CapstoneProject.git
cd CapstoneProject
npm install
pip install -r requirements.txt
```
 
Start backend:
```bash
node server.js
```
 
Start ML service:
```bash
python app.py
```
 
Start frontend:
```bash
npm run dev
```
 
---
 
## Contributors

Built as a Capstone Project at NIIT University. Key contributions include ML pipeline design, SHAP explainability integration, and backend API development for real-time fraud detection. Collaborated with a team on frontend and overall system design.
