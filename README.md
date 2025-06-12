
# Phase-2-Group-1-Project-2025

# 🎬 Movie Data Analysis Project - Group 1

##  Overview

This project analyzes historical movie industry data to help guide business decisions for a new movie studio. Using data from multiple sources, we perform exploratory data analysis to answer key business questions about what types of movies succeed at the box office.

---

## Business Problem

The studio seeks to answer the following core questions:

1️⃣ What genres tend to perform best at the box office?  
2️⃣ Do critic ratings predict box office success?  
3️⃣ How do production budgets correlate with box office revenue?  
4️⃣ Does release timing (season, month) impact revenue?

Our goal is to provide data-driven recommendations on genre focus, budget allocation, and release strategy.

---

## 📁 Datasets Used

- **IMDB**: Movie titles, genres, and ratings (SQLite database)
- **Box Office Mojo (BOM)**: Domestic and foreign gross earnings (CSV)
- **The Numbers**: Production budget and worldwide revenue (CSV)
- **Rotten Tomatoes**: Reviews and critic information (TSV)

---

## 🧹  Data Cleaning & Preparation

- Cleaned currency columns, removed special characters and converted to float to prevent overflow errors.
- Converted dates to pandas datetime format.
- Extracted release year and release month for seasonality analysis.
- Standardized titles using lowercase and stripped whitespace to ensure safe merging.
- Filtered out movies with fewer than 50 votes for rating stability.
- Exploded genre fields to analyze individual genres.

---

## 📊 Exploratory Data Analysis Performed

- Genre vs Revenue Analysis
- Ratings vs Revenue Correlation
- Budget vs Revenue Relationship
- Seasonal Release Month Analysis

---
## Tableau
Tableau Visualisation Link
https://public.tableau.com/app/profile/mirriam.david/viz/MovieAnalysisTableau/Dashboard1?publish=yes

## 💡 Key Findings

- **Top Genres**: Adventure, Animation, Fantasy, and Sci-Fi dominate box office revenue globally.
- **Ratings**: Weak correlation to revenue; high ratings do not guarantee high revenue.
- **Budgets**: Strong positive correlation between production budget and revenue.
- **Release Timing**: Summer and holiday releases (May - July, November - December) outperform others.

---

## ✅ Business Recommendations

- Prioritize production in Adventure, Animation, Fantasy, and Sci-Fi.
- Plan release schedules around seasonal high-performing months.
- Use critic ratings as supplemental but not predictive indicators.
- Manage budgets carefully; large budgets bring higher revenue but higher financial risk.

---

##  Repository Files

- `Project_notebook.ipynb` : Full Jupyter Notebook (analysis and visualizations)
- `Phase2_Merged_Cleaned_Data.csv` : Fully cleaned merged dataset
- `Phase2_CleanedData_For_Tableau.xlsx` : Tableau-ready dataset export
- `Phase2_Presentation_Deck_Final.pptx` : Final Presentation Slides
- `README.md` : This README summary

---


