# Single-Base Substitution Signature Extraction in Cancer Genomes

## Introduction

This project investigates genetic mutations, particularly Single-Base Substitutions (SBS), in human cancer genomes. It explores how SBS signatures are extracted using Non-negative Matrix Factorization (NMF) and how cosine similarity impacts the results of this extraction framework. Two primary research questions are addressed:

1. **RQ1**: How does the cosine similarity of SBS signatures in human cancer genome samples relate to the outcomes produced by the existing SBS signature extraction framework?
2. **RQ2**: Can a linear combination model (LCM) enhance the certainty of the results obtained from the current SBS signature extraction framework?

The project builds on the framework proposed by **Alexandrov et al. (2013)** for SBS signature extraction, utilizing dimensionality reduction, Monte Carlo bootstrap resampling, and K-means clustering.

## Processes and Steps

The SBS extraction process involves the following key steps:

1. **Dimensionality Reduction**: Filtering out mutation types that account for less than 1% of total mutations.
2. **Monte Carlo Bootstrap Resampling**: Increasing accuracy and reproducibility through resampling.
3. **Non-negative Matrix Factorization (NMF)**: Decomposing mutation data into SBS signatures and exposures.
4. **K-means Clustering**: Grouping similar SBS signatures based on cosine similarity.
5. **Evaluation**: Using silhouette width, Frobenius reconstruction error, and cosine similarity as evaluation metrics.

## **Data**
The project uses two primary datasets:
1. **Known SBS Signatures**: From the **COSMIC database**, containing 79 known SBS signatures with mutational probabilities across 96 contexts.
2. **Synthetic Human Genome Data**: Five synthetic genome datasets were generated, each containing different combinations of SBS signatures at various levels of cosine similarity, with random noise added to simulate real-world conditions.

### **Samples**:
- **Sample 1**: SBS 6, SBS 12, and SBS 38 (Cosine similarity = 0.051)
- **Sample 2**: SBS 25, SBS 10c, and SBS 6 (Cosine similarity = 0.279)
- **Sample 3**: SBS 30, SBS 44, and SBS 42 (Cosine similarity = 0.526)
- **Sample 4**: SBS 4, SBS 8, and SBS 29 (Cosine similarity = 0.763)
- **Sample 5**: SBS 56, SBS 10d, and SBS 36 (Cosine similarity = 0.914)

## Linear Combination Model (LCM)

The Linear Combination Model (LCM) is proposed to enhance the current framework by increasing the certainty of signature identification. Unlike NMF, which decomposes matrices, LCM focuses on solving the coefficient matrix for known SBS signatures, using supervised machine learning techniques.

## Technologies Used
- Python
- NumPy
- SciPy
- Scikit-learn
- MatplotLib
- Pandas

## Full Report

For a more in-depth explanation of the methodology, results, and conclusions, please refer to the full research report, available in the repository as `Research_Report.pdf`.
