# Transformer-Based Movie Review Sentiment Analysis

A Deep Learning and Natural Language Processing (NLP) project that classifies movie reviews as **positive or negative** using a Transformer encoder built with TensorFlow and Keras. The project includes an interactive Gradio web interface.

## Project Overview

Sentiment analysis is a Natural Language Processing task that identifies the emotional tone of text. This project uses the IMDB movie review dataset to train a neural network that predicts whether a movie review expresses positive or negative sentiment.

## Features

- Movie review sentiment classification
- Transformer encoder with multi-head self-attention
- Token and positional embeddings
- Text preprocessing and sequence padding
- Binary sentiment classification using a sigmoid output
- Model training, validation, and evaluation
- Accuracy and loss visualization
- Interactive Gradio web interface

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Gradio
- Jupyter Notebook

## Model Architecture

The model consists of the following components:

1. **Input layer:** Receives integer-encoded movie reviews.
2. **Token and positional embeddings:** Represent token meaning and position.
3. **Transformer block:** Uses multi-head self-attention, residual connections, layer normalization, and a feed-forward network.
4. **Global average pooling:** Aggregates token representations while accounting for padding masks.
5. **Dense layers:** Learn features for sentiment classification.
6. **Sigmoid output:** Produces a score between 0 and 1 for binary classification.

## Dataset

This project uses the IMDB movie review dataset available through Keras.

- Training examples: 25,000
- Testing examples: 25,000
- Task: Binary sentiment classification
- Input sequence length: 200 tokens
- Vocabulary limit: 10,000 or 20,000 tokens, depending on the training configuration

## Project Structure

```text
transformer-sentiment-analysis/
├── app.py
├── train.py
├── requirements.txt
├── README.md
├── .gitignore
├── models/
├── notebooks/
└── screenshots/
```

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/transformer-sentiment-analysis.git
cd transformer-sentiment-analysis
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Activate it on macOS or Linux:

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Training

Run the training script:

```bash
python train.py
```

The script should load the IMDB dataset, construct and compile the Transformer model, train it, evaluate it, and save the trained model.

Alternatively, open the notebook in `notebooks/` and execute the cells in order.

## Run the Web Application

After training and saving the model:

```bash
python app.py
```

Open the local URL displayed by Gradio in your browser. Enter a movie review and click the sentiment analysis button.

## Evaluation

The model can be evaluated using test loss and test accuracy. Training and validation curves can also help identify overfitting.

Add your actual test results here after training:

- Test accuracy: Add your measured result
- Test loss: Add your measured result

## Limitations

- The model predicts positive or negative sentiment only.
- Predictions depend on the quality and characteristics of the training dataset.
- The displayed probability is a model score, not a guarantee of correctness.
- The IMDB vocabulary and preprocessing must be consistent between training and inference.

## Future Improvements

- Compare the Transformer with LSTM and CNN models.
- Improve preprocessing and out-of-vocabulary handling.
- Add a confusion matrix and precision, recall, and F1-score.
- Deploy the application on a hosting platform.
- Experiment with pretrained language models.

## Author

**YOUR NAME**

GitHub: https://github.com/YOUR_USERNAME

## License

This project can be released under the MIT License by adding a `LICENSE` file containing the MIT license text.

