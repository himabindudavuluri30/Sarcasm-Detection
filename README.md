
## Smart Sarcasm Detection System

Developed an NLP-based **Sarcasm Detection System** that analyzes textual input and predicts whether the given sentence is **sarcastic or non-sarcastic**, along with a confidence score. The project addresses the challenge of detecting sarcasm in text, where the literal meaning of words may differ from the intended meaning.

The system begins by preprocessing the input text through **lowercasing, URL removal, and removal of non-alphabetic characters**. The cleaned text is then converted into numerical representations using **TF-IDF (Term Frequency–Inverse Document Frequency)**, allowing the model to capture important words and their relevance within the dataset.

To improve the detection of subtle sarcastic patterns, the system also incorporates **handcrafted linguistic and irony-based features**. These features identify common sarcasm cues such as phrases like "yeah right", "obviously", "totally", "as if", and "thanks a lot", along with contrast indicators such as "but", "however", and "although". Additional irony features detect combinations of positive and negative words, polite and rude expressions, self-negation, and changes in sentiment polarity between consecutive words.

The TF-IDF representation and handcrafted features are combined into a single feature vector and used to train a **Random Forest Classifier**. The dataset is divided into training and testing sets, and the model is evaluated using **accuracy, precision, recall, and F1-score**. The trained model and TF-IDF vectorizer are serialized using **Joblib** for later use in the application.

The trained model is integrated into a **Flask-based web application**, where users can enter text and receive a real-time prediction. The application processes the input using the same preprocessing and feature-extraction pipeline used during training, obtains the model's probability prediction, and displays whether the text is **Sarcastic** or **Not Sarcastic**, together with a sarcasm confidence score.

### Key Features

* Text preprocessing and normalization
* TF-IDF-based text representation
* Handcrafted sarcasm and irony feature extraction
* Positive-negative sentiment contrast detection
* Random Forest classification
* Probability-based confidence scoring
* Real-time prediction through a Flask web interface
* Model and vectorizer persistence using Joblib

### Technologies Used

**Python, Pandas, NumPy, Scikit-learn, TF-IDF, Random Forest, Flask, Joblib, HTML/CSS, NLP**

### Workflow

**User Input → Text Cleaning → TF-IDF + Linguistic Features → Feature Combination → Random Forest → Sarcasm Probability → Prediction + Confidence Score**

### Learning Outcomes

* Applied NLP preprocessing techniques to real-world text
* Learned feature engineering for sarcasm and irony detection
* Implemented TF-IDF vectorization for text classification
* Built and evaluated a machine learning classification model
* Integrated a trained ML model into a Flask web application
* Implemented probability-based prediction and confidence scoring
* Understood the complete pipeline from dataset preprocessing to model deployment
