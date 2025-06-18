# Sentence-Word-tokenization-Stemming-Lemmatization

# Sentence, Word Tokenization & Stemming/Lemmatization 🧠

A Python-based toolkit demonstrating foundational NLP techniques including tokenization, contraction handling, stemming, lemmatization, and stop-word filtering using NLTK & spaCy.

---

## 📦 Features

- **Sentence & Word Tokenization**  
  Uses `TweetTokenizer` for informal text and `MWETokenizer` for multi-word expressions like "New York" :contentReference[oaicite:1]{index=1}.

- **Contraction Expansion**  
  Converts contractions (e.g., "I'm", "you're") into expanded forms ("I am", "you are") using a custom function :contentReference[oaicite:2]{index=2}.

- **Stemming**  
  Applies both Porter and Snowball stemmers to reduce words to their root forms :contentReference[oaicite:3]{index=3}.

- **Lemmatization**  
  Leverages spaCy's `en_core_web_sm` to derive dictionary lemmas contextually :contentReference[oaicite:4]{index=4}.

- **Stop Word Filtering**  
  Removes common stop words with NLTK’s predefined list :contentReference[oaicite:5]{index=5}.

---

## 🧩 Requirements

- Python 3.x  
- [NLTK](https://www.nltk.org/)  
- [spaCy](https://spacy.io/) and its English model `en_core_web_sm`

---

## 🚀 Installation

```bash
pip install nltk spacy
python -m spacy download en_core_web_sm

python
>>> import nltk
>>> nltk.download('punkt')       # Tokenizers
>>> nltk.download('stopwords')   # Stop-word corpus
>>> nltk.download('wordnet')     # Lemmatizer resources

````

## ⚙️ Usage
1. Tokenization

from nltk.tokenize import TweetTokenizer
tokenizer = TweetTokenizer()
tokenizer.tokenize("I'm happy you're here.")


2. Expand Contractions
   expand_contractions_clitic("I'm happy you're here.")

3.from nltk.tokenize import MWETokenizer
tokenizing_multiword("I'm going to New York tomorrow.")

4. stemming(["python", "running", "ran"])

5. lemmatizing("am is are was were")

6. tokenize_and_stop_word_filteration("This is an example …")


## 🧪 Examples

text = "I'm going to New York. I can't wait!"
print("Tokens:", tokenizer.tokenize(text))
print("Expanded:", expand_contractions_clitic(text))
print("Lemmas:", lemmatizing(text))
print("Stemmed:", stemming(tokenizer.tokenize(text)))
print("Filtered:", tokenize_and_stop_word_filteration(text))


## 🗂️ File Structure

.
├── tokenize_lemmatize.py    # Main implementation file
└── README.md                # This documentation

## 🔍 About

A concise demonstration of multiple essential text preprocessing steps in NLP using Python’s go-to libraries like NLTK and spaCy. The project provides a foundational understanding of how raw text can be cleaned, normalized, and made ready for downstream NLP tasks.

---

## ✨ Acknowledgements

This project draws from examples and implementations in various NLP tutorials and GitHub repositories, adapted and consolidated here:

- **NLTK & spaCy Tutorials**  
  - [keremkargin.medium.com](https://keremkargin.medium.com)  
  - [GitHub Repositories](https://github.com/search?q=nlp+tokenization+spacy+nltk)  
  - [arXiv Research Papers](https://arxiv.org)

- **Practical Guides on Tokenization, Stemming, Lemmatization**  
  - [keremkargin.medium.com](https://keremkargin.medium.com)  
  - [GitHub NLP Examples](https://github.com/topics/nlp-tokenization)  
  - [arXiv.org NLP Resources](https://arxiv.org)

---

## 🚧 Future Enhancements

- Add **Part-of-Speech (POS) Tagging**, **Named Entity Recognition (NER)**, and **Dependency Parsing**.
- Create fine-tuned pipelines for **multiple languages** or **specific domains**.
- Improve contraction handling with a **more comprehensive dictionary-based mapping system**.
- Include a **Command Line Interface (CLI)** or **Jupyter Notebook** for interactive usage and experimentation.

---
