# Netflix Movies and TV Shows Clustering

## Overview
This project uses **unsupervised machine learning techniques** to analyze and cluster Netflix content, such as movies and TV shows, based on key attributes like genres, countries, and duration. The notebook includes comprehensive steps, from data preprocessing to clustering, visualization, and dimensionality reduction.

## Steps Included

### 1. **Importing Libraries**
Essential Python libraries are imported for data manipulation, visualization, and machine learning:
- `pandas`, `numpy` - Data handling
- `matplotlib`, `seaborn` - Visualization
- `sklearn` - Machine Learning algorithms

### 2. **Loading the Dataset**
The Netflix dataset is loaded and explored. Key columns include:
- `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, and `description`.

### 3. **Data Preprocessing**
- Handling missing values in the dataset.
- Combining and transforming columns like `listed_in` (genres).
- Cleaning up and standardizing data fields for further analysis.

### 4. **Exploratory Data Analysis (EDA)**
Performed to understand the data distribution:
- Distribution of movies vs TV shows.
- Top genres, countries, and directors.
- Visualization of content release trends over time.

### 5. **Text Vectorization**
- **TF-IDF** (Term Frequency-Inverse Document Frequency) is applied to the `listed_in` column (genres) for feature extraction.
- The vectorized data serves as input for clustering.

### 6. **Dimensionality Reduction**
- **PCA (Principal Component Analysis)** is used to reduce dimensions and simplify clustering while retaining key information.

### 7. **Clustering Techniques**
Two clustering algorithms are implemented:
1. **KMeans Clustering**
   - The optimal number of clusters is determined using the **Elbow Method**.
   - KMeans is applied to group similar content.
2. **Hierarchical Clustering**
   - A dendrogram is generated to visualize content clusters hierarchically.

### 8. **Visualization of Clusters**
The results of clustering are visualized using scatter plots and other techniques to interpret and understand the grouped content.

### 9. **Results and Insights**
- Insights into content similarities and patterns within Netflix movies and TV shows.
- Analysis of which genres, durations, or countries share the most similarities.

## Key Features
- **Unsupervised Machine Learning**: Clustering with KMeans and Hierarchical methods.
- **Dimensionality Reduction**: Simplifying features with PCA.
- **EDA**: Clear and detailed visualizations to explore the data.
- **Reproducibility**: Each step is well-documented with code and output.

## Prerequisites
Install the following Python libraries before running the notebook:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/ImAbhijeetPanda/Netflix-Movies-and-TV-Shows-Clustering.git
   ```
2. Install required libraries.
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Netflix_Unsupervised_ML.ipynb
   ```
4. Execute the cells in order.

## Results
- Clustered Netflix content based on genres, countries, and other features.
- Visualized results for better understanding and insights.

## Dataset Source
The dataset was originally obtained from Kaggle or similar sources containing Netflix content information.

## Contribution
Feel free to contribute or suggest improvements. Fork the repository and submit a Pull Request!

---

**Author**: [ImAbhijeetPanda](https://github.com/ImAbhijeetPanda)
