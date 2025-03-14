# DSA-project
# IMDb vs. Rotten Tomatoes: A Comparative Analysis

This project aims to compare movie ratings from **IMDb** and **Rotten Tomatoes** to analyze how different these platforms rate the same films. The analysis will be done using **Python**, focusing on data collection, visualization, and statistical comparison. The results will be visualized through scatter plots and box plots.

## Datasets

The data will be collected from:
- **IMDb API / Web Scraping**: For movie ratings, genres, directors, and user reviews.
- **Rotten Tomatoes API / Web Scraping**: For critic scores, audience scores, and additional movie metadata.

Data will be gathered using **web scraping** and **APIs**, depending on availability.

## Technological Choices

The project will be developed entirely in **Python**, using the following libraries:

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **Visualization Tools**: Scatter plots, box plots, and histograms will be created to show data distribution.
- **Data Collection Methods**: In cases where API access is insufficient, data extraction methods will be used to retrieve movie scores and related information from web pages.
- **Statistical Analysis Techniques**: Correlation analysis and hypothesis testing will be performed to measure the relationship between the scores of the two platforms.


## Data Collection Plan

- **Collecting Data from the Web**: If direct access is not possible, film scores and details will be compiled from relevant web pages.
- **Obtaining Data from Official Sources**: Data access methods provided by relevant platforms will be used to obtain structured film score data.
- **Using Existing Datasets**: If ready-made datasets that are openly accessible are found, they will be included in the analysis process to provide additional information.

All data collection steps will be documented, ensuring reproducibility.

## Project Plan

1. **Identify Data Sources**: IMDb and Rotten Tomatoes rating data sources will be identified.
2. **Data Collection and Cleaning**: The data will be collected using web scraping and API requests.
3. **Exploratory Data Analysis (EDA)**: Descriptive statistics and visualizations will be used to analyze rating distributions.
4. **Comparison of Ratings**: The following comparisons will be performed:
   - **Scatter Plot**: IMDb vs. Rotten Tomatoes scores for the same movies.
   - **Box Plot**: Distribution of ratings across different genres.
   - **Correlation Analysis**: Finding relationships between ratings from both platforms.
5. **Evaluation of Results**: Insights will be extracted, and a report will be generated.

## Code Requirements

- All code will be written in **Python**.
- The code must be well-documented with comments.
- A `requirements.txt` file will list all necessary dependencies. 

## Dependencies

A `requirements.txt` file will be included with the following dependencies:

