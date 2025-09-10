# Project: Bitcoin Sentiment FearvsGreed
Author: Daksh Jain
Date: September 9, 2025

1. Project Overview
This project analyzes the relationship between cryptocurrency trader behavior and overall market sentiment. The primary objective is to determine which factors are most predictive of daily trading volume.

The analysis begins by exploring a simple hypothesis: does the public Fear & Greed Index correlate with trading activity? It then progresses to a more sophisticated approach, engineering features from raw historical trading data to build a high-performance predictive model. The final conclusion identifies the true drivers of trading volume within the provided dataset.

2. Directory Structure
This project is organized as follows:

ds_Daksh_Jain/
├─ notebook_1.ipynb 
├── notebook_2.ipynb (first attempt)
├── csv_files/ 
│ └── *.csv 
├── outputs/ # Store all visual outputs, graphs, or charts here.
│ └── Scatterchart.png
│ └── FeatureImp.png
├── ds_report.pdf # Final summarized insights and explanations.
└── README.md # (Optional but encouraged) Setup
instructions, notes.
3. Methodology
The analysis in the notebook_1.ipynb notebook follows these key steps:

Data Loading and Cleaning: The two primary datasets (historical_data.csv and fear_greed_index.csv) are loaded, cleaned, and preprocessed.

Exploratory Data Analysis (EDA): Initial visualizations are created to understand the basic relationships between market sentiment and trading behaviors like volume and profitability.

Initial Modeling: A simple model is built using only the Fear & Greed index as a predictor. This step establishes a baseline and highlights the limitations of using sentiment alone.

Feature Engineering: New, more powerful features are engineered from the raw trading data. These features aim to capture the internal market dynamics of each day, such as trade_count, active_traders, and avg_trade_size_usd.

Final Model Training: A Random Forest Regressor is trained using the new, enriched feature set.

Evaluation & Conclusion: The final model's performance is evaluated, and its feature importances are analyzed to draw a definitive conclusion about what truly drives trading volume.

4. Key Findings
The final, high-performance model (RMSE: $1.84M) revealed two critical insights:

Internal Dynamics are Key: The most predictive factors for daily trading volume are the internal market mechanics. The number of trades (trade_count) and the average size of those trades (avg_trade_size_usd) account for over 90% of the model's predictive power.

Sentiment is a Minor Factor: The external Fear & Greed Index was found to be the least important feature, proving that while it provides context, it is not a strong direct predictor of volume.

5. How to Run
Open the notebook_1.ipynb notebook in Google Colab.

Ensure the csv_files/ directory and its contents (historical_data.csv, fear_greed_index.csv) are accessible to the notebook. The simplest way is to upload them to the Colab session's file system.

Execute the notebook cells sequentially from top to bottom.

Dependencies
The analysis relies on the following major Python libraries:

pandas

numpy

scikit-learn

matplotlib

seaborn.
