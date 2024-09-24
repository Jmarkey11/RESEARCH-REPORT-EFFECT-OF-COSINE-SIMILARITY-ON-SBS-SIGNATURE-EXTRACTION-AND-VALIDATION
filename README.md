# **The Effect of Cosine Similarity on SBS Signature Extraction and Validation via the Linear Combination Model**

## **Project Overview**
This project investigates genetic mutations, particularly Single-Base Substitutions (SBS), in human cancer genomes. It explores how SBS signatures are extracted using Non-negative Matrix Factorization (NMF) and how the cosine similarity between SBS signatures impacts the results of this extraction framework. Two primary research questions are addressed:

1. **RQ1**: How does the cosine similarity of SBS signatures in human cancer genome samples relate to the outcomes produced by the existing SBS signature extraction framework?
2. **RQ2**: Can a linear combination model (LCM) enhance the certainty of the results obtained from the current SBS signature extraction framework?

## **Key Methods Utilised**
1. **Dimensionality Reduction**: To eliminate less significant mutational types that contribute minimally to the overall dataset, improving analysis efficiency.
2. **Monte Carlo Bootstrap Resampling**: To create multiple resampled datasets for robustness in statistical analysis, allowing for better estimation of variability and uncertainty.
3. **Non-Negative Matrix Factorization (NMF)**: To extract meaningful patterns (SBS signatures) from the data by decomposing the dataset into non-negative components.
4. **Cosine Similarity Clustering**: To group similar signatures based on cosine similarity, facilitating the identification of clusters within the data.
6. **Regression Analysis**: To analyze the relationship between cosine similarity and evaluation metrics, helping to understand the influence of similarity on clustering performance.
7. **Linear-Combination Method (LCM) Implementation**: A proposed method to enhance the current framework by increasing the certainty of signature identification. Unlike NMF, which decomposes matrices, LCM focuses on solving a coefficient matrix based on known SBS signatures, using supervised machine learning techniques.

## **Dataset Information**
The project uses two primary datasets:
1. **Known SBS Signatures**: From the **COSMIC database**, containing 79 known SBS signatures with mutational probabilities across 96 contexts.
2. **Synthetic Human Genome Data**: Five synthetic genome samples were generated, each containing different combinations of SBS signatures at various levels of cosine similarity, with random noise added to simulate real-world conditions.
- **Sample 1**: SBS 6, SBS 12, and SBS 38 (Cosine similarity = 0.051)
- **Sample 2**: SBS 25, SBS 10c, and SBS 6 (Cosine similarity = 0.279)
- **Sample 3**: SBS 30, SBS 44, and SBS 42 (Cosine similarity = 0.526)
- **Sample 4**: SBS 4, SBS 8, and SBS 29 (Cosine similarity = 0.763)
- **Sample 5**: SBS 56, SBS 10d, and SBS 36 (Cosine similarity = 0.914)

## **Evaluation Methods**
Various evaluation metrics were used in this project including:
1. **Frobenius Reconstruction Error (FRE%)**: To evaluate the accuracy of the reconstruction by measuring the difference between the original and reconstructed matrices.
2. **Silhouette Width**: To assess the quality of clustering by measuring how similar each point is to its own cluster versus other clusters.
3. **Intra-Cluster Distance**: To measure the average cosine distance within clusters, indicating the consistency of the signatures in a cluster.
4. **Inter-Cluster Distance**: To measure the average cosine distance between clusters, reflecting how distinct the clusters are from one another.
5. **Cosine Similarity**: To assess the similarity between the extracted and known SBS signatures, helping to evaluate how closely the results match the expected patterns.
6. **Linear Regression Metrics**: To analyze the relationship between cosine similarity and other evaluation metrics (FRE%, silhouette width, intra- and inter-cluster distances) and quantify how much variance is explained by the cosine similarity.
7. **Linear Combination Model (LCM) Coefficient Values**: To determine the significance of SBS signature contributions in clusters by analyzing the coefficient values derived from the LCM.

The evaluation metrics were analyzed through comparative analysis across samples, using summary statistics such as mean, median, standard deviation, and interquartile ranges. Additionally, linear regression models were used to examine the relationships between cosine similarity and each evaluation metric, helping to identify trends and assess the significance of the findings.

For a full analysis of the results please refer to the **Results** section of the report found in **`Research_Report.pdf`**.

## **Technologies Used**
The following Python libraries are used in this project:
- `NumPy`
- `Pandas`
- `Scikit-learn`
- `SciPy`
- `Statsmodels`
- `Seaborn`


