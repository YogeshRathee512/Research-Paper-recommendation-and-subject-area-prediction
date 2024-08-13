# 📄 Research Paper Recommendation and Subject Area Prediction

![Research Paper Recommendation](https://img.shields.io/badge/Research%20Paper%20Recommendation-Brightgreen)

## 🎯 Objective
Recommend research papers and predict subject areas using transfer learning.

## Procedure
Convert string in input dataset to literal eval ["'cs.LG','cs.CV'"] --> ['cs.LG','cs.CV']
Create string look up layer to generate a vacbolaruy out of all unique values in terms coloumn and apply multi-hot encoding (to convert terms coloumn)
Create a vacbolury using all unique words and apply text vectorization using bi gramns and tf_idf (to convert abstract coloumns)
Used a multiLayer perceptron to predict the label of each research paper



## 📸 Screenshots

### 📝 Input
![Input Screenshot](https://github.com/user-attachments/assets/0e2babba-ba2e-4388-a2a7-76abaa46e274)

### 📊 Output
![Output Screenshot](https://github.com/user-attachments/assets/c6c8719b-5f3a-44d7-8ca4-b74571dde80b)


## 📝 Description
- **🔄 Comparison**: Compared transfer learning (**all-MiniLM-L6-v2**) with a Multi-Layer Perceptron for recommending research papers.
- **🔧 Text Processing**: Performed text vectorization ,data cleaning and data preprocessing.
- **🚀 Deployment**: Deployed the model using a **Streamlit** interface (on a local machine).

## 📂 Dataset
[ArXiv Paper Abstracts Dataset](https://www.kaggle.com/datasets/spsayakpaul/arxiv-paper-abstracts/data)
