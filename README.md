# Emoji Predictor RNN

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)

## 📋 Overview

The **Emoji Predictor** is an AI model that predicts emojis based on input text using an LSTM-based Recurrent Neural Network (RNN). The model leverages pre-trained GloVe word embeddings for better contextual understanding, enabling accurate emoji predictions.

## 🚀 Features

- **LSTM Model with Word Embeddings**: Utilizes GloVe embeddings for text preprocessing and a custom LSTM architecture for sequence modeling.
- **Two Model Variants**: Includes a single-layer LSTM and a double-layer LSTM for enhanced performance.
- **Emoji Visualization**: Outputs predictions in both text and emoji format using the `emoji` library.
- **Early Stopping and Model Checkpointing**: Integrated with Keras callbacks for training optimization.

## 📁 Project Structure

```
emoji-predictor-rnn/
│
├── data/
│   ├── train_emoji.csv
│   └── test_emoji.csv
│
├── glove/
│   └── glove.6B.50d.txt
│
├── models/
│   ├── model_v1.h5
│   └── model_v2.h5
│
├── Emoji_Predictor_RNN_Word_Embeddings.ipynb
├── README.md
└── requirements.txt
```

## 🛠️ Setup & Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Vamsi404/emoji-predictor-rnn.git
    cd emoji-predictor-rnn
    ```

2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Download GloVe Embeddings**:
   - Place the `glove.6B.50d.txt` file in the `glove/` directory.

4. **Run the Notebook**:
    - Open and run `Emoji_Predictor_RNN_Word_Embeddings.ipynb` in your preferred environment (e.g., Jupyter, Colab).

## 🧠 Model Details

The model takes in short text sequences and predicts one of the following emojis:

| Label | Emoji |
|-------|-------|
|   0   | ❤️    |
|   1   | ⚾    |
|   2   | 😀    |
|   3   | 😞    |
|   4   | 🍴    |

The model architecture uses an LSTM layer for sequential data, followed by dense layers with softmax activation for classification.

## 🔍 Example Predictions

Input: "I love programming"  
Output: ❤️

Input: "Let's play some ball"  
Output: ⚾

## 🖼️ Visualization

The notebook includes a section where you can visualize the predictions in both text and emoji format.

## 📈 Training and Evaluation

The model is trained with:
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam
- **Evaluation**: Accuracy on the test set

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check out the [issues page](https://github.com/Vamsi404/emoji-predictor-using-RNN/issues).
