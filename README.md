# Rainfall-Prediction

## Overview
This is a Flask web app which predicts whether it will rain tomorrow or not.

## Dataset:
https://www.kaggle.com/jsphyg/weather-dataset-rattle-package

## About the project:

Firstly, the dataset was bisected and numerical(continuous,discrete) and categorical features were identified. Missing Values were handled using Random Sample imputation to maintain the variance,Categorical Values like location, wind direction were handled by using Target guided encoding. Outliers were handled using IQR and boxplot. Feature scaling was also performed but it was not required. These are present in the ipynb file named "Data Preprocessing".
Secondly, Feature Selection was done considering correlation heatmap and Extra Trees Classifier and plotting the feature importances but all the features were considered as it has only 25 features. This is present in the ipynb file named "Feature Selection".
Finally, Imbalanced Dataset was handled using SMOTE. Model Creation was then performed. Different types of Machine Learning algorithms were tried like catboost, random forest, logistic regression, xgboost, support vector machines, knn, naive bayes and Decision tree. Out of these models the best classifier was selected. Catboost, random forest and Xgboost were the top 3. 
However, Xgboost out performed others slightly. So, the best classifier model was Xgboost. Hyperparameter Optimazation was also performedusing RandomizedSearchCV but due to system limitations a small sample out of the dataset was considered.
The conclusion were made using classification metrics, roc curve and auc score.

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

## Frontend Using HTML,CSS and Backend using Flask

http://rainpredsm.herokuapp.com/

![Screenshot (93)](https://user-images.githubusercontent.com/75041273/127237352-4519280e-0212-47c6-9f17-28791b3f6467.png)

![Rainy Day - Google Chrome 2021-07-28 02-20-23](https://user-images.githubusercontent.com/75041273/127236925-4f893eea-9fa9-41a0-9ff6-89d7dadf2ff9.gif)

![Rainy Day - Google Chrome 2021-07-28 04-11-31](https://user-images.githubusercontent.com/75041273/127237047-df6d69a0-461b-425c-abd8-b011dd9c567f.gif)


## Technology Stack

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://scikit-learn.org/stable/_static/scikit-learn-logo-small.png" width=200>](https://scikit-learn.org/stable/) 

## Further Changes to be Done

- [ ] Deploying the Web Application on Cloud.
     - [ ] Google Cloud 
     - [ ] Azure
     - [ ] AWS EC2 Instance


