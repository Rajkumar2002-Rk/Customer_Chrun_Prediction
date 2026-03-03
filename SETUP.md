# 💻 Local Setup Instructions

Follow these steps to run the SaaS Churn Predictor notebook on your local machine.

### 1. Clone the Repository
Download the project files to your computer:
```bash
git clone [https://github.com/Rajkumar2002-Rk/Customer_Chrun_Prediction.git](https://github.com/Rajkumar2002-Rk/Customer_Chrun_Prediction.git)
cd Customer_Chrun_Prediction
```

### 2. Install Dependencies
It is recommended to use a Python virtual environment. Once activated, install the required libraries:
```bash
pip install -r requirements.txt
```

### 3. Launch the Environment
Open Jupyter to view and run the notebook:
```bash
jupyter notebook notebooks/Customer_churn_prediction.ipynb
```

**Note:** The raw data files are not included in this repository. The notebook is configured to pull the required dataset directly from Amazon S3.
