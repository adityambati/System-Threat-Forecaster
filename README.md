# 🔥 System Threat Detector - Malware Prediction  

![Project Status](https://img.shields.io/badge/Status-Active-green)  
![Contributors](https://img.shields.io/badge/Contributors-1-blue)  
![License](https://img.shields.io/badge/License-MIT-lightgrey)  

## 🔍 Overview  

This project is part of a Kaggle competition where the goal is to **predict a system’s probability of getting infected by various families of malware** based on different system properties.  

The dataset is derived from **antivirus telemetry data** containing system configurations, installed security products, OS details, and past malware detections.  

Each row in the dataset represents a **unique machine** identified by `MachineID`, with `target` as the ground truth (1 = Malware detected, 0 = No Malware detected).  

## 📂 Repository Structure  
```plaintext
📦 System_Threat_Detector ├── 📂 data/ # Contains train and test datasets │ ├── train.csv
│ ├── test.csv
├── 📜 kaggle_notebook.ipynb # Main Jupyter Notebook with all code
├── 📜 requirements.txt # Dependencies for running the notebook
├── 📜 README.md # Project documentation
```

## 🚀 Features Implemented  

✔️ **Data Cleaning & Preprocessing** – Handling missing values, feature encoding, and feature scaling.  
✔️ **Exploratory Data Analysis (EDA)** – Understanding data distributions, correlations, and system security trends.  
✔️ **Feature Engineering** – Creating meaningful features to improve model accuracy.  
✔️ **Model Training & Evaluation** – Using **XGBoost, LightGBM, Random Forest, and Logistic Regression**.  
✔️ **Hyperparameter Tuning** – Optimizing model performance using **GridSearchCV**.  
✔️ **Final Predictions** – Generating probability scores for malware infections on test machines.  

## 📊 Model Performance  

| Model          | Accuracy | F1 Score |
|---------------|---------|----------|
| Logistic Regression | 0.6122 | 0.63 |
| Decision Tree | 0.5568 | 0.56 |
| Random Forest | 0.6064 | 0.62 |
| XGBoost | 0.6254 | 0.64 |
| LightGBM | 0.6287 | 0.65 |

✅ **Best Model:** `XGBoost` achieved the highest accuracy & F1-score.

## 🔎 Dataset Details  

The dataset consists of **76 features**, including:  

- **System Information**: `OSVersion`, `Processor`, `RAM`, `DiskCapacity`, `PrimaryDisplayResolution`, `ChassisType`, etc.  
- **Security Features**: `IsSystemProtected`, `FirewallEnabled`, `IsSecureBootEnabled`, `AutoSampleSubmissionEnabled`, etc.  
- **Software & Updates**: `EngineVersion`, `AppVersion`, `SignatureVersion`, `OSBuildLab`, `LicenseActivationChannel`, etc.  
- **Malware Detection History**: `DateAS` (Malware signature dates), `DateOS` (OS update timestamps), and `target`.  

📌 **Full column descriptions can be found in the notebook.**  

## 📦 Installation & Usage  

To **run this project locally**, follow these steps:

### Clone the Repository  
```bash
git clone https://github.com/adityambati/System-Threat-Forecaster.git
cd System-Threat-Forecaster
pip install -r requirements.txt\
```
You can run the kaggle_notebook.ipynb using Jupyter Notebook or Google Colab.
