# RNN-Based Text Generation

## Aim

To implement a Recurrent Neural Network (RNN) for text generation and evaluate its ability to generate meaningful text by predicting the next word in a sequence.

## Description

This experiment uses the **Tiny Shakespeare** dataset to train an RNN-based next-word prediction model. The model learns patterns and relationships between words from Shakespearean text and uses the learned patterns to generate new text from a given seed phrase.

The text data is converted into lowercase and punctuation is removed during preprocessing. The text is then divided into individual words, and each unique word is assigned an integer index. Input sequences of 20 words are created, where the next word acts as the prediction target.

The data is divided into training and validation sets. The model is trained to predict the next word based on the preceding sequence and its performance is evaluated using training and validation accuracy and loss.

## Dataset

The experiment uses the **Tiny Shakespeare** dataset, which contains text from Shakespeare's works.

Dataset source:

https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt

## Data Preparation

The following preprocessing operations are performed:

* The Shakespeare text is loaded from the dataset.
* Text is converted to lowercase.
* Punctuation is removed to reduce unnecessary variations in the vocabulary.
* The text is split into individual words.
* A vocabulary of unique words is created.
* Words are converted into integer indices.
* Sequences containing the previous 20 words are created for next-word prediction.
* Padding is applied so that all input sequences have a fixed length.
* The dataset is divided into 80% training data and 20% validation data.

## Training and Evaluation

The model is trained using the generated word sequences. Training and validation accuracy and loss are monitored throughout the training process.

Early stopping is used based on validation loss to reduce unnecessary training and help control overfitting.

The observed results show that the training accuracy increases as the model learns the training data, while validation accuracy remains considerably lower. The difference between training and validation performance indicates that the model experiences overfitting.

Since the model predicts the exact next word from a large vocabulary, the validation accuracy is relatively low compared with the training accuracy.

## Text Generation

After training, the model is used to generate text from different seed phrases, including:

* `the king`
* `my lord`
* `love is`
* `to be`
* `when i`

The model repeatedly predicts the next word and uses the predicted word as part of the input for the following prediction.

The generated text contains Shakespeare-like words and phrases, showing that the model has learned some patterns from the training data. However, repetitive words and phrases are also observed in several generated sequences.

## Observations

* The model successfully learns relationships between words in the training data.
* A sequence length of 20 provides previous-word context for next-word prediction.
* Padding ensures that all sequences have the same input size.
* Training accuracy is higher than validation accuracy, indicating overfitting.
* SimpleRNN has difficulty maintaining information over longer sequences.
* Generated text can contain meaningful word combinations but may also become repetitive.
* The quality of generated text depends on the learned word patterns and the context provided by the seed phrase.

## Result

The RNN-based text generation experiment was successfully implemented using the Tiny Shakespeare dataset. The model learned sequential word patterns and generated text from different seed phrases. The experiment also demonstrated the effects of sequence length, padding, model training, validation, and overfitting on text-generation performance.

## Conclusion

The experiment demonstrates how Recurrent Neural Networks can be used for next-word prediction and text generation. The trained model is able to generate text based on a given seed phrase and reproduce some patterns present in Shakespeare's writing.

The results also show that SimpleRNN-based text generation has limitations, particularly in maintaining longer contextual relationships and avoiding repetitive predictions. Overall, the experiment provides an understanding of how sequential data can be processed and used for generating text.
