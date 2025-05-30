# IMDb vs. Rotten Tomatoes – Predicting IMDb Ratings with Machine Learning
## Project Overview
This project investigates whether metadata such as Rotten Tomatoes scores, Metacritic scores, genre, runtime, and awards can be used to predict IMDb scores for movies. Through exploratory data analysis (EDA) and machine learning modelling, we explore the relationships between different rating platforms and build a predictive model using Random Forest Regressor.

---

# Research Question
Can we leverage publicly available metadata to predict a movie's IMDb score?
Understanding this factor can provide valuable insights for movie enthusiasts, critics, and filmmakers while serving as a practical application of the complete data science pipeline.

---

# Machine Learning Approach
Problem Formulation
**Type:** Supervised Regression
**Target Variable:** IMDb Rating (0-10 scale)
**Model:** Random Forest Regressor

## Features Used
- Rotten Tomatoes Rating (RT_Rating)
- Metacritic Score (Metacritic)
- Runtime (in minutes)
- Decade (extracted from release year)
- Oscar Status (Won_Oscar - binary)
- Main Genre (one-hot encoded)

## Model Performance
- **R² Score:** ~0.76
- **RMSE:** ~0.38
- **Optimisation:** GridSearchCV for hyperparameter tuning

---

# Dataset Description
- **Source:** movies-250.json - Publicly available dataset
- **Size:** 250 well-known and critically acclaimed films
- **Key Fields:**
  - Title, Year, Genre, Director
  - Runtime, Awards information
  - Multi-platform ratings (IMDb, Rotten Tomatoes, Metacritic)

---

# Methodology
## 1. Data Preparation & Cleaning
- **Loading:** JSON file converted to pandas DataFrame
- **Rating extraction:** Numerical scores extracted from nested rating structures
- **Data type conversion:** String values converted to appropriate numeric types
- **Runtime cleaning:** Removed " min" suffix and converted to numeric

## 2. Feature Engineering
- **Decade:** Derived from release year (1990s, 2000s, etc.)
- **Won_Oscar:** Binary feature extracted from Awards string
- **MainGenre_Label:** Primary genre extracted for visualisation
- **MainGenre_ForModel:** One-hot encoded genre features for ML model

## 3. Exploratory Data Analysis
- **Univariate Analysis:** Distribution histograms for IMDb and RT ratings
- **Bivariate Analysis:**
   - Scatter plots for rating relationships
   - Pearson correlation coefficient: -0.01 between IMDb and RT
   - Categorical Analysis: Box plots of IMDb ratings by genre and decade
   - Trend Analysis: Average ratings across different time periods

## 4. Machine Learning Pipeline
- **Data Splitting:** 80% training, 20% testing
- **Model Selection:** Random Forest Regressor (chosen for robustness and interpretability)
- **Hyperparameter Tuning:** GridSearchCV optimisation
- **Evaluation Metrics:** RMSE and R² Score
- **Feature Importance Analysis:** Identification of the most influential predictors

---

# Key Results
## Exploratory Findings
- **Correlation:** Correlation between IMDb and Rotten Tomatoes scores
- **Genre Insights:** Drama and Crime genres tend to receive higher IMDb ratings
- **Temporal Trends:** Rating patterns show consistency across decades with slight variations

## Machine Learning Results
- **Predictive Performance:** Model explains ~76% of variance in IMDb scores
- **Feature Importance Ranking:**
   - Rotten Tomatoes Score
   - Metacritic Score
   - Genre (particularly Drama)
   - Runtime
   - Oscar Winner Status

## Model Interpretation
- Critic scores from other platforms are strong predictors of IMDb ratings
- Genre significantly impacts rating predictions
- Award recognition (Oscar wins) contributes to higher predicted ratings
- Runtime shows a moderate influence on rating patterns

---

# Key Insights
- **Platform Consistency:** While IMDb and Rotten Tomatoes often align, they capture different aspects of movie reception
- **Critical vs. Popular Appeal:** The strong correlation suggests overlapping but distinct audience preferences
- **Genre Influence:** Certain genres consistently perform better across rating platforms
- **Metadata Predictive Power:** Publicly available information can effectively predict movie ratings

---

# Limitations
- **Dataset Size:** Limited to 250 movies, affecting model generalisation
- **Genre Complexity:** A simplified primary genre approach may lose nuanced categorisation
- **Rating Subjectivity:** IMDb ratings are subject to user bias and review manipulation
- **Feature Scope:** Missing potentially influential factors:
  - Budget and box office data
  - Cast/crew popularity metrics
  - Marketing campaign effectiveness
  - Detailed user sentiment analysis

---

# Future Improvements
## Dataset Enhancement
- Expand to larger, more diverse movie collection
- Include international and independent films
- Add temporal data (release month/season effects)

## Feature Engineering
- **Financial Data:** Budget, box office earnings, ROI
- **Cast/Crew Metrics:** Star power indices, director track record
- **Content Analysis:** NLP on plot summaries and user reviews
- **Marketing Data:** Trailer views, social media engagement

## Advanced Modeling
- **Algorithm Exploration:** Gradient Boosting, Support Vector Regression
- **Deep Learning:** Neural networks for complex pattern recognition
- **Classification Approach:** High/low rating prediction tasks
- **Ensemble Methods:** Combining multiple model predictions

---

# Technologies Used
- **Core Technologies**
  - Python - Primary programming language
  - Jupyter Notebook - Development environment
- **Libraries & Frameworks**
  - Data Manipulation: Pandas, NumPy
  - Visualisation: Matplotlib, Seaborn
  - Machine Learning: Scikit-learn
  -  Random Forest Regressor
  -  GridSearchCV for hyperparameter tuning
  -  Train/test splitting and evaluation metrics

---

# Conclusion
This project successfully demonstrates the application of machine learning to predict IMDb movie ratings using publicly available metadata. The Random Forest model achieved strong predictive performance , confirming that critic scores, genre, and other film characteristics are significant predictors of audience ratings.
The analysis reveals meaningful relationships between different rating platforms and highlights the importance of proper feature engineering in movie rating prediction. While the current model shows promising results, the identified limitations provide clear directions for future enhancements.
This work contributes to understanding the complex dynamics of movie ratings and demonstrates the practical value of data science techniques in the entertainment industry.
