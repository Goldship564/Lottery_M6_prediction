# Lottery_M6_prediction
# Mark Six Lottery Analysis and Prediction

## Overview
This project analyzes historical Mark Six lottery data and uses both frequency-based and machine learning methods to predict the next set of winning numbers. Mark Six is a popular lottery game in Hong Kong, where players select 6 numbers from 1 to 49, and 7 numbers are drawn (6 main numbers + 1 extra number). The goal is to explore patterns in the data and generate predictions, though lottery draws are inherently random and predictions are experimental.

### Features
- **Data Analysis**: Frequency of main and extra numbers, distribution of low/high and odd/even numbers.
- **Frequency-Based Prediction**: Predicts numbers based on their historical frequency.
- **Machine Learning Prediction**: Uses K-Means clustering to group draws and predict based on cluster centroids.
- **Visualization**: Bar chart of number frequencies.

### Dataset
The dataset contains 62 draws from May 28, 2024, to March 11, 2025, stored in `mark_six_history.csv`. Key columns include:
- `Draw`: Draw identifier (e.g., 25/027).
- `Date`: Date of the draw (e.g., 2025-03-11).
- `Winning Number 1`, `2`, `3`, `4`, `5`, `6`: The 6 main numbers drawn.
- `Extra Number`: The 7th number drawn (bonus number).
- Additional columns: `From Last`, `Low`, `High`, `Odd`, `Even`, `1-10`, `11-20`, `21-30`, `31-40`, `41-50`, prize-related columns (`Division 1 Winners`, etc.), and `Turnover`.

## Prerequisites
- **Python 3.x**
- **Libraries**:
  - `pandas`: Data manipulation.
  - `numpy`: Numerical operations.
  - `sklearn`: Machine learning (K-Means).
  - `matplotlib`: Visualization.
  - `collections`: Frequency counting.
  - `google.colab`: For Colab-specific file uploads (optional).

Install dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib
git clone https://github.com/yourusername/mark-six-prediction.git
cd mark-six-prediction

Upload your Mark Six CSV file:
[Uploads mark_six_history.csv]
Uploaded file: mark_six_history.csv
Loaded 62 draws from mark_six_history.csv

Top 10 Most Frequent Main Numbers:
Number 1: 11 times
Number 3: 10 times
Number 15: 9 times
...

Draws per Cluster: Counter({0: 15, 2: 14, 1: 12, 4: 11, 3: 10})

Machine Learning Prediction (K-Means Clustering):
Predicted Main Numbers: [4, 11, 19, 25, 34, 42]
Predicted Extra Number: 22

Frequency-Based Prediction (for comparison):
Predicted Main Numbers: [1, 3, 15, 18, 25, 33]
Predicted Extra Number: 23

