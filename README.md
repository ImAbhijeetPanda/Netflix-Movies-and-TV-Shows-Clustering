# Netflix Movies and TV Shows Clustering

## Overview
This project uses **unsupervised machine learning** to analyze and cluster Netflix movies and TV shows using various data visualization, text preprocessing, and clustering techniques.

## Table of Contents
1. [Dataset Description](#dataset-description)
2. [Steps Involved](#steps-involved)
   - [Data Preprocessing](#data-preprocessing)
   - [Data Visualization](#data-visualization)
   - [Text Preprocessing](#text-preprocessing)
   - [Model Building](#model-building)
3. [Techniques Used](#techniques-used)
4. [Requirements](#requirements)
5. [How to Run](#how-to-run)

---

## Dataset Description
The dataset used contains details about Netflix movies and TV shows, including attributes such as title, director, cast, country, release year, and more.

## Steps Involved

### 1. Data Preprocessing
The following steps were performed to clean and preprocess the data:
```plaintext
├── Loading the Data
│   ├── Read the dataset using pandas.
├── Handling Missing Values
│   ├── Identified missing values using heatmaps and pandas.
│   ├── Dropped or imputed rows/columns with significant missing values.
├── Data Cleaning
│   ├── Removed duplicates.
│   ├── Stripped leading/trailing whitespaces in textual features.
├── Multi-Valued Columns
│   ├── Exploded columns such as 'director', 'cast', and 'listed_in' to separate rows.
├── Feature Engineering
│   ├── Created new columns from existing ones (e.g., splitting 'date_added').
│   ├── Extracted year from 'release_year'.
├── Outlier Detection and Treatment
│   ├── Used boxplots to identify outliers in numerical columns like 'duration'.
│   ├── Filtered or capped extreme values to reduce skewness.
├── Standardizing Numerical Columns
│   ├── Scaled features such as 'release_year' and 'duration' using StandardScaler.
```

### 2. Data Visualization
The following visualizations were created to better understand the data:
```plaintext
├── Heatmap of Missing Values
├── Bar Chart of Movies vs. TV Shows
├── Top 10 Directors by Movie Count
├── Top 10 Countries Producing Content
├── Distribution of Content Ratings (e.g., PG, TV-MA, etc.)
├── Word Cloud for Titles
├── Pie Chart for Top Genres (Exploded 'listed_in')
├── Boxplots for Numerical Features (Outlier Detection)
├── Pair Plots for Correlation between Numerical Features
├── Count Plots for Year-Wise Content Release
```

### 3. Text Preprocessing
The following steps were applied to prepare textual data for modeling:
```plaintext
├── Text Cleaning
│   ├── Removed punctuation, special characters, and extra whitespaces.
├── Tokenization
│   ├── Split text into individual words/tokens.
├── Stopwords Removal
│   ├── Used NLTK's stopword list to filter out common uninformative words.
├── Lemmatization
│   ├── Applied lemmatization to reduce words to their base forms.
├── TF-IDF Vectorization
│   ├── Converted text into numerical form using Term Frequency-Inverse Document Frequency.
├── Handling Multi-Valued Text Columns
│   ├── Exploded and vectorized columns like 'cast' and 'listed_in'.
```

### 4. Model Building
The following steps were performed to build and evaluate clustering models:
```plaintext
├── Dimensionality Reduction
│   ├── Applied Principal Component Analysis (PCA) to reduce feature dimensions.
│   ├── Reduced the TF-IDF vectorized text features for better efficiency.
├── Clustering Algorithms
│   ├── KMeans Clustering
│   │   ├── Implemented KMeans to create clusters.
│   │   ├── Used the Elbow Method to determine the optimal number of clusters (k).
│   ├── Agglomerative Clustering
│   │   ├── Hierarchical clustering to group similar content.
│   ├── DBSCAN Clustering
│   │   ├── Density-based clustering for content grouping.
├── Model Evaluation
│   ├── Calculated Silhouette Scores to measure clustering performance.
├── Saving the Best Model
│   ├── Saved the best-performing model using the Pickle library for reuse.
```

---

## Techniques Used
- **Data Cleaning and Preprocessing**
  - Handling missing values, duplicates, and multi-valued columns.
  - Outlier detection and treatment.
  - Standardization of numerical columns.
- **Data Visualization**
  - Heatmaps, bar charts, pie charts, pair plots, word clouds, and boxplots.
- **Text Preprocessing**
  - Tokenization, stopwords removal, lemmatization, and TF-IDF vectorization.
- **Unsupervised Machine Learning**
  - Dimensionality reduction using PCA.
  - Clustering using KMeans, Agglomerative Clustering, and DBSCAN.
  - Silhouette Scores for model evaluation.

## Requirements
To run this project, you need the following libraries:
- Python >= 3.8
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-learn
- NLTK
- WordCloud
- Pickle

You can install them using:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk wordcloud
```

## How to Run
1. Clone this repository:
   ```bash
   git clone <https://github.com/ImAbhijeetPanda/Netflix-Movies-and-TV-Shows-Clustering>
   ```
2. Install the required libraries.
3. Open the notebook `Netflix_Unsupervised_ML.ipynb` and run the cells sequentially.
4. Visualize the results and check the saved model.

---

## Results
The project successfully clusters Netflix titles into meaningful groups based on features like title, director, cast, and ratings. Dimensionality reduction helped in visualizing and improving clustering performance. Silhouette Scores validated the quality of clustering.

---

## Credits
This project is authored and maintained by **Abhijeet Panda**.



