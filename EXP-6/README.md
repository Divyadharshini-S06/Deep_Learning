# LSTM-Based Sentiment Analysis

## Aim

To implement an LSTM neural network for sentiment analysis and classify movie reviews as positive or negative.

## Description

This experiment uses the **IMDB Movie Reviews dataset** to train an LSTM-based sentiment classification model. The model learns sequential patterns in review text and predicts the sentiment of a given review.

The text is converted to lowercase, cleaned, tokenized, and transformed into integer sequences. The sequences are padded to a fixed length of 200 tokens before being passed to the LSTM model.

The model consists of an Embedding layer, an LSTM layer, a Dropout layer, and a Dense output layer with sigmoid activation.

## Dataset

The experiment uses the IMDB dataset containing 50,000 movie reviews labeled as positive or negative.

Dataset source:

https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

After removing 418 duplicate rows, 49,582 reviews were used.

## Data Preparation

The following preprocessing operations are performed:

- The dataset is loaded directly into Google Colab using KaggleHub.
- Missing values and duplicate reviews are checked.
- Text is converted to lowercase and unnecessary characters are removed.
- Sentiment labels are converted into numerical values: negative = 0 and positive = 1.
- Reviews are tokenized using a vocabulary of 20,000 words.
- Text is converted into integer sequences and padded to 200 tokens.
- The dataset is divided into training, validation, and testing sets.

## Training and Evaluation

The LSTM model is trained using the Adam optimizer and binary cross-entropy loss. Early stopping monitors validation loss and restores the best model weights.

The model achieved the following results on the test dataset:

- **Test accuracy:** 86.43%
- **Precision:** 89.82%
- **Recall:** 82.28%
- **F1-score:** 85.89%
- **Test loss:** 0.395

Training accuracy increased over the recorded epochs, while validation accuracy decreased slightly and validation loss increased. This indicates possible overfitting.

## Sentiment Prediction

The trained model is tested using new movie-review sentences with different sentiments. Each review is preprocessed and converted into a padded sequence using the same tokenizer used during training.

The model predicts a positive probability, which is used to classify the review as positive or negative.

All six example reviews were classified correctly. However, this small sample does not represent the model's overall performance on unseen reviews.

## Observations

- The LSTM model learns sequential patterns from movie reviews.
- Tokenization and padding convert textual data into a suitable format for the model.
- The model achieved 86.43% test accuracy.
- The validation results indicate possible overfitting.
- The model correctly classified the six sample reviews.
- Prediction performance may vary for reviews containing sarcasm, mixed opinions, or unfamiliar wording.

## Result

The LSTM-based sentiment analysis experiment was successfully implemented using the IMDB Movie Reviews dataset. The model classified reviews as positive or negative and achieved 86.43% accuracy on the test dataset.

## Conclusion

This experiment demonstrates how LSTM networks can be used for sentiment classification by learning sequential patterns in text. The evaluation metrics show that the model performs reasonably well on the IMDB test dataset. The experiment also highlights the importance of preprocessing, sequence padding, validation, and overfitting control in deep learning.

