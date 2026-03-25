# CSL 7640: Natural Language Understanding - Assignment 2

**Author:** Viswanadhapalli Sujay (Roll No: B22CS063)  
**Course:** CSL 7640: Natural Language Understanding  
**Instructor:** Dr. Anand Mishra  

---

## 📌 Overview

This repository contains the source code, datasets, results, and the final report for **Assignment 2** of CSL 7640.  

The project implements **sequence modeling** and **distributional semantics** from scratch using **PyTorch**, without relying on high-level NLP libraries.

### 🔹 Problem 1: Word Embeddings
Scraping localized academic data from the IIT Jodhpur web domain to train custom:
- Continuous Bag of Words (CBOW)
- Skip-gram with Negative Sampling (SGNS)

### 🔹 Problem 2: Character-Level Name Generation
Designing and comparing recurrent neural network architectures:
- Vanilla RNN  
- Bidirectional LSTM (BLSTM)  
- Attention-based RNN  

The goal is to generate phonetically realistic Indian names.

---

## 📂 Repository Structure

```
CSL7640_Assignment2_B22CS063/
├── README.md                               # Project documentation and execution instructions
├── report.pdf         # Comprehensive report detailing methodology and analysis
│
├── Problem_1/                              # Word2Vec Implementation
│   ├── Problem1_WordEmbeddings.ipynb       # Colab Notebook: Web scraping, preprocessing, and training
│   ├── cleaned_corpus.txt                  # The final preprocessed token dataset
│   └── visualizations/                     # Saved Wordcloud and t-SNE projection plots
│       ├── wordcloud.jpeg
│       ├── tsne_cbow.jpeg
│       └── tsne_sgns.jpeg
│
└── Problem_2/                              # RNN Name Generation
    ├── Problem2_NameGeneration.ipynb       # Colab Notebook: RNN models, training, and evaluation
    ├── TrainingNames.txt                   # Dataset of 1000 Indian names used for training
    └── results/                            # Generated samples from the trained architectures
        ├── Vanilla_RNN_samples.txt
        ├── BLSTM_samples.txt
        └── Attention_RNN_samples.txt
```

---

## ▶️ How to Run the Code

The source code is provided as `.ipynb` notebooks designed specifically for execution in **Google Colab**.

All necessary library installations and environment setups are handled within the first cells of each notebook.  
No local Python environment setup is required.

---

# 🚀 Executing Problem 1 (Word Embeddings)

1. Open `Problem1_WordEmbeddings.ipynb` in **Google Colab**.
2. Ensure the Colab runtime is connected.
   - **Recommended:** GPU (T4) for faster training.
   - CPU execution is also supported.
3. Run the cells sequentially from top to bottom.

### What Happens Automatically:

- Initial cells scrape text from the IITJ domain.
- The corpus is cleaned and stored as `cleaned_corpus.txt`.
- CBOW and SGNS architectures are defined using PyTorch.
- Models are trained from scratch.
- The notebook outputs:
  - Nearest Neighbor tables
  - Analogy tests
  - t-SNE visualizations

All outputs are displayed directly below their respective code cells.

---

# 🚀 Executing Problem 2 (Character-Level RNNs)

1. Open `Problem2_NameGeneration.ipynb` in **Google Colab**.
2. **Important:** Upload `TrainingNames.txt` to the root directory of the Colab session (`/content/`).
3. Run the cells sequentially from top to bottom.

### Implementation Details:

- Character vocabulary construction
- Packed sequence training using `pack_padded_sequence`
- Training from scratch:
  - Vanilla RNN
  - BLSTM
  - Attention RNN

### Evaluation:

The notebook automatically computes:
- **Novelty Rate**
- **Diversity Metric**

Results are displayed in a formatted comparison table.

### Output Generation:

The final cell:
- Generates 1,000 sampled names for each architecture.
- Automatically triggers browser downloads of the sample files.

(These generated sample files are also pre-saved inside `Problem_2/results/` in this repository.)

---

## 📊 Report

The complete methodology, experimental setup, training details, hyperparameters, analysis, and comparisons are documented in:

```
report.pdf
```



## 📌 Notes

- All models are implemented **from scratch**.
- No pretrained embeddings or external NLP frameworks were used.
- Designed specifically to satisfy the academic requirements of CSL 7640.

---

**Author:**  
Viswanadhapalli Sujay  
B22CS063  
CSL 7640 - Natural Language Understanding  
IIT Jodhpur
