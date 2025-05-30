# IMDb vs. Rotten Tomatoes – Predicting IMDb Ratings with Machine Learning

## Project Overview

This project investigates whether metadata such as Rotten Tomatoes scores, genre, runtime, and awards can be used to **predict IMDb scores** for movies. In addition to exploratory data analysis (EDA), we built and optimized a machine learning model using Random Forest Regressor.

The goal is to learn if there's a strong correlation between public/critical perception and IMDb ratings, and whether it's feasible to predict a film’s IMDb score based on such features.

---

##  Objective

> Using Rotten Tomatoes rating, Metacritic score, genre, year, runtime, and award information, we aim to **predict the IMDb rating** of a movie using supervised machine learning.

This is treated as a **regression problem**, with IMDb score (0–10 scale) as the target variable.

---

## Machine Learning Summary

- **Model Type:** Regression (Random Forest Regressor)
- **Target:** `imdbRating`
- **Input Features:**
  - Rotten Tomatoes Rating (`RT_Rating`)
  - Metacritic Score (`Metacritic`)
  - Runtime (in minutes)
  - Decade (extracted from Year)
  - Oscar-Winning Status (`Won_Oscar`)
  - Main Genre (transformed using one-hot encoding)

- **Performance Metrics:**
  - **R² Score:** 
  - **RMSE:** 

- **Tuning:** GridSearchCV used to optimize `n_estimators` and `max_depth`

---

## Exploratory Data Analysis

The following visual analyses were included:

- Histograms for IMDb and RT rating distributions
- Scatter plot for IMDb vs RT score
- Pearson correlation coefficient between scores
- Box plot of IMDb by genre
- Bar chart of average IMDb rating per decade

---

## Feature Engineering & Transformation

To make data suitable for machine learning:

- `Genre` → main genre extracted and one-hot encoded (`MainGenre_ForModel_*`)
- `Awards` → binary column indicating if the movie won an Oscar
- `Year` → converted to decade (`Decade`)
- `Runtime` → converted from text to numeric

Additionally:
- `MainGenre_Label` was kept for use in plots, while encoding was applied to `MainGenre_ForModel`

---

## Dataset

- **File:** `movies-250.json`
- **Source:** Publicly available dataset of 250 well-known films
- **Fields Used:** Title, Year, Genre, Runtime, Ratings (IMDb, RT, Metacritic), Awards

