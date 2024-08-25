# Spam vs. Ham Text Classification Using LSTM

This project focuses on classifying text messages as either spam or ham (not spam) using a Long Short-Term Memory (LSTM) neural network. The LSTM model is designed to capture the sequential patterns in the text, enabling effective classification of messages.

## Table of Contents
- [Overview](#overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview
This project demonstrates the use of LSTM, a type of Recurrent Neural Network (RNN), to classify text messages into spam or ham. The model is trained on a labeled dataset and can be used to predict whether new incoming messages are spam or not.

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/alihassanml/Spam-Text-Detection-LSTM.git
    cd spam-ham-classification
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Dataset
The dataset used for training consists of labeled text messages where each message is tagged as "spam" or "ham". The dataset should be preprocessed to remove noise, tokenize the text, and convert it into sequences of word indices.

## Model Architecture
The model is built using the following layers:
- **Embedding Layer:** Converts input words into dense vectors of fixed size.
- **LSTM Layers:** Three LSTM layers with 150 units each to capture sequential dependencies.
- **Dropout Layers:** Applied to prevent overfitting.
- **Dense Layer:** A single neuron with a sigmoid activation function for binary classification.

## Training
The model is trained using the binary cross-entropy loss function and the Adam optimizer. Early stopping and learning rate reduction strategies are applied to prevent overfitting and ensure better convergence.

## Evaluation
The model’s performance is evaluated using metrics such as accuracy, precision, recall, and F1-score. The confusion matrix helps in understanding the types of errors made by the model.

### Confusion Matrix
\[
\begin{bmatrix}
1581 & 6 \\
29 & 223
\end{bmatrix}
\]
- **Accuracy:** 98.09%
- **Precision:** 97.42%
- **Recall:** 88.53%
- **F1-Score:** 92.79%

## Results
The model achieved high accuracy, precision, and F1-score, indicating it is effective in distinguishing spam from ham. However, the model can be further fine-tuned to improve recall, reducing false negatives.

## Usage
To use the model, you can run the `predict.py` script with a new text message as input:
```bash
python predict.py --message "Your free coupon is waiting! Click now!"
```

The script will output whether the message is spam or ham.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License.
