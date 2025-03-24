# Spam SMS Detection

## Overview
This project implements a machine learning solution to classify SMS messages as spam or ham (non-spam). Using natural language processing techniques and supervised learning algorithms, the system achieves high accuracy in identifying unwanted messages.

## Problem Statement
The goal is to develop an SMS classification model that accurately identifies spam messages using a labeled dataset of SMS messages.

## Dataset
The dataset contains 5,572 SMS messages labeled as either 'ham' or 'spam'. It includes:
- 4,825 ham messages (86.6%)
- 747 spam messages (13.4%)

## Features
- Text preprocessing including lowercase conversion, special character removal, stopword removal, and stemming
- TF-IDF vectorization for feature extraction
- SMOTE for handling class imbalance

## Models Evaluated
- Naive Bayes (best performing with 98.39% accuracy)
- Random Forest (98.03% accuracy)
- Logistic Regression (98.39% accuracy)
- SVM (97.49% accuracy)

## Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/spam-sms-detection.git
cd spam-sms-detection

# Install dependencies
pip install -r requirements.txt

# Download NLTK resources
python -c "import nltk; nltk.download('stopwords'); nltk.download('punkt')"
```

## Usage
### Training the model
```bash
python main.py --mode train
```

### Making predictions
```bash
python predict.py --message "Your message here"
```

### Using the API
```bash
# Start the API server
python api.py

# Make a request
curl -X POST http://localhost:5000/predict -d "message=Your message here"
```

## Results
The Naive Bayes model achieved the highest performance with:
- 98.39% accuracy
- 94% precision for spam detection
- 94% recall for spam detection
- 94% F1-score for spam detection

## Visualization
![Model Comparison](model_comparison.png)
![Confusion Matrix](naive_bayes_confusion_matrix.png)

## Future Improvements
- Experiment with deep learning models like LSTM or BERT
- Add more features beyond text content (e.g., time of day, message length)
- Collect more diverse spam messages to improve detection