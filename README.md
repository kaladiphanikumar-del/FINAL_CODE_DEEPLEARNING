# FINAL_CODE_DEEPLEARNING
Multilingual fake news detection system

🌍 Multilingual Fake News Detection System
📌 Project Overview

This project is a Multilingual Fake News Detection System designed to classify news as real or fake across multiple languages. It supports:

English
Hindi
Bengali

The application is built with Streamlit for an interactive user interface and leverages advanced NLP models for accurate predictions.

📂 Dataset
Dataset sourced from KaggleHub
Includes multilingual news data in English, Hindi, and Bengali
Initial preprocessing steps:
Loaded and explored dataset structure
Examined data shape and column distributions
🧹 Data Preparation
Combined datasets from all three languages
Created unified structure with common columns
Generated labels:
True → Real news
Fake → Fake news
Final Dataset Processing
Removed empty text entries
Eliminated duplicate records
Final dataset size: 66,181 rows
🏗️ Feature Engineering
Combined title and text into a single column: full_text
Encoded labels into numeric format: label_num
Created a clean modeling dataframe
🔀 Data Splitting
Used stratified splitting to maintain class balance
Split into:
Training set
Validation set
Test set
📊 Baseline Model
Feature extraction using TF-IDF
Classification using Logistic Regression
Served as a benchmark for model comparison
🤗 Hugging Face Integration
Dataset converted into DatasetDict format
Custom evaluation metrics implemented:
Accuracy
Precision
Recall
F1-score
🧠 Deep Learning Models
🔹 mBERT (Multilingual BERT)
Model: bert-base-multilingual-cased
Tokenization length: 256
Trained for 1 epoch
🔹 XLM-RoBERTa
Model: xlm-roberta-base
Tokenization length: 128
Achieved best performance
🏆 Model Selection
XLM-RoBERTa selected as the final model
Achieved highest F1-score
Evaluated performance across all languages
Saved in FP16 format for efficiency
🚀 Streamlit Application
Loads trained XLM-RoBERTa model
Loads weights from .pth file
User inputs news text
Outputs:
Prediction (Real/Fake)
Confidence score
💻 How to Run
# Clone the repository
git clone <your-repo-link>

# Navigate to project folder
cd multilingual-fake-news-detection

# Install dependencies
pip install -r requirements.txt

# Run Streamlit app
streamlit run app.py
📈 Future Improvements
Add more languages
Improve model training with larger datasets
Deploy on cloud platforms
Enhance UI/UX
📜 License

This project is open-source and available under the MIT License.
