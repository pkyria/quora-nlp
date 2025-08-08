# Quora Question Pairs Similarity

This project focuses on building  machine learning models to determine whether two questions on Quora are semantically similar. It leverages natural language processing (NLP) techniques to analyze and classify question pairs as duplicates or not.

## Task

Given a pair of questions, predict whether they are duplicates (i.e., ask the same thing) or not.

## Dataset

The dataset used is the **Quora Question Pairs** dataset, originally provided as part of a Kaggle competition.

- **Columns**:
  - `id`: ID of the pair.
  - `qid1`, `qid2`: IDs of the individual questions.
  - `question1`, `question2`: The text of the two questions.
  - `is_duplicate`: Target variable (1 if questions are duplicates, 0 otherwise).
 
## Approach

The task is a **binary classification** problem. The general pipeline is:

1. **Preprocessing**:
   - Lowercasing, punctuation removal, stopword removal.
   - Tokenization and stemming/lemmatization (when beneficial).
   - Handling missing values.

2. **Feature Engineering**:
   - TF-IDF vectors
   - Cosine similarity
   - Word embeddings (Sentence-BERT, Word2Vec)
   - Hand-crafted features (question length difference, common word count, etc.)

3. **Modeling**:
   - Traditional ML models: LightGBM, XGBoost
   - Deep Learning (LSTM)
   
4. **Evaluation**:
   - Accuracy, Precision, Recall, F1 Score, Log loss

5. **Results**:
<img width="1040" height="717" alt="image" src="https://github.com/user-attachments/assets/170ac19d-b7b4-46cc-81a2-d659e045b00a" />

