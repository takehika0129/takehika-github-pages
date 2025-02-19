---
title: "Simple Data Visualization in Python Using a Public Dataset (2025/02/19)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no10-public-data-visualisation)](https://github.com/takehika0129/no10-public-data-visualisation)


# **Concept**
The goal is to provide a streamlined way to explore, clean, and visualize datasets before applying machine learning or statistical modeling. By using a Jupyter Notebook, users can interactively analyze the dataset, detect missing values, evaluate feature correlations, and identify outliers efficiently.


# **Features**
- **🔄 Skewness & Kurtosis Analysis**: Evaluates the distribution of numerical features to detect skewed data.
- **🔥 Correlation heatmaps**: Identifies relationships between numerical features.
- **📈 Visualizations for Better Understanding**: Generates barplots, histograms, boxplots, to identify patterns in the data.


# **Challenges & Solutions**
- **Feature Redundancy**: When features are highly correlated, including both can lead to redundancy in machine learning models. The correlation heatmap helps identify redundant features, allowing users to drop unnecessary columns and improve dataset efficiency.


# **Future Improvements**
- **Interactive Visualizations**: Integrate `plotly` or `dash` to allow dynamic filtering and zooming in visualizations, improving the user experience.
- **Text Data Analysis**: Extend support for text-based datasets, including sentiment analysis, keyword extraction, and named entity recognition (NER). This will allow users to analyze datasets that contain unstructured text data alongside numerical and categorical features. 

  
---
[Back to All Prototypes](../index.md)
