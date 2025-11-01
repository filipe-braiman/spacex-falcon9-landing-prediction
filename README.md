# SpaceX Falcon 9 First Stage Landing Prediction

**IBM Data Science Professional Certificate Capstone Project**

## Project Overview

This project is an enhanced adaptation of my IBM Data Science Capstone project, delivering an end-to-end data science solution to predict the landing success of the SpaceX Falcon 9 rocket's first stage. The original capstone project was completed as part of my [IBM Data Science Professional Certificate on Coursera](https://coursera.org/share/839efad34c9080742b9d556d8c7d608b).

The Falcon 9 is a revolutionary vehicle in the aerospace industry due to its reusable first stage, which dramatically reduces launch costs. The ability to accurately predict landing success is critical for cost estimation, operational planning, and competitive analysis in the commercial launch market.

This project demonstrates a complete workflow from data acquisition to predictive modeling, providing actionable insights into the factors driving launch success.

## Project Objectives

The primary goals of this project were to:

*   Identify the key factors—such as payload mass, booster version, orbit type, and launch site—that influence Falcon 9 first-stage landing success.
*   Quantify performance differences between launch sites and booster versions.
*   Explore how payload ranges and mission profiles affect landing outcomes.
*   Build and evaluate a predictive model capable of accurately forecasting landing success to support decision-making.

## Methodology and Workflow

The project followed a comprehensive data science pipeline:

1.  **Data Collection:** Combined data from the SpaceX REST API and web-scraped Wikipedia to build comprehensive datasets of Falcon 9 launches.
2.  **Data Wrangling:** Cleaned, standardized, and engineered key features, including payload mass, booster version, orbit type, and the target landing outcome variable.
3.  **Exploratory Data Analysis (EDA):**
    *   Performed structured data analysis using SQL.
    *   Conducted statistical visual analysis with Python libraries.
    *   Mapped launch sites and outcomes geographically using Folium.
4.  **Interactive Visualization:** Built an interactive Plotly Dash dashboard for dynamic exploration of launch data and success rates.
5.  **Predictive Modeling:** Trained, tuned, and evaluated multiple classification models, including Logistic Regression, Support Vector Machine (SVM), Decision Tree, and K-Nearest Neighbors (KNN), using GridSearchCV for hyperparameter optimization.

## Key Results and Findings

### Model Performance Comparison

After training and evaluation, the performance of the classification models was compared based on accuracy.

| Model | Training Accuracy | Test Accuracy |
| :--- | :---: | :---: |
| Decision Tree | 88.9% | 94.4% |
| Support Vector Machine (SVM) | 86.2% | 83.6% |
| Logistic Regression | 83.4% | 83.3% |
| K-Nearest Neighbors (KNN) | 83.4% | 77.8% |

### Conclusions

*   The Decision Tree classifier was the best-performing model with a 94.4% test accuracy, demonstrating excellent predictive power for landing success.
*   Logistic Regression and SVM showed strong and consistent performance, making them reliable candidates for scenarios where model interpretability is key.
*   Data analysis revealed that booster upgrades and payload optimization are critical factors in improving landing reliability. Furthermore, launch site KSC LC-39A demonstrated the highest success rate.

## Repository Structure

```
spacex-falcon9-landing-prediction/
├── 1-Data_Collection_API.ipynb          # Collects launch data from SpaceX API
├── 2-Data_wrangling.ipynb               # Cleans and preprocesses the raw data
├── 3-Web_scraping.ipynb                 # Scrapes additional data from Wikipedia
├── 4-EDA_with_SQL.ipynb                 # Performs exploratory analysis using SQL queries
├── 5-EDA_with_Visualization.ipynb       # Creates statistical visualizations and charts
├── 6-Launch_Sites_Locations_Analysis_with_Folium.ipynb  # Geospatial analysis of launch sites
├── 7-spacex-dash-app.py                 # Interactive dashboard application
├── 8-Space_X_Falcon_9_First_Stage_Landing_Prediction.ipynb  # Machine learning modeling
├── Datasets/
│   ├── dataset_part_1.csv               # Initial dataset from SpaceX API containing raw launch data
│   ├── dataset_part_2.csv               # Dataset with landing outcome classes (1=success, 0=unsuccessful)
│   ├── dataset_part_3.csv               # Feature engineered dataset with all numerical classes for modeling
│   ├── my_data1.db                      # SQL database version used for EDA with SQL operations
│   ├── spacex_launch_geo.csv            # Augmented dataset with launch site coordinates for mapping
│   └── spacex_web_scraped.csv           # Dataset extracted from Wikipedia page with historical data
├── assets/
│   ├── crash.gif                        # Animated visualization of a failed landing
│   ├── landing_1.gif                    # Animated visualization of a successful landing
│   ├── map.html                         # Folium map export (launch site visualization)
│   ├── map2.html                        # Folium map export (alternate view)
│   ├── map3.html                        # Folium map export (alternate view)
│   ├── map4.html                        # Folium map export (alternate view)
│   ├── map5.html                        # Folium map export (alternate view)
│   └── map_final.html                   # Final polished Folium map for external viewing
├── requirements.txt                     # Python dependencies and package requirements
└── README.md                            # Project documentation (this file)
```
### Launch on Binder

Some notebooks include interactive Plotly and Folium visualizations that may not render correctly on GitHub.  
To view the fully interactive version, launch it on Binder:

[![Launch Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/filipe-braiman/spacex-falcon9-landing-prediction/HEAD)

## Installation and Usage

### Prerequisites

Ensure you have Python 3.7 or later installed on your machine.

### Steps

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2.  Install required libraries:
    ```bash
    pip install -r requirements.txt
    ```

3.  Run the Jupyter Notebooks:
    Execute the notebooks in numerical order (from 1- to 8-) to follow the project's workflow from data collection to prediction.

4.  Launch the Dash App (Optional):
    ```bash
    python 7-spacex-dash-app.py
    ```
    Then, open your web browser to the address provided in the terminal (typically `http://127.0.0.1:8050/`).

## Technologies and Libraries

*   **Languages:** Python, SQL
*   **Data Handling:** Pandas, NumPy
*   **Data Collection:** Requests, Beautiful Soup
*   **Database & Analytics:** SQLAlchemy, ipython-sql
*   **Visualization:** Matplotlib, Seaborn, Plotly, Folium
*   **Machine Learning:** Scikit-learn
*   **Web Application:** Dash

## Author
**Filipe B. Carvalho**

**Email:** [filipebraiman@gmail.com](mailto:filipebraiman@gmail.com)  
**LinkedIn:** [linkedin.com/in/filipe-b-carvalho](https://www.linkedin.com/in/filipe-b-carvalho)  
**GitHub:** [github.com/filipe-braiman](https://github.com/filipe-braiman)  

### About Me  
Data and AI professional with experience in **AI model evaluation, data annotation, and NLP projects**, currently contributing to AI initiatives at **Huawei**. Skilled in **Python, SQL, data visualization, machine learning, AI, and dataset building**, and certified through the **IBM Data Science Professional Certificate**. Multilingual in **Portuguese, English, Spanish, Turkish, and French**, bringing a linguistic and analytical perspective to data-driven problem solving. Passionate about leveraging data and AI to create practical, high-impact solutions.

## Version History

| Version | Date       | Changes                |
| :------ | :--------- | :--------------------- |
| 1.0     | 2025-10-29 | First publication.     |