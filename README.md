# DSA-project
# IMDb vs. Rotten Tomatoes: A Comparative Analysis

This project aims to compare movie ratings from **IMDb** and **Rotten Tomatoes** to analyse how these platforms rate the same films differently. By collecting and cleaning public movie data, we perform exploratory data analysis and a statistical comparison to evaluate how similar or different the two platforms are in scoring the same films. The analysis will be done using **Python**, focusing on data collection, visualisation, and statistical comparison. The results will be visualised through scatter plots and box plots.

---

## Datasets

- **Source**: Publicly available dataset (`movies-250.json`) containing 250 top-rated films.
- **Fields used**:
  - `Title`, `Year`, `Genre`, `Director`
  - `IMDb Rating` (0–10 scale)
  - `Rotten Tomatoes Score` (0–100 scale)

---

## Methodology

### 1. **Data Cleaning**
- Extracted relevant fields from JSON format.
- Converted Rotten Tomatoes ratings from percentage strings (e.g., `"91%"`) to floats.
- Removed movies that were missing either IMDb or RT ratings.

### 2. **Exploratory Data Analysis (EDA)**
- Visualised IMDb and RT score distributions using histograms.
- Created scatter plots to show relationships between the two rating systems.
- Calculated the correlation coefficient between IMDb and RT scores.

### 3. **Statistical Testing**
- A paired t-test was applied to test whether the average IMDb and RT ratings are statistically different.
- RT scores were scaled down to match IMDb’s 0–10 scale.

---

## Key Findings

- **IMDb and RT scores are moderately correlated** (~0.7), indicating a general agreement.
- Several films show a significant rating difference between platforms.
- **T-test results** suggest that the difference between the two platforms' ratings is **(statistically significant / not significant)** (based on p-value).
- Most genres follow similar trends, but a deeper genre-based analysis is planned for the next milestone.

---

## Technologies Used

- **Python**
- `pandas`, `numpy`: Data manipulation
- `matplotlib`, `seaborn`: Visualisation
- `scipy`: Statistical testing

---

## 📁 Project Structure

[DSA-project.pdf](https://github.com/user-attachments/files/19914316/DSA-project.pdf)
