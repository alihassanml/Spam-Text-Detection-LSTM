# Text Classification using LSTM: Spam or Ham

## 1. Introduction
This project aims to classify text messages as either spam or ham (non-spam) using a Long Short-Term Memory (LSTM) neural network. LSTM networks are well-suited for sequential data and can capture long-range dependencies, making them ideal for text classification tasks.

## 2. Dataset
The dataset consists of labeled text messages. Each message is labeled as either "spam" or "ham." The dataset is preprocessed to remove noise, convert text to lowercase, and tokenize the words.

## 3. Data Preprocessing
- **Text Cleaning:** Remove special characters, punctuation, and numbers.
- **Tokenization:** Convert text into a sequence of tokens (words).
- **Padding:** Ensure all sequences have the same length by padding shorter sequences.
- **Label Encoding:** Convert labels ("spam" or "ham") to binary values.

## 4. Model Architecture
The LSTM model consists of the following layers:
- **Embedding Layer:** Converts words into dense vectors.
- **LSTM Layer:** Captures sequential dependencies in the text.
- **Dense Layer:** Fully connected layer with ReLU activation.
- **Output Layer:** Sigmoid activation for binary classification.

## 5. Training
- **Loss Function:** Binary Crossentropy.
- **Optimizer:** Adam.
- **Metrics:** Accuracy.

The model is trained on a training set with validation to monitor overfitting. Early stopping is used to halt training when validation performance stops improving.

## 6. Evaluation
The model is evaluated using accuracy, precision, recall, and F1-score. Confusion matrix and ROC curve analysis are also performed.

## 7. Results
- The LSTM model achieved high accuracy on both the training and validation datasets, effectively distinguishing between spam and ham messages.

## 8. Conclusion
The LSTM-based model successfully classifies text messages as spam or ham with high accuracy. This approach can be extended to other text classification tasks with minor adjustments.
