# 📄 Research Paper Recommendation and Subject Area Prediction

![Research Paper Recommendation](https://img.shields.io/badge/Research%20Paper%20Recommendation-Brightgreen)

<img width="617" alt="Research Paper Recommendation" src="https://github.com/user-attachments/assets/9efa9874-1ab4-4dfd-9d6e-c83be2a763cf">

## 🎯 Objective
Recommend research papers and predict subject areas using transfer learning.

## 📂 Dataset
[ArXiv Paper Abstracts Dataset](https://www.kaggle.com/datasets/spsayakpaul/arxiv-paper-abstracts/data)

## 🛠 Procedure

1. **📝 Data Preparation**:
   - Convert strings in the input dataset to literal eval format (e.g., `["'cs.LG','cs.CV'"]` --> `['cs.LG','cs.CV']`).
   - Create a string lookup layer to generate a vocabulary from all unique values in the terms column and apply multi-hot encoding.

2. **🔠 Text Vectorization**:
   - Construct a vocabulary using all unique words from the abstracts.
   - Apply text vectorization using bi-grams and TF-IDF to the abstracts column.

3. **🤖 Model Training**:
   - Use a Multi-Layer Perceptron (MLP) to predict the label of each research paper (using abstracts and labels to predict titles and find similar research papers).

4. **🔍 Embedding and Recommendation**:
   - Utilize the `all-MiniLM-L6-v2` model from Sentence Transformers to perform word embedding on the title column.
   - Apply Cosine Similarity to find and recommend papers similar to a given input paper.

## 📸 Screenshots

### 📝 Input
![Input Screenshot](https://github.com/user-attachments/assets/0e2babba-ba2e-4388-a2a7-76abaa46e274)

### 📊 Output
![Output Screenshot](https://github.com/user-attachments/assets/c6c8719b-5f3a-44d7-8ca4-b74571dde80b)

## 📝 Description
- **🔄 Comparison**: Compared transfer learning (**all-MiniLM-L6-v2**) with a Multi-Layer Perceptron (MLP) for recommending research papers.
- **🔧 Text Processing**: Performed text vectorization, data cleaning, and preprocessing.
- **🚀 Deployment**: Deployed the model using a **Streamlit** interface (on a local machine).
