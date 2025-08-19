# Fraud Detection ML Project

A machine learning system for detecting fraudulent financial transactions using a trained Logistic Regression model and interactive Streamlit web application.

## 🎯 Overview

This project analyzes financial transaction data to identify potentially fraudulent activities based on transaction characteristics like amount, balance changes, and transaction type. The system achieves 94% accuracy using a Logistic Regression model trained on over 6.3 million transactions.

## 📊 Dataset

**Download the dataset from Kaggle**: [Fraud Detection Dataset](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download)

**Features:**
- `step`: Time step of transaction
- `type`: Transaction type (PAYMENT, TRANSFER, CASH_OUT, DEPOSIT)
- `amount`: Transaction amount
- `nameOrig/nameDest`: Sender/receiver account identifiers
- `oldbalanceOrg/newbalanceOrig`: Sender balance before/after
- `oldbalanceDest/newbalanceDest`: Receiver balance before/after
- `isFraud`: Fraud indicator (target variable)
- `isFlaggedFraud`: Flagged fraud indicator

## 🏗️ Project Structure

```
├── fraud_detection.py                  # Streamlit web app
├── analysis_model.ipynb                # EDA & model training notebook
├── fraud_detection_pipeline.pkl        # Trained ML pipeline
├── requirements.txt                     # Dependencies
└── AIML Dataset.csv                    # Training dataset (download from Kaggle)
```

## 🚀 Features

- **Real-time Fraud Detection**: Instant predictions via Streamlit interface
- **Interactive Web App**: User-friendly input forms for transaction details
- **Production-Ready Model**: Serialized pipeline for easy deployment
- **Comprehensive Analysis**: Full EDA and feature engineering workflow

## 🛠️ Quick Start

1. **Clone & Setup**
   ```bash
   git clone https://github.com/yourusername/machinelearning-fraud-detection-v1.git
   cd machinelearning-fraud-detection-v1
   pip install -r requirements.txt
   ```

2. **Download Dataset**
   - Get `AIML Dataset.csv` from [Kaggle](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download)
   - Place in project root directory

3. **Run the App**
   ```bash
   streamlit run fraud_detection.py
   ```

## 🎮 Usage

### Web Application
- Select transaction type (PAYMENT, TRANSFER, CASH_OUT, DEPOSIT)
- Enter transaction amount and balance details
- Get instant fraud prediction (0 = legitimate, 1 = fraudulent)

### Model Development
Open `analysis_model.ipynb` to explore:
- Data analysis and visualizations
- Feature engineering process
- Model training and evaluation
- Pipeline creation

## 📈 Model Performance

| Metric | Non-Fraudulent | Fraudulent |
|--------|----------------|------------|
| **Accuracy** | 94% | 94% |
| **Precision** | 100% | 2% |
| **Recall** | 94% | 94% |
| **F1-Score** | 97% | 4% |

*Note: Low precision for fraud class is common in highly imbalanced datasets (0.13% fraud rate)*

## 🔍 Key Insights

- **Fraud Rate**: Only 0.13% of transactions are fraudulent
- **High-Risk Types**: TRANSFER and CASH_OUT transactions show higher fraud rates
- **Balance Patterns**: Zero balance after transfer is a strong fraud indicator
- **Feature Importance**: Transaction amount and balance changes are key predictors

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Junid Ebadi**

---

*Built with ❤️ using Python, Scikit-learn, and Streamlit*


