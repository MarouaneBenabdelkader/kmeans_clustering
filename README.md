# Kmeans course
## Clustering: A Concise Definition

Clustering is a data analysis technique used to group sets of objects in such a way that objects within the same cluster exhibit 
higher similarity to each other than to those in other clusters. This approach is foundational in unsupervised learning, where it
seeks to categorize data into classes or groups based on inherent patterns, without the need for predefined labels. 

Key Characteristics:
- **Objective**: Identifies inherent groupings in data by discovering patterns of similarity.
- **Labeling**: In contrast to supervised learning, clustering attempts to label data into classes or groups without pre-existing labels.
- **Quantitative Focus**: Particularly effective in analyzing quantitative datasets, where numerical features play a crucial role.
- **Applications**: Extensively used across various fields such as market research, pattern recognition, and image processing.

Clustering helps to uncover the natural structure of the data, providing insights into its characteristics and enabling the identification of patterns or outliers.


## Partitioning and Hierarchical Clustering

These are two primary approaches to clustering, each with its unique methodology and applications.

### Partitioning Clustering

1. **Overview**: 
   - Partitioning clustering divides the dataset into a set of clusters by assigning each data point to exactly one cluster.
   - Commonly exemplified by the K-means algorithm.

2. **Characteristics**: 
   - **Direct Assignment**: Each point is associated with the nearest centroid.
   - **Optimization Goal**: Minimize the variance within each cluster.
   - **Scalability**: Generally efficient for large datasets.

3. **Applications**: 
   - Ideal for market segmentation, document classification, and as a preliminary step in complex hierarchical clustering processes.

### Hierarchical Clustering

1. **Overview**: 
   - Builds a hierarchy of clusters, either aggregating individual elements into clusters (Agglomerative) or splitting a large cluster into smaller ones (Divisive).

2. **Characteristics**: 
   - **Agglomerative**: Starts with each element as a separate cluster and merges them based on similarity.
   - **Divisive**: Starts with a single cluster containing all elements and divides it iteratively.
   - **Dendrogram Representation**: The hierarchy is often represented as a tree structure, or dendrogram.

3. **Applications**: 
   - Particularly useful in biological sciences for species classification, in social network analysis, and any domain where the hierarchical relationship between clusters is valuable.

Both partitioning and hierarchical clustering have their distinct advantages and are chosen based on the nature of the dataset and the specific goals of the clustering process.

## Similarity and Dissimilarity in Clustering

### Similarity
- **Definition**: A measure that reflects how much alike two data objects are.
- **Usage in Clustering**: High similarity within a cluster.
- **Common Measures**: Cosine similarity (for text data), Pearson correlation, Jaccard similarity.
- **Importance**: Determines how closely data points in a cluster are related to each other.

### Dissimilarity
- **Definition**: A measure of how different two data objects are.
- **Usage in Clustering**: Low dissimilarity within a cluster, higher between clusters.
- **Common Measures**: Euclidean distance (most common in K-means), Manhattan distance.
- **Importance**: Helps in differentiating between clusters, crucial for cluster separation.

Understanding both similarity and dissimilarity is essential in defining appropriate clustering algorithms and for interpreting the results of a clustering process.
## Measures of Distance Between Two Clusters with Formulae

Quantifying the distance between clusters is key in clustering. Below are common measures with their respective formulae:

### 1. Single Linkage (Nearest Neighbor)
- **Formula**: \( \min_{x \in A, y \in B} d(x, y) \)
- **Description**: Minimum distance from any member of one cluster to any member of the other.
- **Characteristic**: May result in "chain-like" clusters.

### 2. Complete Linkage (Farthest Neighbor)
- **Formula**: \( \max_{x \in A, y \in B} d(x, y) \)
- **Description**: Maximum distance from any member of one cluster to any member of the other.
- **Characteristic**: Forms more compact clusters.

### 3. Average Linkage
- **Formula**: \( \frac{1}{|A||B|} \sum_{x \in A, y \in B} d(x, y) \)
- **Description**: Average of all distances between all pairs in two clusters.
- **Characteristic**: A balance between single and complete linkage.

### 4. Centroid Distance
- **Formula**: \( d(\text{centroid}_A, \text{centroid}_B) \)
- **Description**: Distance between the centroids of the two clusters.
- **Characteristic**: Flexible with distance measures.

### 5. Ward's Method
- **Formula**: Minimize increase in total within-cluster variance.
- **Description**: Merge clusters that minimally increase total variance.
- **Characteristic**: Creates clusters of similar sizes.

Note: \( d(x, y) \) represents the distance between elements \( x \) and \( y \), \( |A| \) and \( |B| \) are the sizes of clusters A and B, respectively.

The choice of measure can significantly influence the structure of the resulting clusters, and should align with the nature of the data and the clustering objectives.

