# NBA-Game-Prediction-Engine

This `README.md` is designed to showcase your technical rigor to recruiters by highlighting the specific data engineering and machine learning workflows you implemented.

---

# NBA Game Prediction Engine

An end-to-end data science project that leverages 17 years of historical NBA data to predict game outcomes. This project covers the entire pipeline from raw data ingestion and relational database management to feature engineering and machine learning model deployment.

## Project Overview

This engine analyzes over **23,000 game records** (2008–2025) to identify winning patterns. By processing complex variables like betting odds, team performance metrics, and historical matchups, the system provides a probabilistic prediction of which team will win a given game.

## Tech Stack

* **Language:** Python
* **Data Engineering:** Pandas, NumPy
* **Database:** SQLite (Relational Modeling)
* **Machine Learning:** Scikit-Learn (Random Forest Classifier)
* **Visualization:** Matplotlib, Seaborn

## Key Features & Results

* **Relational Data Modeling:** Architected a normalized **SQLite** database to efficiently store and query 17 years of team and player statistics.
* **Automated ETL Pipeline:** Built a robust pipeline to clean raw CSV data, handle missing values in betting odds, and execute bulk SQL loading.
* **Feature Engineering:** Developed custom features including rolling win percentages and head-to-head performance metrics.
* **Predictive Performance:** Achieved a **66.17% accuracy** rate on unseen test data using a tuned **Random Forest** model.
* **Model Validation:** Utilized train/test splitting and confusion matrices to verify model reliability across different NBA eras.

## Project Structure

```text
├── data/                   # Raw CSV files (games, players, teams)
├── nba_project.db          # SQLite Database containing cleaned records
├── notebooks/              # Jupyter Notebooks for EDA and Model Training
├── src/                    # Python scripts for ETL and Inference
└── README.md

```

## How It Works

1. **Data Ingestion:** Raw datasets are processed through a Python-based ETL script.
2. **Database Storage:** Data is stored in a structured SQL environment to ensure referential integrity.
3. **Preprocessing:** Data is normalized and scaled; categorical variables are encoded for the ML model.
4. **Training:** A Random Forest algorithm is trained on historical data, prioritizing features like effective field goal percentage and home-court advantage.
5. **Inference:** The model accepts two team IDs and returns the predicted winner with a confidence score.

---

### Future Improvements

* Implement real-time data scraping using BeautifulSoup to include 2026 season stats.
* Deploy a web-based dashboard using **Streamlit** for interactive predictions.
* Experiment with Gradient Boosting (XGBoost) to push accuracy beyond 70%.
