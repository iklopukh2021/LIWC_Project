# NLTK Notes

Certainly! NLTK (Natural Language Toolkit) is a Python library that provides tools and resources for working with human language data, particularly for text analysis and natural language processing (NLP) tasks. In this guide, I'll introduce you to some basic NLTK functionalities and show you how to perform common NLP tasks using NLTK.

**Step 1: Installation**

First, you need to install NLTK. You can do this using pip, the Python package manager:

```bash
pip install nltk
```

**Step 2: Importing NLTK and Downloading Data**

After installation, you need to import NLTK and download some datasets and resources that NLTK provides. This can be done using the following commands in Python:

```python
import nltk
nltk.download('popular')
```

This will download commonly used datasets, including stopwords and example corpora, which are often used in NLP tasks.

**Step 3: Tokenization**

Tokenization is the process of splitting text into individual words or tokens. NLTK provides functions for tokenization:

```python
from nltk.tokenize import word_tokenize, sent_tokenize

text = "NLTK is a great library for natural language processing. It's easy to use."
words = word_tokenize(text)
sentences = sent_tokenize(text)

print("Tokenized words:", words)
print("Tokenized sentences:", sentences)
```

**Step 4: Stopword Removal**

Stopwords are common words (e.g., "the," "and," "is") that are often removed in NLP tasks because they don't provide much meaningful information. NLTK provides a list of stopwords, and you can use it to remove them from your text:

```python
from nltk.corpus import stopwords

text = "This is an example sentence with some stopwords."
words = word_tokenize(text)
filtered_words = [word for word in words if word.lower() not in stopwords.words('english')]

print("Filtered words:", filtered_words)
```

**Step 5: Stemming and Lemmatization**

Stemming and lemmatization are techniques used to reduce words to their root or base form. NLTK provides tools for both:

```python
from nltk.stem import PorterStemmer
from nltk.stem import WordNetLemmatizer

stemmer = PorterStemmer()
lemmatizer = WordNetLemmatizer()

word = "running"
stemmed_word = stemmer.stem(word)
lemmatized_word = lemmatizer.lemmatize(word, pos='v')  # pos='v' indicates it's a verb

print("Stemmed word:", stemmed_word)
print("Lemmatized word:", lemmatized_word)
```

**Step 6: Part-of-Speech Tagging**

Part-of-speech tagging assigns a part of speech (e.g., noun, verb, adjective) to each word in a sentence. NLTK provides a function for this:

```python
from nltk import pos_tag

text = "NLTK is a powerful library for natural language processing."
words = word_tokenize(text)
pos_tags = pos_tag(words)

print("Part-of-speech tags:", pos_tags)
```

These are some of the basic NLP tasks you can perform with NLTK. NLTK provides many more functionalities for more advanced NLP tasks like named entity recognition, sentiment analysis, and more. You can explore the NLTK documentation and tutorials for more in-depth information and examples: http://www.nltk.org/.