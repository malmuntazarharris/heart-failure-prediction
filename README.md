# Heart Failure Prediction: Project Overview
Exploring a dataset of heart disease patients and predicting the mortality based on their comorbities and laboratory test parameters

* Load the dataset and identify the features included in the dataset
* Explore the dataset and find any trends or correlations with the features
* Preprocess the dataset for modeling
* Create models with all the features in the dataset
* Identify important features and produce models only including these features
* Create models with only ejection fraction and serum creatinine
* Compare the performances of all the models created

## Code and Resources Used 
**Python Version:** Python 3.9.7

**Packages:** pandas, numpy, sklearn, xgboost, matplotlib, seaborn

## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![correlation heatmap](https://user-images.githubusercontent.com/29358953/137792294-01e4c9a9-f586-48d0-94a8-75d4d736c836.png)
![Age](https://user-images.githubusercontent.com/29358953/137792309-c972bb2e-0489-470b-9784-19b42e160dfb.png)
![Sex pie chart](https://user-images.githubusercontent.com/29358953/137792318-cbdc70ae-3936-4edc-9ac5-121c55881719.png)

## Model Building 

First, I normalized the creatinine phosphokinase data and scaled the features in dataset. I also split the data into train and tests sets with a test size of 20%.   

I tried seven different models with three different variations of the datasets evaluated them using an accuracy score. 

I used the following models:
*	**Naive Bayes**
*	**Logistic Regression**
*	**Decision Tree**
*	**K-Nearest Neighbors**
*	**Random Forest**
*	**SVC**
*	**XGBoost**

After the first model with all the features included in the dataset, I viewed the feature importances of the model and noticed that the most important features were Age, Serum Creatinine, Ejection Fraction. 

![feature importance](https://user-images.githubusercontent.com/29358953/137794984-1f64945f-5b6d-4fe6-8172-1591d993c873.png)

After producing a model with this dataset, I further reduced the dataset to just serum creatinine and ejection fraction only as the machine learning study that the dataset was produced from found accurate results with only those two features. 

I compared all three methods and found the best result of an accuracy of 85% with the decision tree at All and Two Features and the Random Forest at All features.

![accuracy](https://user-images.githubusercontent.com/29358953/137795782-9b5045e7-e519-457f-acda-b11e2ab1f74c.png)
