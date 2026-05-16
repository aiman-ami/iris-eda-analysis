# Iris Dataset Exploratory Data Analysis

**Author:** Aiman Ishaq
**Date:** May 2026
**Tools:** Python, pandas, matplotlib, seaborn
**Dataset:** Iris Dataset (150 rows × 5 columns)

---

## Overview

This project performs exploratory data analysis and visualization on the classic Iris dataset. The goal is to understand the dataset's structure, summarize its key statistics, and uncover patterns across the three flower species using visual tools.

---

## Dataset

The Iris dataset contains measurements for 150 flower samples across three species: Setosa, Versicolor, and Virginica. Each sample has four numeric features: sepal length, sepal width, petal length, and petal width (all in cm). The dataset is perfectly balanced with 50 samples per species and contains no missing values.

It is loaded directly via seaborn — no manual download required.

---

## Project Structure

```
iris-eda-analysis/
│
├── iris_exploring_and_visualizing_dataset.ipynb
└── plots/
    ├── scatter_plot.png
    ├── histogram.png
    ├── boxplot.png
    └── heatmap.png
```

---

## Analysis Steps

**1. Load Dataset**
Loaded using `sns.load_dataset('iris')` with all imports and folder setup at the top.

**2. Explore Structure**
Examined shape, column names, data types, statistical summary, missing values, and species count using `.shape`, `.columns`, `.head()`, `.info()`, `.describe()`, `.isnull().sum()`, and `.value_counts()`.

**3. Scatter Plot**
Plotted sepal length vs petal length, color-coded by species, to analyze relationships between variables.

**4. Histogram**
Created a 2×2 grid of histograms with KDE curves to examine the distribution of each numeric feature across species.

**5. Box Plot**
Generated side-by-side box plots for each feature to detect outliers and visualize the spread and IQR per species.

**6. Correlation Heatmap**
Plotted a heatmap of feature correlations to quantify linear relationships between numeric variables.

---

## Key Findings

The dataset contains 150 rows and 5 columns with no missing values. Each of the three species has exactly 50 samples, making it a perfectly balanced dataset.

Setosa is the most distinct species with the smallest average petal length of approximately 1.46 cm and separates cleanly from the other two species in all petal-based plots. Virginica has the largest average petal length at approximately 5.55 cm and petal width at approximately 2.03 cm.

Petal length and petal width are the most useful features for distinguishing between species, showing clear separation in the scatter plot, histograms, and box plots. Sepal width shows the most overlap across species and contains a few outliers visible in the box plot.

The correlation heatmap confirms a strong positive correlation of 0.87 between sepal length and petal length across all species.

---

## Skills Demonstrated

Data loading and inspection using pandas, basic data summarization, and visualization using matplotlib and seaborn.
