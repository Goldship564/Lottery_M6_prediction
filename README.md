# Lottery_M6_prediction

Below is a README file tailored for your Mark Six lottery analysis and prediction project, assuming it’s hosted on a platform like GitHub or run in Google Colab. It includes instructions, an overview, and details about the dataset and code.
Mark Six Lottery Analysis and Prediction
Overview
This project analyzes historical Mark Six lottery data and uses both frequency-based and machine learning methods to predict the next set of winning numbers. Mark Six is a popular lottery game in Hong Kong, where players select 6 numbers from 1 to 49, and 7 numbers are drawn (6 main numbers + 1 extra number). The goal is to explore patterns in the data and generate predictions, though lottery draws are inherently random and predictions are experimental.
Features
Data Analysis: Frequency of main and extra numbers, distribution of low/high and odd/even numbers.
Frequency-Based Prediction: Predicts numbers based on their historical frequency.
Machine Learning Prediction: Uses K-Means clustering to group draws and predict based on cluster centroids.
Visualization: Bar chart of number frequencies.
Dataset
The dataset contains 62 draws from May 28, 2024, to March 11, 2025, extracted from a provided CSV file (mark_six_history.csv). Key columns include:
Draw: Draw identifier (e.g., 25/027).
Date: Date of the draw (e.g., 2025-03-11).
Winning Number 1, 2, 3, 4, 5, 6: The 6 main numbers drawn.
Extra Number: The 7th number drawn (bonus number).
Additional columns: From Last, Low, High, Odd, Even, 1-10, 11-20, 21-30, 31-40, 41-50, prize-related columns (Division 1 Winners, etc.), and Turnover.
Prerequisites
Python 3.x
Libraries:
pandas: Data manipulation.
numpy: Numerical operations.
sklearn: Machine learning (K-Means).
matplotlib: Visualization.
collections: Frequency counting.
google.colab: For Colab-specific file uploads (optional).
Google Colab: Recommended for running the code interactively with file uploads.
Install dependencies:
bash
pip install pandas numpy scikit-learn matplotlib
Installation
Clone or Download:
If hosted on GitHub:
bash
git clone https://github.com/yourusername/mark-six-prediction.git
cd mark-six-prediction
Alternatively, download the code and dataset manually.
Prepare the Dataset:
Save your CSV as mark_six_history.csv with the header:
Draw,Date,Winning Number 1,2,3,4,5,6,Extra Number,...
Ensure the file matches the structure described in "Dataset" above.
Run in Google Colab:
Open Google Colab (https://colab.research.google.com/).
Upload the Python script (e.g., mark_six_predictor.py) and CSV file.
Run the cells as instructed below.
Usage
Running the Code
Upload the Script:
Copy the provided Python code into a Colab notebook cell or save it as mark_six_predictor.py.
Upload the CSV:
When prompted, upload mark_six_history.csv using the Colab file upload widget.
Execute:
Run the script:
python
if __name__ == "__main__":
    main()
The script will:
Load and validate the CSV.
Perform frequency analysis.
Predict numbers using K-Means clustering.
Compare with a frequency-based prediction.
Display a frequency bar chart.
Example Output
Upload your Mark Six CSV file:
[Upload widget appears]
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
A bar chart of main number frequencies will also display.
Code Structure
load_data(csv_file): Loads and preprocesses the CSV into main numbers and extra numbers.
frequency_analysis(main_numbers, extra_numbers): Computes and displays number frequencies.
kmeans_prediction(main_numbers, extra_numbers): Applies K-Means clustering to predict numbers.
main(): Orchestrates the workflow (upload, analysis, prediction, visualization).
Analysis Insights
Frequency: Numbers like 1, 3, 15, 18, 25, and 33 are the most common main numbers in the dataset.
K-Means: Clusters draws into 5 groups, predicting a "typical" combination (e.g., [4, 11, 19, 25, 34, 42]).
Randomness: Lottery draws are independent, so predictions are experimental and not guaranteed.
Limitations
Random Nature: Lottery outcomes are random, limiting the predictive power of ML or frequency methods.
Small Sample: 62 draws (372 main numbers) is a tiny fraction of possible combinations (13.9 million).
Model Simplicity: K-Means assumes patterns that may not exist in truly random data.
Future Improvements
Larger Dataset: Incorporate more historical draws for better analysis.
Advanced Models: Experiment with neural networks or Markov chains (though randomness persists).
Additional Features: Use columns like Odd, Even, or Low/High as features for prediction.
Contributing
Feel free to fork this project, submit pull requests, or suggest improvements via issues. Contributions to enhance analysis or prediction methods are welcome!
License
This project is licensed under the MIT License - see the LICENSE file for details (create one if hosting publicly).
Acknowledgments
Data provided by the user, based on Mark Six draws from 2024–2025.
Built with inspiration from lottery analysis techniques and machine learning experimentation.
Notes
Replace yourusername and repository URL with your actual GitHub details if hosting online.
Add a LICENSE file if you plan to share publicly (e.g., MIT License text).
Adjust paths or instructions if you’re not using Colab (e.g., local Python setup).
Let me know if you’d like to tweak this further!
