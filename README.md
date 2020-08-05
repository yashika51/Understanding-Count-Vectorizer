# Understanding-Count-Vectorizer

This repository contains complete code for the article Understanding Count Vectorizer. Access the article [here](https://medium.com/@yashika51/understanding-count-vectorizer-5dd71530c1b)

![](https://unsplash.com/photos/BVyNlchWqzs)

Whenever we work on any NLP related problem, we process a lot of textual data. The textual data after processing needs to be fed into the model.
Since the model doesn’t accept textual data and only understands numbers, this data needs to be vectorized.

### What do I mean by vectorized?

Before we use text for modeling we need to process it. The steps include removing stop words, lemmatizing, stemming, tokenization, and vectorization. Vectorization is a process of converting the text data into a machine-readable form. The words are represented as vectors.
However, our main focus in this article is on Count Vectorizer. Let’s get started by understanding the Bag of Words model:

### Bag of Words(BoW)

As already mentioned, we cannot process text directly, so we need to convert it into numbers. The Bag of Words(BoW) model is a fundamental (and old way) of doing this.
The model is very simple as it discards all the information and order of the text and just considers the occurrences of the word. It converts the documents to a fixed-length vector of numbers.
A unique number is assigned to each word. Within the length of the vocabulary(vocabulary means a collection of all the unique words), the frequency of words is assigned. This is the encoding of the words, in which we are focusing on the representation of the word and not on the order of the word.
There are multiple ways with which we can define what this ‘encoding’ would be. Our focus in this post is on Count Vectorizer.

### Count Vectorizer:

CountVectorizer tokenizes(tokenization means dividing the sentences in words) the text along with performing very basic preprocessing. It removes the punctuation marks and converts all the words to lowercase.
The vocabulary of known words is formed which is also used for encoding unseen text later.
An encoded vector is returned with a length of the entire vocabulary and an integer count for the number of times each word appeared in the document. The image below shows what I mean by the encoded vector.

Count Vectorizer sparse matrix representation of words. (a) is how you visually think about it. (b) is how it is really represented in practice.
The row of the above matrix represents the document, and the columns contain all the unique words with their frequency. In case a word did not occur, then it is assigned zero correspondings to the document in a row.

Imagine it as a one-hot encoded vector and due to that, it is pretty obvious to get a sparse matrix with a lot of zeros.

For examples check out the notebook.

Open the notebook in Colab and play with the code.

Feel Free to drop any doubts on [Twitter](https://twitter.com/yashika51) and [Linkedin](https://www.linkedin.com/in/yashikasharma5174/)
