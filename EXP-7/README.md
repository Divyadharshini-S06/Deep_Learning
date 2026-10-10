# Text Preprocessing and Word2Vec Using NLTK

## Aim
To perform text preprocessing using NLTK and generate Word2Vec embeddings to analyze semantic relationships between words.

## Description
This experiment uses the Brown News Corpus for text preprocessing and Word2Vec embedding generation. The text is converted to lowercase, tokenized, filtered to remove punctuation and stop words, and lemmatized. A Skip-gram Word2Vec model is trained to generate word vectors and identify semantic relationships using cosine similarity.

## Dataset
- **Dataset:** Brown Corpus (News category)
- **Total sentences:** 4,623
- **Sentences after preprocessing:** 4,590
- **Total processed words:** 47,682
- **Vocabulary size:** 9,896

## Data Preprocessing
- Converted text to lowercase.
- Performed word tokenization.
- Removed punctuation and stop words.
- Applied lemmatization using WordNetLemmatizer.
- Prepared tokenized sentences for Word2Vec training.

## Word Frequency Analysis
The ten most frequent words were identified using NLTK's FreqDist. The most frequent words included:

- said: 406
- year: 260
- would: 249
- new: 241
- state: 223

A bar chart was generated to visualize the top ten words.

## Word2Vec Model
- **Model:** Skip-gram
- **Vector size:** 100
- **Context window:** 5
- **Minimum word frequency:** 2
- **Training epochs:** 10

The model generated 100-dimensional word vectors. The five most similar words to *government* were department, federal, local, nation, and program.

## Cosine Similarity Results
- year – day: 0.8999
- president – government: 0.8487
- city – state: 0.7697

The word pair **year – day** achieved the highest cosine similarity score of 0.8999, indicating the strongest contextual similarity among the selected pairs.

## Result
Text preprocessing was successfully performed using NLTK, and a Skip-gram Word2Vec model was trained on the Brown News Corpus. Word embeddings and cosine similarity scores were used to analyze relationships between words.

## Conclusion
The experiment demonstrated how text preprocessing improves text representation and how Word2Vec generates dense word embeddings to identify contextual and semantic relationships between words.
