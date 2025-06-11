# Phase-2-Group-1-Project-2025

# 🎬 Movie Data Analysis Project - Group 1

This project explores movie data from **TMDb (The Movie Database)** and **The Numbers**, focusing on analyzing trends in popularity, budgeting, genres, and profitability. The goal is to extract insights from raw datasets by cleaning, transforming, and visualizing the data using Python and various data science tools.

---

## 📁 Datasets Used

We worked with the following CSV files: 

1. **`rt.reviews.tsv`**   
2. **`bom.movie_gross.csv`**  
3. **`tmdb.movies.csv`**  
   - Source: [TMDb](https://www.themoviedb.org/)  
   - Contains metadata about movies, including:
     - Title
     - Genre
     - Popularity
     - Vote average & vote count
     - Runtime
     - Release date

2. **`tn.movie_budgets.csv`**  
   - Source: [The Numbers](https://www.the-numbers.com/)  
   - Contains financial data about movies, including:
     - Production budget
     - Domestic gross
     - Worldwide gross
     - Release date

3. **`project.ipynb`**  
   - A Jupyter Notebook containing the full workflow for data loading, cleaning, analysis, and visualization.

---

## 🧱 Project Structure



---

## 🛠️ Tools and Technologies Used

### 💻 Languages
- **Python** – Used for data manipulation, cleaning, and visualization.
- **Jupiter Notebook** – Used for running python on it.
- **VS code** – Used for running python on it.

### 🧰 Libraries & Frameworks
- **Pandas** – For data loading, transformation, and analysis.
- **NumPy** – For numerical operations.
- **Matplotlib & Seaborn** – For creating visualizations.
- **Python-dotenv** – For managing environment variables securely.

### 📓 Environment
- **Jupyter Notebook** – Used to organize code and analysis in an interactive format.

---

## 🔧 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd movie-data-analysis


# 📊 Movie Data Analysis – Data Loading, Cleaning & Analysis Summary

This document outlines the full data workflow used in our movie data analysis project, including **data loading**, **cleaning**, **merging**, and **visual analysis** to extract key insights from the datasets.

---

## 📥 Data Loading

We used the Python `pandas` library to load the datasets into DataFrames for analysis:

```python
import pandas as pd

tmdb_df = pd.read_csv("data/tmdb.movies.csv")
budgets_df = pd.read_csv("data/tn.movie_budgets.csv")

# 🎬 Movie Data Analysis Project

This project provides an in-depth analysis of movie data using datasets from **TMDb (The Movie Database)** and **The Numbers**. The process includes loading, cleaning, merging, analyzing, and visualizing movie-related data to uncover trends in genres, financial performance, and popularity.

---

## 📂 Data Cleaning

### 🎬 TMDb Movies Dataset
To prepare the TMDb dataset for analysis, we performed the following steps:

- ✅ Converted `release_date` to `datetime` format.
- 🧹 Dropped rows with missing values in important columns such as `popularity` and `vote_average`.
- 📅 Filtered movies to include only those **released after the year 2000**.
- 🔧 Standardized column names and data types for consistency across the project.

---

### 💸 The Numbers Budget Dataset
To clean and standardize financial data:

- 💵 Removed currency symbols (`$`, `,`) from `production_budget`, `domestic_gross`, and `worldwide_gross`.
- 🔢 Converted monetary values into **integers** for numerical computation.
- 📆 Parsed `release_date` into `datetime` format.
- 🏷️ Renamed columns to ensure consistent naming:
  - `production_budget`
  - `domestic_gross`
  - `worldwide_gross`

---

### 🔗 Merging Datasets
To build a unified dataset, we:

- 📤 Extracted `release_year` from `release_date` in both datasets.
- 🔄 Merged both datasets using `movie_title` and `release_year` as keys.
- 🧠 Applied **basic fuzzy matching techniques** to better align slightly mismatched movie titles across datasets.

---

## 📊 Analysis & Visualization

We conducted several analyses to uncover insights using aggregated statistics and visual representations.

---

### 🎭 Genre Popularity
- 🔢 Counted the number of movies produced in each genre.
- ⭐ Calculated **average rating** (`vote_average`) per genre.
- 📈 Explored how genre **popularity trends changed over time**.

---

### 📅 Time-Based Trends
- 📊 Plotted **yearly movie release trends** to detect peaks and changes in production over time.
- 📈 Analyzed how **popularity** and **ratings** evolved across years.

---

### 💰 Budget vs Revenue
To examine financial performance:

- ⚫ Created **scatter plots** to visualize the relationship between `production_budget` and `worldwide_gross`.
- 💡 Computed **Return on Investment (ROI)** using the formula:

  ```python
  ROI = (worldwide_gross - production_budget) / production_budget_
