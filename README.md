# 🍔 Zomato Data Exploratory Data Analysis (EDA)

This repository contains a comprehensive Exploratory Data Analysis (EDA) project focused on the Zomato restaurant dataset. The goal of this project is to uncover patterns, insights, and key characteristics of restaurant data, including ratings, location, cost, and online delivery options, using Python's data science libraries.

This project was developed as part of an AI/ML class exercise.

## 📊 Dataset Overview

The analysis is performed on two primary datasets:

1.  `zomato.csv`: The main dataset containing restaurant-specific information (ratings, cost, location, etc.).
2.  `Country-Code.xlsx`: A lookup table used to map `Country Code` to `Country Name`.

## 🛠️ Technologies & Libraries

* **Jupyter Notebook (.ipynb):** The environment used for the analysis.
* **Python 3:** The primary programming language.
* **Pandas:** Used for data loading, cleaning, merging, and manipulation.
* **NumPy:** Used for numerical operations.
* **Matplotlib & Seaborn:** Used for data visualization.

## ✨ Key Analysis & Insights

The notebook covers standard EDA practices and generates several key insights:

### 1. Data Loading and Pre-processing

* Data is loaded from CSV and Excel files.
* The `zomato.csv` and `Country-Code.xlsx` files are merged using the **'Country Code'** column to enrich the dataset with country names.
* Initial data inspection includes viewing the head, checking columns (`df.columns`), and summarizing data types (`final_df.dtypes`).
* Missing values are identified, showing **9 missing values** in the **'Cuisines'** column.

### 2. Geographic Distribution

* **Restaurant Presence by Country:** A pie chart is used to visualize the proportion of restaurants in the top 3 countries.
    * **Insight:** The vast majority of records are for restaurants in **India (94.39%)**, followed by the **United States (4.73%)** and the **United Kingdom (0.87%)**. This indicates a high bias towards Indian data. * **Restaurant Presence by City:** A pie chart shows the top 5 cities by restaurant count, all of which are in India (New Delhi, Gurgaon, Noida, Faridabad, Ghaziabad).

### 3. Rating Analysis

* **Rating Distribution:** A new DataFrame (`ratings`) is created to group and count restaurants by their `Aggregate rating`, `Rating color`, and `Rating text`.
* **Visualizing Rating Counts:** A bar plot visualizes the frequency of different aggregate rating scores (from 0.0 to 4.9).
* **Color Distribution:** A count plot shows the count of each `Rating color`.
    * **Insight:** A large number of restaurants have a rating of **0.0 (Not Rated - White color)**, indicating a significant portion of the dataset lacks user ratings.
    * **Insight:** Most rated restaurants fall in the **Average (Orange)** and **Good (Yellow)** categories.

### 4. Online Delivery

* The analysis determines which countries offer **'Has Online delivery'**.
    * **Insight:** Only **India (2423)** and the **UAE (28)** offer online delivery options in this dataset, with India dominating the count.

## 🚀 How to Run the Code

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Sidharth-kesar/EDA_Assignment-]
    ```
2.  **Ensure you have the required files:**
    * `eda-aiml-class.ipynb`
    * `zomato.csv` (inside an `input/new-dataset` directory, or adjust the path in the notebook)
    * `Country-Code.xlsx` (inside an `input/new-dataset` directory, or adjust the path in the notebook)
3.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn openpyxl
    ```
4.  **Open the Jupyter Notebook:**
    ```bash
    jupyter notebook eda-aiml-class.ipynb
    ```
5.  Run all cells in the notebook to reproduce the analysis and visualizations.
