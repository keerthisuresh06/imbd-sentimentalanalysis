IMDb Sentiment Analysis using PyTorch



\## Project Overview

This project classifies IMDb movie reviews as positive or negative using a neural network built with PyTorch.



The goal was to understand the fundamentals of NLP and deep learning by building a sentiment classifier from scratch.



Dataset

\- 50,000 IMDb movie reviews

\- 25,000 positive reviews and 25,000 negative reviews

\- 40,000 reviews for training and 10,000 for testing

\- Stratified train-test split to preserve class balance



&#x20;Data Preprocessing

\- Removed HTML tags

\- Converted text to lowercase

\- Tokenised reviews using whitespace

\- Built the vocabulary using training data only

\- Replaced rare words with an unknown token

\- Padded or truncated reviews to 500 tokens



Model Architecture

\- Embedding layer: 64-dimensional word embeddings

\- Masked mean pooling: creates one vector per review while ignoring padding tokens

\- Linear layer: produces one sentiment logit

\- Binary cross-entropy with logits loss

\- Adam optimiser with a learning rate of 0.001



The model was trained for 3 epochs.



Results

The model achieved approximately \*\*89% accuracy\*\* on the held-out test set.



| Metric | Negative | Positive |

|---|---:|---:|

| Precision | 0.89 | 0.89 |

| Recall | 0.89 | 0.89 |

| F1-score | 0.89 | 0.89 |

| Support | 5,000 | 5,000 |



\## Technologies

\- Python

\- PyTorch

\- Pandas

\- Scikit-learn

\- Jupyter Notebook



\## Project Files

\- notebook800886bb82.ipynb — preprocessing, model training and evaluation

\- sentiment\_model.pth — trained model weights

\- vocab.json - word-to-index vocabulary

\- config.json - model and preprocessing settings



\## Limitations

\- Uses simple whitespace tokenisation.

\- Mean pooling does not preserve word order.

\- Word embeddings are learned from the training data rather than using a pretrained language model.

\- Results may vary with different random seeds and training settings.



\## Future Improvements

\- Compare against an LSTM or pretrained transformer.

\- Add a script for predicting the sentiment of new reviews.

\- Experiment with different embedding dimensions and pooling methods.



