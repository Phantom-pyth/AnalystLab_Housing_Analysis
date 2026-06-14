# Housing Price Analysis

> Exploratory Data Analysis (EDA) to identify key factors influencing residential property prices.

## Project Overview

This project performs a comprehensive analysis of a housing dataset containing 545 residential property records across 13 features. The goal is to uncover which property characteristics most significantly influence price  providing actionable insights for buyers, sellers, developers, and data scientists building predictive models.


## Repository Structure

housingpriceanalysis
Housing.csv                     Original raw dataset
Housing_Cleaned.csv             Cleaned & encoded dataset (ready for ML)
Housing_Price_Analysis.ipynb   Full Jupyter Notebook (EDA + visualizations)
Housing_Insight_Report.docx    Insight Summary Report (Word document)
README.md                      This file




## 📊 Dataset Description

 Property  Details 

 Source  Housing.csv 
 Rows  545 
 Columns  13 
 Target Variable  `price` 
 Missing Values  None 
 Duplicates  None 

### Features

 Feature  Type  Description 

 `price`  Numeric  Property sale price 
 `area`  Numeric  Floor area in square feet 
 `bedrooms`  Numeric  Number of bedrooms 
 `bathrooms`  Numeric  Number of bathrooms 
 `stories`  Numeric  Number of stories 
 `parking`  Numeric  Number of parking spaces 
 `mainroad`  Binary  Located on main road (yes/no) 
 `guestroom`  Binary  Has guest room (yes/no) 
 `basement`  Binary  Has basement (yes/no) 
 `hotwaterheating`  Binary  Has hot water heating (yes/no) 
 `airconditioning`  Binary  Has air conditioning (yes/no) 
 `prefarea`  Binary  Located in preferred area (yes/no) 
 `furnishingstatus`  Categorical  Furnished / Semifurnished / Unfurnished 



## Analysis Summary

### Part 1  Data Loading & Inspection
 Dataset loaded with Pandas; first 10 rows displayed
 Structure inspection: dtypes, shape, missing values, duplicates
 Finding: Dataset is complete and clean with no missing values or duplicate records

### Part 2  Data Cleaning
 Binary yes/no columns encoded as 0/1 integers
`furnishingstatus` ordinally encoded (unfurnished=0, semifurnished=1, furnished=2)
 Cleaned dataset exported as `Housing_Cleaned.csv`

### Part 3  Exploratory Data Analysis
 Univariate: Histograms, boxplots, and bar charts for all features
 Bivariate: Price relationships with area, bedrooms, bathrooms, AC, furnishing, and stories

### Part 4  Correlation & Feature Importance
 Full correlation matrix computed and visualized as a heatmap
 Features ranked by absolute correlation with `price`

### Part 5  Insights & Recommendations
 7 key insights derived from the analysis (see report for full detail)



## Key Insights

 #  Insight  Correlation (r) 

 1  Area is the strongest price driver  0.54 
 2  Bathrooms outperform bedrooms as a price signal  0.52 
 3  Air conditioning commands a significant premium  0.45 
 4  Stories reflect increased total area and add value  0.42 
 5  Preferred area location adds consistent location premium  0.33 
 6  Hot water heating is essentially priceirrelevant  0.09 
 7  Outlier properties are legitimate luxury homes, not data errors   



## Technologies Used

 Python 3.x
 Pandas  data loading, cleaning, manipulation
 NumPy  numerical operations
 Matplotlib  base plotting
 Seaborn  statistical visualizations and heatmaps
 Jupyter Notebook  interactive analysis environment



## Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Run the Analysis

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/housingpriceanalysis.git
cd housingpriceanalysis

# Launch the Jupyter Notebook
jupyter notebook Housing_Price_Analysis.ipynb
```

The notebook will walk through all 5 parts of the analysis endtoend.



## Feature Importance Summary

For ML model development, features are tiered as follows:

 Tier  Features  Action 
 High importance  area, bathrooms, airconditioning, stories  Always include 
 Moderate importance  parking, bedrooms, prefarea, furnishingstatus  Include by default 
 Low importance  mainroad, guestroom, basement  Test inclusion 
 Negligible  hotwaterheating  Consider dropping 



## Outputs

 `Housing_Cleaned.csv`  Analysisready dataset with encoded categorical variables
 `Housing_Price_Analysis.ipynb`  Complete reproducible analysis notebook
 `Housing_Insight_Report.docx`  Executive insight summary with 7 detailed insights and recommendations



## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.



## License

This project is open source 