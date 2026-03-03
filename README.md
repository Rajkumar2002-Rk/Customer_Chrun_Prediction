# 🎯 AWS-Native Sentiment & Churn Intelligence Engine

## 🚀 The Mission
Modern SaaS businesses lose millions to "silent churn"—customers who are unhappy but don't leave until it's too late. This project engineered an intelligence engine on **AWS SageMaker** that listens to the "emotional pulse" of customers by analyzing support tickets with **AWS Comprehend** and predicting departure risk using high-performance **XGBoost**.

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
