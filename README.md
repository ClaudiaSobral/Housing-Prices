# 🏡 Housing Prices Prediction with Linear Regression

This project focuses on predicting real estate prices using linear regression. Through a structured pipeline — from exploratory data analysis to model evaluation — I aimed to identify key features influencing housing prices and build a simple yet insightful predictive model.

## 🔍 Project Overview

This notebook includes the following steps:

1. **Exploratory Data Analysis (EDA)**  
   Performed descriptive statistics using `pandas` and visualized feature distributions to understand data patterns and detect potential outliers.

2. **Feature Relationship Analysis**  
   Plotted pairwise relationships between features to identify potential candidates for linear regression. In particular, the relationship between `area` and `price` showed strong linear correlation.

3. **Feature Engineering**  
   Selected key features:
   - Area
   - Bedrooms
   - Bathrooms
   - Floors
   - Garage Spaces  
   The target variable is `price`.

4. **Model Training**  
   - Split the data into training and testing sets using `train_test_split`.
   - Trained a Linear Regression model with `scikit-learn`.
   - Extracted model coefficients and identified that `area` and `floors` had the strongest influence on price.

5. **Model Evaluation**  
   - Compared predicted vs actual prices in the test set.
   - Evaluated using:
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - Root Mean Squared Error (RMSE)
   - Analyzed residuals: the distribution showed a right-skewed tail, suggesting that the model underperforms when predicting high-price outliers.

6. ** Known issues and future improvements**
   - Removing or transforming outliers to improve regression fit
   - Trying log transformation of the target variable to reduce skew
   - Exploring other regression models (Ridge, Lasso, or Tree-based methods)

## 📂 Project structure
Housing-Prices/<br>
│<br>
├── data/<br>
│   └── Housing.csv               # raw data<br>
├── notebooks/<br>
│   └── housing.ipynb             # Main notebook<br>
├── requirements.txt<br>
├── README.md<br>
└── .gitignore<br>

## 📈 Key Insights

- **Area** was the most influential predictor, as expected.
- **Floors** had more impact than initially assumed.
- The model performs reasonably well on typical cases but struggles with outlier values (very high prices).
- Residual analysis revealed a long right tail, indicating non-normal residuals and possible heteroscedasticity.
## 🙌 Thank you

A huge thank you to [alejandro-ao](https://github.com/alejandro-ao), who provided a great framework and tutorial in his [YouTube class about Linear Regression](https://youtu.be/O2Cw82YR5Bo?si=RQkSIDJl2vTEeiti).<br>
Another huge thanks to the owner of the public dataset, [HARISH KUMARdatalab](https://www.kaggle.com/harishkumardatalab), that can be found [here](https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction).

## 🔧 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt

