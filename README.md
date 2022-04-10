# CS5228-Data-Mining
Course project for CS5228 Data Mining, Academic Year 2021-2022 Semester 2. 

Group member: [Yutong Xia](https://yutong-xia.github.io/), [Ziji Shi](https://zijishi.xyz/), [Ronghua Zhu](https://github.com/AliciaZhu-rh).

# Overview

In this project, we build a predictive model for the resale price of condominiums in Singapore. Through extensive 
exploratory data analysis, we investigate the relationship between the features, and we find some problems including 
missing values and outliers. We then perform the data transformation to clean the dataset. We augment the original 
dataset using the landmarks information, which improves the model performance. We also explore 3 types of models to 
predict the housing price: gradient boosted trees, random forests, and ridge regression. We observe that random forest
outperforms the rest in our setting. To deal with the exploding hyper-parameter search space, we also explore Bayesian 
Optimization. We believe this study can provide more insights to the factors that impact the property price, and help 
the future policy-making. 

You can visualize the property price through the website [here](https://cs5228-demo.netlify.app/).

Our report is accessible [here](CS5228_Report.pdf). 


# Project Structure

```
├── CS5228_Report.pdf
├── EDA
├── Preprocessing
├── GeoDataAugment (code to calculate nearest facilities to augment dataset)
├── README.md
├── Regression (model and experiment scripts)
├── dataset
│   ├── README.md
│   ├── auxiliary-data
│   ├── distance
├── distance_attributes (data for landmark info)
│   ├── test_distance_attributes.csv
│   └── train_distance_attributes.csv
├── model (serialized model weights)
├── plots (plots for the report)
├── prediction (submissions to Kaggle)
└── requirements.txt

```

# Reproducing the result

## Installation

```bash
pip install -r requirements.txt
```

## Exploratory Data Analysis

Follow `EDA/data_visualisation.ipynb`.

## Data Preprocessing

1. Duplication removal and filling missing values: `Preprocessing/missing_value_part1.ipynb`
2. Outlier removal: `Preprocessing/Dataset_Preparation.ipynb`


## Model and Evaluation

1. XGBoost: `Regression/xgboost_v2.ipynb`
2. Ridge Regression: `Regression/rf_and_ridge.ipynb`
3. Random Forest: `Regression/rf_and_ridge.ipynb`

