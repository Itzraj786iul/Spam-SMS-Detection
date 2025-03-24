# Spam SMS Detection

## Overview
This project implements a machine learning solution to classify SMS messages as spam or ham (non-spam). Using natural language processing (NLP) techniques and supervised learning algorithms, the system achieves high accuracy in detecting unwanted messages.

## Problem Statement
The goal is to develop an SMS classification model that accurately identifies spam messages using a labeled dataset of SMS messages.

## Dataset
The dataset contains **5,572 SMS messages**, labeled as either 'ham' or 'spam'.  
- **4,825 ham messages** (86.6%)  
- **747 spam messages** (13.4%)  

### **Preprocessing Steps**
- Convert text to lowercase
- Remove special characters and punctuation
- Stopword removal using **NLTK**
- Stemming using **Porter Stemmer**
- TF-IDF vectorization for feature extraction
- Handle class imbalance using **SMOTE (Synthetic Minority Over-sampling Technique)**

## Models Evaluated
| Model               | Accuracy  |
|--------------------|-----------|
| **Naive Bayes**   | **98.39%** |
| **Logistic Regression** | **98.39%** |
| Random Forest     | 98.03%    |
| SVM               | 97.49%    |

## Installation
```bash
# Clone the repository
git clone https://github.com/Itzraj786iul/Spam-SMS-Detection.git
cd Spam-SMS-Detection

# Install dependencies
pip install -r requirements.txt

# Download NLTK resources
python -c "import nltk; nltk.download('stopwords'); nltk.download('punkt')"
```

## Usage
### **Train the Model**
```bash
python main.py --mode train
```

### **Make Predictions**
```bash
python predict.py --message "Congratulations! You've won a free prize!"
```


## Results
The **Naive Bayes** and **Logistic Regression** models performed the best with:
- **98.39% accuracy**
- **94% precision** for spam detection
- **94% recall** for spam detection
- **94% F1-score** for spam detection


## Future Improvements
- **Try deep learning models** (e.g., **LSTM, BERT** for better feature extraction)
- **Use ensemble learning** (stacking multiple models for improved accuracy)
- **Deploy in real-world applications** (integrate with an SMS spam detection API)
- **Expand dataset** (collect real-world spam messages to improve detection)