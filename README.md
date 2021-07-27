# Rainfall-Prediction

## Overview
This is a Flask web app which predicts whether it will rain tomorrow or not.

## Dataset:
https://www.kaggle.com/jsphyg/weather-dataset-rattle-package

## About the project:

Firstly, the dataset was bisected and numerical(continuous,discrete) and categorical features were identidied. Missing Values were handled using Random Sample imputation to maintain the variance,Categorical Values like location, wind direction are handled by using Target guided encoding. Outliers are handled using IQR and boxplot. Feature scaling was also performed but it was not required. This is present in the ipynb file named "Data Preprocessing".
Secondly, Feature Selection and was done but all the features were considered as it has only 25 features. This is present in the ipynb file named "Feature Selection".
Finally, Imbalanced Dataset was handled using SMOTE. Model Creation was then performed. Different types of models were tried like catboost, random forest, logistic regression, xgboost, support vector machines, knn, naive bayes and Decision tree.Out of these models the best classifier was selected. Catboost, random forest and Xgboost were the top 3. 
However, Xgboost out performed others slightly. So, the best classifier model was Xgboost. Hyperparameter Optimazation was also performed but due to system compatibility a small sample out of the dataset was considered for these models.
The conclusion were made using classification metrics. roc curve and auc score

## Installation
The Code is written in Python 3.7.3 If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:

##### 1. First create a virtual environment by using this command:
```bash
conda create -n myenv python=3.7
```
##### 2. Activate the environment using the below command:
```bash
conda activate myenv
```
##### 3. Then install all the packages by using the following command
```bash
pip install -r requirements.txt
```
##### 4. Then, in cmd or Anaconda prompt write the following code:
```bash
python app.py
```
##### Make sure to change the directory to the root folder.  

## Deployement on Heroku
Login or signup in order to create virtual app. You can either connect your github profile or download Heroku CLI to manually deploy this project.

[![](https://i.imgur.com/dKmlpqX.png)](https://heroku.com)

Our next step would be to follow the instruction given on [Heroku Documentation](https://devcenter.heroku.com/articles/getting-started-with-python) to deploy a web app.

## Directory Tree that is used in Model Deployment 
```

├── templates
│   ├── home.html
    ├── rainy.html
    ├── sunny.html
├── static
    ├── predictor.css
    ├── style01.css
├── Procfile
├── README.md
├── app.py
├── Xgboost model.ipynb
├── xg_random.pkl
├── requirements.txt
```
The rest ipynb files are for selecting the best classifier.

![Rainy Day - Google Chrome 2021-07-28 02-20-23](https://user-images.githubusercontent.com/75041273/127225796-42dbda09-8e3b-44b0-a159-3654c087b3a8.gif)
