# IMDb Movie Ratings Analysis

## Project Overview
Analysis of factors influencing IMDb movie ratings using fundamental data science techniques.
Objective: Identify which movie attributes (genre, budget, runtime, cast popularity) most impact audience ratings.

## Dataset
- **Source:** IMDb Movie Dataset
- **Records:** 5,000+ movies
- **Features:** Genre, Budget, Runtime, Release Year, Director, Cast Popularity, Vote Count, IMDb Rating

## Methodology
1. **Data Preprocessing:** Data cleaning, handling missing values (15% threshold), feature normalization
2. **Exploratory Data Analysis (EDA):** Correlation analysis, trend identification, statistical testing
3. **Regression Modeling:** Linear Regression, Multiple Regression with R² evaluation
4. **Feature Importance:** Statistical significance testing to rank predictor variables

## Key Findings
- **Audience engagement metrics** (vote count, review volume) are **3x stronger predictors** of ratings than financial attributes
- **Correlation Analysis:** Audience metrics show 0.68+ correlation with ratings vs. budget (0.18 correlation)
- **Model Performance:** Achieved R² = 0.68 with multi-factor regression model

## Technologies Used
- **Language:** R
- **Libraries:** ggplot2, dplyr, stats
- **Methods:** Regression Analysis, Correlation Analysis, Statistical Testing

## Project Structure
```
imdb-movie-ratings-analysis/
├── README.md
├── data/
│   └── imdb_movies.csv
├── analysis/
│   └── movie_ratings_analysis.R
└── visualizations/
    ├── correlation_heatmap.png
    └── rating_distribution.png
```

## How to Run
1. Install R and required libraries: `install.packages(c("ggplot2", "dplyr"))`
2. Load dataset: `imdb_data <- read.csv("data/imdb_movies.csv")`
3. Run analysis: `source("analysis/movie_ratings_analysis.R")`

## Results
- Identified audience engagement as primary rating driver
- Regression model explains 68% of rating variance
- Insights inform movie success prediction strategies

## Author
Yash Yadav | B.Tech CSE 2nd Year | UPES Dehradun
