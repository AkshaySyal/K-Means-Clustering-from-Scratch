# K-Means-Clustering-from-Scratch
This project focuses on implementing a custom K-Means clustering algorithm and applying it to the MNIST, Fashion, and 20 Newsgroups datasets, with evaluation based on the K-Means objective function, Purity, and Gini Index

# Problem Statement
![image](https://github.com/user-attachments/assets/ee0c8ff1-5f12-4965-aead-4ddaccfa6623)

# Solution Summary
- Implemented a **custom K-Means clustering algorithm** supporting:
  - **Euclidean distance**
  - **Cosine similarity**

- **Algorithm Details**:
  - Core EM (Expectation-Maximization) steps:
    - `computePi`: Assign data points to nearest centroids.
    - `computeCentroids`: Update cluster centers.
  - Termination conditions:
    - Convergence of K-Means objective (sum of squared distances).
    - Reaching a specified max number of iterations.

- **Datasets Used**:
  - **MNIST** (K=10)
  - **Fashion-MNIST** (K=10)
  - **20 Newsgroups** (K=20, with additional trials at K=40 and lower K)

- **Performance Evaluation**:
  - Internal metric: K-Means objective function.
  - External metrics:
    - **Purity**
    - **Gini Index**
  - Derived from confusion matrices comparing cluster assignments vs. true labels.

- **Key Insights**:
  - Changing K affected the K-Means objective trends.
  - On 20 Newsgroups, setting K=40 caused a **RuntimeWarning** and `nan` objective due to empty clusters.
  - Extensive **text preprocessing** was required for 20 Newsgroups, yielding a sparse numerical matrix (99.82% zeros).

- **Conclusion**:
  - Custom K-Means successfully clustered varied datasets.
  - External metrics provided a more holistic view of clustering performance beyond internal objectives.
