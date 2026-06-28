### NBA Player Longevity Prediction: Feature Engineering

An end-to-end data processing and feature engineering pipeline designed to prepare historical NBA player statistics for machine learning models predicting 5-year career longevity.

### 📌 Project Overview

Predicting whether a rookie player will last 5 years in the NBA is crucial for franchise investments and draft strategies. This project takes raw, noisy player performance datasets and transforms them through specialized feature engineering, statistical filtering, and data cleaning techniques to build a highly optimized, model-ready training matrix.

### 🛠️ Key Features & Tasks

*   **Target Definiton:** Isolate and balance the dependent variable (`target_5yrs`).
*   **Leakage Prevention:** Automate the removal of non-predictive features, player names, and database hashes to ensure models generalize accurately.
*   **Multicorrelation Filtering:** Construct a statistical correlation matrix to flag and drop overlapping variables.
*   **Advanced Advanced Analytics:** Engineer new domain-specific metrics like Points Per Minute (PPM) and holistic performance efficiency coefficients.
*   **Robust Imputation:** Handle missing data using structural column medians to protect models against systemic gaps without introducing outlier bias.

### 📁 Repository Structure

text

    ├── data/
    │   ├── nba_players.csv               # Raw input dataset
    │   └── nba_players_engineered.csv    # Final processed output
    ├── notebooks/
    │   └── feature_engineering.ipynb      # Main development notebook
    ├── README.md                         # Project documentation
    └── requirements.txt                  # Python dependency stack
    

Use code with caution.

### ⚙️ Requirements & Dependencies

Make sure you have Python 3.8+ installed. You can install all structural dependencies using the provided package list:

bash

    pip install -r requirements.txt
    

Use code with caution.

### Core Libraries Used:

*   **Pandas:** Data manipulation, column restructuring, and file parsing.
*   **NumPy:** Fast mathematical execution and vector alignment.
*   **Seaborn & Matplotlib:** Heatmap plotting and feature variance visualizations.
*   **Scikit-Learn:** (Optional) Scalers, splits, and downstream predictive classifiers.

### 🚀 Getting Started

1.  **Clone the repository:**
    
    bash
    
        git clone https://github.com
        cd nba-longevity-prediction
        
    
    Use code with caution.
    
2.  **Run the Notebook:**  
    Launch Jupyter or VS Code, open `notebooks/feature_engineering.ipynb`, and run the cells sequentially to build the cleaned matrix.

### 📊 Feature Engineering Rationale

*   **Points Per Minute (PPM):** Raw points can distort evaluation if a player gets highly varying court time. Normalizing points by total minutes (`PTS / MIN`) exposes pure scoring velocity.
*   **Composite Efficiency:** Basketball is a game of positive impacts and errors. This metric constructs a rapid health score by combining positive metrics (Points + Rebounds + Assists) and subtracting turnovers (`TOV`).

* * *

*Developed as part of the Advanced Data Science and Predictive Sports Analytics framework.*
