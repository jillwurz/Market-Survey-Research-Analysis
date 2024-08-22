# Market Research Survey Dataset Analysis

This project focuses on analyzing a market research survey dataset. The analysis involves exploratory data analysis (EDA), data transformation, and machine learning model implementation to understand patterns and make predictions based on the given features.

## Dataset Overview

The dataset contains responses to a market research survey. The survey includes questions on various demographics and preferences, such as yearly salary, age, education level, car make, region (based on zip code), credit availability, and preferred computer brand.

### Survey Questions and Response Key

1. **What is your yearly salary, not including bonuses?**
   - Respondents enter a numeric value.
   
2. **What is your age?**
   - Respondents enter a numeric value.
   
3. **What is the highest level of education you have obtained?**
   - Respondents select from the following 5 choices:
     - 0: Less than High School Degree
     - 1: High School Degree
     - 2: Some College
     - 3: 4-Year College Degree
     - 4: Master's, Doctoral or Professional Degree
     
4. **What is the make of your primary car?**
   - Respondents select from the following 20 choices:
     - 1: BMW
     - 2: Buick
     - 3: Cadillac
     - 4: Chevrolet
     - 5: Chrysler
     - 6: Dodge
     - 7: Ford
     - 8: Honda
     - 9: Hyundai
     - 10: Jeep
     - 11: Kia
     - 12: Lincoln
     - 13: Mazda
     - 14: Mercedes Benz
     - 15: Mitsubishi
     - 16: Nissan
     - 17: Ram
     - 18: Subaru
     - 19: Toyota
     - 20: None of the above

5. **What is your zip code?**
   - Respondents enter their zip code, which is captured as one of the following 9 regions in the U.S.:
     - 0: New England
     - 1: Mid-Atlantic
     - 2: East North Central
     - 3: West North Central
     - 4: South Atlantic
     - 5: East South Central
     - 6: West South Central
     - 7: Mountain
     - 8: Pacific

6. **What amount of credit is available to you?**
   - Respondents enter a numeric value.
   
7. **Which brand of computers do you prefer?**
   - Respondents select from the following 2 choices:
     - 0: Acer
     - 1: Sony

## Exploratory Data Analysis (EDA)

The dataset was first explored to understand its structure, identify missing values, and examine relationships between variables. Key steps included:

- **Data Description**: Overview of the dataset's main statistics, such as mean, standard deviation, and distribution of responses.
- **Correlation Analysis**: A heatmap was used to visualize correlations between features.
- **Data Visualization**: Various visualizations (e.g., histograms, box plots, count plots) were created to understand the distribution of features like education level, car make, zip code, computer brand, and more.

## Data Transformation

The dataset's categorical variables were transformed into more readable formats:

- **Education Level**: Mapped numeric values to their respective descriptions.
- **Car Make**: Converted numeric values to corresponding car brands.
- **Zip Code**: Transformed numeric values into U.S. regions.
- **Computer Brand**: Converted numeric values to 'Acer' or 'Sony'.

## Machine Learning Models

Two machine learning models were implemented to predict the preferred computer brand (Acer or Sony) based on other features in the dataset:

1. **Random Forest Classifier**
   - Accuracy: 92.22%
   - Top Features: `salary`, `age`, `credit`

2. **XGBoost Classifier**
   - Accuracy: 90.86%
   - Top Features: `age`, `salary`, `credit`

### Feature Importance

Both models identified `salary`, `age`, and `credit` as the top three most important features for predicting the preferred computer brand.

### Confusion Matrix

Confusion matrices were generated for both models to assess their performance in terms of correctly and incorrectly classified instances.

## Conclusion

This analysis provided insights into how demographic factors such as salary, age, and credit availability influence computer brand preferences. The Random Forest model outperformed the XGBoost model in terms of accuracy.

## Files in This Repository
- `Market Survey Research Analysis.ipynb`
- `CompleteResponses.csv`
