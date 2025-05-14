# Information-Retrieval
Information Retrieval Project at Faculty of Science

# TF-IDF Calculator

This project implements a simple **TF-IDF (Term Frequency-Inverse Document Frequency)** algorithm to convert text into vector format based on the importance of words in a sentence. It demonstrates how to compute TF, IDF, and the final TF-IDF values using two example sentences.

---

## 📚 What is TF-IDF?

TF-IDF is a statistical measure used in Natural Language Processing to evaluate how important a word is in a document relative to a collection of documents.

- **TF (Term Frequency)** = (Number of times a word appears in a sentence) / (Total number of words in the sentence)
- **IDF (Inverse Document Frequency)** = log(Total number of sentences / Number of sentences containing the word)
- **TF-IDF** = TF × IDF

---

### Sentences

- **Sentence 1 (Sen1)**: `the cat sat on my face`
- **Sentence 2 (Sen2)**: `the dog sat on my bed`

---

### Step 1: Term Frequency (TF)

| Word  | Sen1 TF | Sen2 TF |
|-------|---------|---------|
| the   | 1/6     | 1/6     |
| cat   | 1/6     | 0       |
| sat   | 1/6     | 1/6     |
| on    | 1/6     | 1/6     |
| my    | 1/6     | 1/6     |
| face  | 1/6     | 0       |
| dog   | 0       | 1/6     |
| bed   | 0       | 1/6     |

---

### Step 2: Inverse Document Frequency (IDF)

| Word  | IDF        |
|-------|------------|
| the   | log(2/2) = 0   |
| cat   | log(2/1) = 0.3 |
| sat   | log(2/2) = 0   |
| on    | log(2/2) = 0   |
| my    | log(2/2) = 0   |
| face  | log(2/1) = 0.3 |
| dog   | log(2/1) = 0.3 |
| bed   | log(2/1) = 0.3 |

---

### Step 3: TF × IDF (TF-IDF)

| Word  | Sen1 TF-IDF | Sen2 TF-IDF |
|-------|-------------|-------------|
| the   | 0           | 0           |
| cat   | 0.115       | 0           |
| sat   | 0           | 0           |
| on    | 0           | 0           |
| my    | 0           | 0           |
| face  | 0.115       | 0           |
| dog   | 0           | 0.115       |
| bed   | 0           | 0.115       |

---

## ✅ Features

- Calculates TF for each word per sentence
- Calculates IDF for all unique words
- Multiplies TF and IDF to compute final TF-IDF vector
- Simple and understandable implementation

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open the main script.
3. Edit the input sentences as needed.
4. Run the script in Python.
5. Check the console output for TF, IDF, and TF-IDF values.

---

## 🛠 Technologies Used

- Python
- Math (`log` function)
- Core data structures (`lists`, `dictionaries`)

---

## 🔮 Future Improvements

- Support for multiple documents
- Add preprocessing (stopword removal, lowercasing)
- Export TF-IDF vectors to CSV or JSON
- Create web-based user interface

---

