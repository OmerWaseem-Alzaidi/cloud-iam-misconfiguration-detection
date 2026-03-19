# Misconfiguration Detection Dataset for Cloud IAM and APIs

> **✅ Completed Research Project** - All results, figures, and analysis included. No installation or re-running required!

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Machine learning analysis for detecting misconfigurations in Cloud IAM (Identity and Access Management) and API usage using AWS CloudTrail audit logs.

---

## 🎯 Research Results

### Model Performance

Our analysis achieved strong accuracy in detecting IAM and API misconfigurations (e.g., unknown roles, insecure configurations):

| Model | Accuracy | AUC | Recall | Precision | F1-Score |
|-------|----------|-----|--------|-----------|----------|
| **XGBoost** | **0.9928** | **0.9990** | **0.9646** | **0.9083** | **0.9356** |
| **Random Forest** | 0.9923 | 0.9991 | 0.9469 | 0.9145 | 0.9304 |
| MLP Neural Network | 0.9822 | 0.9788 | 0.9469 | 0.7754 | 0.8526 |
| Logistic Regression | 0.8943 | 0.9279 | 0.8319 | 0.3186 | 0.4608 |

### Key Achievements

- ✅ **99.28% Accuracy** with XGBoost (best model)
- ✅ **~99.9% AUC-ROC** for top tree-based models
- ✅ **High Recall** — effective detection of misconfigurations
- ✅ **Multiple model types** — Classical ML, Neural Networks, and Bidirectional LSTM evaluated

---

## 🗂️ Repository Contents

```
cloud-iam-misconfiguration-detection/
├── README.md                           # This file
├── LICENSE                             # MIT License
├── .gitignore
│
├── notebooks/
│   └── Cloud_misconfiguration_ML_analysis.ipynb   # Complete analysis notebook
│
└── data/
    └── raw/
        └── misconfiguration_dataset.csv         # Place downloaded dataset here (see below)
```

---

## 📖 About This Research

### Overview

This research applies machine learning to detect cloud security misconfigurations from AWS CloudTrail audit logs. The models identify anomalous IAM patterns and API usage that may indicate misconfigured access, unknown roles, or insecure configurations.

### Methodology

1. **Dataset**: AWS CloudTrail API audit logs
   - 10,404 instances
   - 35 features (event metadata, user identity, event source, region, etc.)
   - Binary classification (Misconfiguration / Normal)

2. **Preprocessing**: Feature engineering, label encoding, SMOTE for class imbalance

3. **Model Training**: Comparison of 5+ algorithms:
   - Logistic Regression
   - Random Forest
   - XGBoost
   - MLP Neural Network
   - Bidirectional LSTM (Deep Learning)

4. **Evaluation**: Comprehensive metrics (Accuracy, AUC-ROC, Precision, Recall, F1-Score)

### Key Technologies

- **Cloud Security**: AWS CloudTrail, IAM, API audit logs
- **Machine Learning**: XGBoost, Random Forest, scikit-learn
- **Deep Learning**: TensorFlow/Keras (MLP, Bidirectional LSTM)
- **Python**: pandas, matplotlib, seaborn, imbalanced-learn

---

## 📓 Viewing the Analysis

### Option 1: View Online (Easiest)
- Open the [Jupyter Notebook](notebooks/Cloud_misconfiguration_ML_analysis.ipynb) directly on GitHub
- GitHub automatically renders notebooks for easy viewing

### Option 2: View Locally
If you want to explore or re-run the notebook:

```bash
# Clone the repository
git clone https://github.com/omerwaseem-alzaidi/cloud-iam-misconfiguration-detection.git

# Open the notebook
cd cloud-iam-misconfiguration-detection/notebooks
jupyter notebook Cloud_misconfiguration_ML_analysis.ipynb
```

**Dependencies (if re-running):**
```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost imbalanced-learn tensorflow
```

---

## 💾 Dataset

The dataset is **not included** in this repository. You must download it from IEEE DataPort (subscription required).

### Download Instructions

1. **Get the dataset**: [Misconfiguration Detection Dataset for Cloud IAM and APIs](https://ieee-dataport.org/documents/misconfiguration-detection-dataset-cloud-iam-and-apis) (IEEE DataPort)
2. **Place the file**: Save the downloaded CSV as `misconfiguration_dataset.csv` in `data/raw/`
3. **Create the folder** if it doesn't exist:
   ```bash
   mkdir -p data/raw
   ```
   Then copy your downloaded file to `data/raw/misconfiguration_dataset.csv`

### Dataset Details

- **Source**: IEEE DataPort — synthetic AWS CloudTrail audit logs and IAM configurations
- **Size**: ~10.4K CloudTrail event records
- **Features**: 35 attributes including eventVersion, userIdentity_type, eventSource, eventName, awsRegion, errorCode, RoleName (target), and more

---

## 🔬 Research Highlights

### Contributions

1. **ML-based Misconfiguration Detection**: Automated identification of IAM/API misconfigurations from audit logs
2. **Comprehensive Model Comparison**: Evaluated classical ML, gradient boosting, and deep learning approaches
3. **Production-ready Performance**: XGBoost achieves 99.28% accuracy with high recall for security-critical detection
4. **Reproducible Pipeline**: Complete notebook with preprocessing, training, and evaluation

### Applications

- Cloud security monitoring
- IAM policy compliance auditing
- API usage anomaly detection
- Automated misconfiguration discovery
- Security Operations Center (SOC) tooling

---

## 👤 Authors

**Omer Waseem AL-Zaidi**
- 🎓 UG Scholar, Department of Software Engineering
- 🏛️ Halic University, Istanbul, Turkey
- 📧 omaralzaidi2002@gmail.com

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

For questions about this research:

<a href="mailto:omaralzaidi2002@gmail.com"><img src="https://cdn.simpleicons.org/gmail/EA4335" width="22" height="22" alt="Email"/></a>
<a href="https://github.com/OmerWaseem-Alzaidi"><img src="https://cdn.simpleicons.org/github/e6edf3" width="22" height="22" alt="GitHub"/></a>
<a href="https://www.linkedin.com/in/omerwaseemal-zaidi">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin&logoColor=white" />
</a>

---

<div align="center">

**⭐ If you find this research useful, please star this repository! ⭐**

*Cloud Security • ML-Powered Detection • Ready to Use*

</div>
