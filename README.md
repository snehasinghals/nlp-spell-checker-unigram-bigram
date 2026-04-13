#  NLP Spell Checker using Unigram & Bigram Models

##  Project Overview
This project implements a Spell Checker using Natural Language Processing (NLP) techniques.  
It uses Unigram and Bigram Language Models along with Edit Distance (Levenshtein distance) to correct misspelled words and sentences.

The system performs both:
- Word-level correction
- Context-aware sentence correction using bigram probabilities

---

##  Technologies Used
- Python  
- NumPy  
- Scikit-learn  
- TextDistance  
- Collections (Counter, defaultdict)  

---

##  Dataset

The model is trained on a custom text corpus (`Training.txt`) which is preprocessed to build vocabulary and language models.

###  Data Preprocessing Steps:
- Lowercasing text  
- Removing timestamps  
- Removing numbers  
- Removing punctuation  
- Tokenization into words  

---

##  Language Models

###  Unigram Model
- Calculates probability of each word independently  
- Used for basic spell correction  

###  Bigram Model
- Calculates probability of word given previous word  
- Provides **context-aware correction**  

---

##  Project Workflow

### 1. Data Cleaning
- Raw text is cleaned and converted into tokens  

### 2. Vocabulary Creation
- Unique words stored as vocabulary  
- Word frequencies calculated  

### 3. Model Building
- Unigram probabilities computed  
- Bigram counts and probabilities calculated  

### 4. Error Correction
- Uses Levenshtein Distance to find similar words  
- Combines:
  - Word probability  
  - Error probability  

### 5. Sentence Correction
- Unigram: word-by-word correction  
- Bigram: context-based correction  

---

##  Test Dataset

The model is evaluated on a custom dataset of incorrect and correct sentences.

###  Example Input (Incorrect Sentences)
```python
"i dont no what you doing"
"this movi is amazng"
"we shold go hom now"
