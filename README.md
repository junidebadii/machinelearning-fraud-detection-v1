# Fraud Detection Machine Learning Project

A comprehensive machine learning project for detecting fraudulent financial transactions using a Streamlit web application and a trained machine learning model.

## 🎯 Project Overview

This project implements a fraud detection system that can identify potentially fraudulent financial transactions based on transaction characteristics such as amount, balance changes, and transaction type. The system uses a Logistic Regression model trained on a large dataset of financial transactions.

## 📊 Dataset

The model is trained on the [Fraud Detection Dataset](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download) from Kaggle, which contains over 6.3 million financial transactions with the following features:

- **step**: Time step of the transaction
- **type**: Transaction type (PAYMENT, TRANSFER, CASH_OUT, DEPOSIT)
- **amount**: Transaction amount
- **nameOrig**: Sender account identifier
- **oldbalanceOrg**: Sender's balance before transaction
- **newbalanceOrig**: Sender's balance after transaction
- **nameDest**: Receiver account identifier
- **oldbalanceDest**: Receiver's balance before transaction
- **newbalanceDest**: Receiver's balance after transaction
- **isFraud**: Fraud indicator (target variable)
- **isFlaggedFraud**: Flagged fraud indicator

## 🏗️ Project Structure

```
fraud-detect-ml-copy/
├── README.md                           # This file
├── fraud_detection.py                  # Streamlit web application
├── analysis_model.ipynb                # Jupyter notebook with EDA and model training
├── fraud_detection_pipeline.pkl        # Trained machine learning pipeline
└── AIML Dataset.csv                    # Training dataset (not included in repo)
```

## 🚀 Features

- **Interactive Web Interface**: User-friendly Streamlit app for real-time fraud detection
- **Real-time Prediction**: Instant fraud detection for new transactions
- **Comprehensive Analysis**: Extensive exploratory data analysis and feature engineering
- **Production-Ready Model**: Trained and serialized machine learning pipeline

## 🛠️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd fraud-detect-ml-copy
   ```

2. **Install required dependencies**
   ```bash
   pip install streamlit pandas numpy matplotlib seaborn scikit-learn joblib
   ```

3. **Download the dataset**
   - Visit [Kaggle Dataset](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download)
   - Download and place `AIML Dataset.csv` in the project directory

## 🎮 Usage

### Running the Web Application

```bash
streamlit run fraud_detection.py
```

The app will open in your browser where you can:
1. Select transaction type
2. Enter transaction amount
3. Input sender and receiver balance details
4. Get instant fraud prediction

### Model Training

Open `analysis_model.ipynb` in Jupyter to:
- Explore the dataset
- View data visualizations
- Understand feature engineering
- See model training process
- Generate the trained pipeline

## 📈 Model Performance

The Logistic Regression model achieves:
- **Accuracy**: 94%
- **Precision**: 100% for non-fraudulent, 2% for fraudulent transactions
- **Recall**: 94% for both classes
- **F1-Score**: 97% for non-fraudulent, 4% for fraudulent transactions

*Note: The low precision for fraudulent transactions is common in highly imbalanced fraud detection datasets.*

## 🔍 Key Insights

- **Fraud Rate**: Only 0.13% of transactions are fraudulent
- **High-Risk Types**: TRANSFER and CASH_OUT transactions have higher fraud rates
- **Balance Patterns**: Zero balance after transfer is a strong fraud indicator
- **Feature Importance**: Transaction amount and balance changes are key predictors

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

Junid Ebadi

---


