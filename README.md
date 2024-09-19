# Mall Customers Clustering

This project utilizes clustering techniques to segment customers of a mall based on their purchasing behavior and demographic information. By identifying different customer groups, the mall management can develop targeted marketing strategies to enhance customer satisfaction and profitability.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Data Preprocessing](#data-preprocessing)
4. [Clustering Techniques](#clustering-techniques)
5. [Evaluation](#evaluation)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Results](#results)
9. [Contributors](#contributors)
10. [License](#license)
11. [Let's Connect](#lets-connect)

## Project Overview

Customer segmentation is a crucial aspect of marketing strategy for any retail business. This project aims to cluster mall customers based on their attributes using unsupervised learning techniques. The resulting customer segments can help mall management to:
- Develop targeted marketing strategies.
- Optimize store layout and product placement.
- Improve customer experience by offering personalized services.

### Objectives:
1. Understand the distribution of customers based on different features.
2. Apply clustering algorithms to group similar customers.
3. Visualize the resulting clusters for better interpretability.

## Dataset

The dataset used for this project is the [Mall Customers Dataset](https://www.kaggle.com/datasets/hosammhmdali/mall-customers-dataset) available on Kaggle. It contains information on 200 customers of a mall, including their age, annual income, and spending score.

- **Features**:
  - `CustomerID`: Unique identifier for each customer.
  - `Gender`: Male or Female.
  - `Age`: Age of the customer.
  - `Annual Income (k$)`: Annual income of the customer in thousands of dollars.
  - `Spending Score (1-100)`: Score assigned by the mall based on customer behavior and spending nature.

## Data Preprocessing

Before applying clustering algorithms, the following preprocessing steps are performed:
1. **Handling Missing Values**: Ensuring there are no missing values in the dataset.
2. **Encoding Categorical Variables**: Converting the `Gender` column into numerical values using label encoding.
3. **Feature Scaling**: Scaling numerical features like `Age`, `Annual Income`, and `Spending Score` using standardization or normalization to ensure uniformity across all features.
4. **Exploratory Data Analysis (EDA)**: Visualizing the distribution of features and understanding relationships between them using pair plots, histograms, and box plots.

## Clustering Techniques

Multiple clustering algorithms are explored to find the best segmentation of the customers:

1. **K-Means Clustering**:
   - The most popular clustering algorithm used to segment customers into `K` clusters based on the Euclidean distance between data points.
   - Optimal `K` value is determined using the Elbow Method and the Silhouette Score.

2. **Hierarchical Clustering**:
   - Creates a tree of clusters by iteratively merging or splitting existing clusters.
   - Visualized using Dendrograms to decide the optimal number of clusters.

3. **DBSCAN**:
   - Density-Based Spatial Clustering of Applications with Noise.
   - Suitable for discovering clusters of arbitrary shape and for handling noise/outliers in the data.

## Evaluation

The quality of the clusters is evaluated using the following metrics:
- **Inertia (Within-Cluster Sum of Squares)**: Measures how tightly the data points are grouped in a cluster.
- **Silhouette Score**: Measures how similar a point is to its own cluster compared to other clusters. A higher score indicates better-defined clusters.
- **Dendrogram Analysis**: For hierarchical clustering, the dendrogram helps determine the optimal number of clusters.

## Installation

To run this project on your local machine, follow the steps below:

1. Clone the repository:
   ```bash
   git clone https://github.com/3m0r9/clustring-Mall_Customers.git
   ```
2. Navigate to the project directory:
   ```bash
   cd clustring-Mall_Customers
   ```
3. Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
4. Install the necessary dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/hosammhmdali/mall-customers-dataset) and place it in the `data/` directory.
2. Preprocess the dataset:
   ```bash
   python preprocess_data.py --input data/Mall_Customers.csv --output data/processed_customers.csv
   ```
3. Apply clustering algorithms:
   ```bash
   python clustering.py --input data/processed_customers.csv --method kmeans
   python clustering.py --input data/processed_customers.csv --method hierarchical
   python clustering.py --input data/processed_customers.csv --method dbscan
   ```
4. Visualize the clusters:
   ```bash
   python visualize_clusters.py --input data/processed_customers.csv --method kmeans
   ```

## Results

### K-Means Clustering:
- **Optimal Clusters**: 5 clusters based on the Elbow Method and Silhouette Score.
- **Cluster Characteristics**: Each cluster represents a unique group of customers based on their age, income, and spending score.

### Hierarchical Clustering:
- **Optimal Clusters**: 4 clusters based on the Dendrogram.
- **Cluster Characteristics**: Provides a hierarchical view of customer segments.

### DBSCAN:
- **Clusters and Noise**: Identifies dense clusters and isolates noisy data points.
- **Best for Outlier Detection**: Effective in identifying customers with unique spending behaviors.

## Contributors

- **Imran Abu Libda** - [3m0r9](https://github.com/3m0r9)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Let's Connect

- **GitHub** - [3m0r9](https://github.com/3m0r9)
- **LinkedIn** - [Imran Abu Libda](https://www.linkedin.com/in/imran-abu-libda/)
- **Email** - [imranabulibda@gmail.com](mailto:imranabulibda@gmail.com)
- **Medium** - [Imran Abu Libda](https://medium.com/@imranabulibda_23845)
