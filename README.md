# 🎯 AWS-Native Sentiment & Churn Intelligence Engine

## 🚀 The Mission
Modern SaaS businesses lose millions to "silent churn"—customers who are unhappy but don't leave until it's too late. This project engineered an intelligence engine on **AWS SageMaker** that listens to the "emotional pulse" of customers by analyzing support tickets with **AWS Comprehend** and predicting departure risk using high-performance **XGBoost**.

## 📊 The Dataset
This project utilizes a public SaaS customer churn dataset containing usage metrics and support ticket logs. 
* **Data Governance:** To adhere to MLOps best practices and respect data licensing, the raw `.csv` files are **not** hosted in this public repository. 
* **Ingestion:** Within the notebook, the data is staged in and pulled directly from an **Amazon S3** bucket to simulate a secure cloud environment.

## 🛠️ The Architecture
* **Data Lake:** Amazon S3
* **NLP Engine:** AWS Comprehend
* **Compute:** SageMaker Notebooks & Training Jobs
* **Stack:** Python, XGBoost, Scikit-Learn, Pandas

## 🧠 Engineering Highlights
### 🔹 Sentiment Feature Extraction
Instead of ignoring text data, I used **AWS Comprehend** to derive a **Sentiment Score** from the last customer support ticket. This converted "human frustration" into a mathematical feature that the model used to identify high-risk accounts.

### 🔹 Usage Intensity Metric
I engineered a custom ratio: `Usage Intensity = Daily Usage Mins / Account Age Days`. This normalized activity levels, allowing the model to distinguish between a "new power user" and a "fading veteran".

### 🔹 Business-Centric Optimization
I challenged the standard 0.5 probability threshold. By shifting the threshold to **0.3**, I intentionally traded minor accuracy for a **Recall jump to 0.67**. This ensures the business catches 67% of churners, prioritizing revenue retention over perfect guesses.

## 📈 Performance Ledger
| Model | Accuracy | Churn Recall (Sensitivity) |
| :--- | :--- | :--- |
| **Logistic Regression (Baseline)** | 82.40% | 0.64 |
| **Optimized XGBoost (Final)** | **80.00%** | **0.67 (Winner)** |

## 🏗️ Deployment Strategy
The pipeline is designed for **MLOps**. By staging data in S3 and using SageMaker's modular training, the model can be retrained automatically as customer behavior "drifts," ensuring the intelligence remains sharp as the business scales.

<img width="522" height="552" alt="Customer_churn_Confusion_Matrix" src="https://github.com/user-attachments/assets/47f5b7d0-38bb-4019-9a7c-84473516dd05" />
