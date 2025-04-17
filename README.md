# Y-data-profiling
Perform an EDA of dataset subject_info using YDATA Profiling.
What is EDA?
Exploratory Data Analysis (EDA) is an analysis approach that identifies general patterns in the data. These patterns include outliers and features of the data that might be unexpected. EDA is an important first step in any data analysis.

Why use ydata-profiling? 
ydata-profiling is a valuable tool for data scientists and analysts because it streamlines EDA,provides comprehensive insights, enhances data quality, and promotes data science best practices.

In the early stages of any data science or machine learning project, one of the most crucial steps is exploratory data analysis (EDA). Understanding the structure, patterns, and issues within your dataset can dramatically shape the outcome of your model-building process. This is where YData Profiling comes in.

Previously known as Pandas Profiling, YData Profiling is an open-source Python library that automates EDA, helping data analyst/data scientists save time and gain deeper insights with just a few lines of code.

YData Profiling generates an in-depth profiling report of your dataset. It analyzes the data and provides a visual and statistical summary including, This allows you to quickly spot anomalies, understand distributions, and make informed decisions for cleaning or preprocessing the data.
Data types,Missing values,Descriptive statistics,Correlations,Duplicate rows,Interactions between variables,Data distributions

Steps to craete code in jupyter notebook
 Step 1: Launch Jupyter notebook from anaconda navigator
 Step 2 : Create new jupyet notebook to write below code, make sure to have subject_info.csv dataset in your local machine or in your server
 Step 3 :  Install this package inorder to perform EDA on any dataset - !pip install ydata-profili 
 Step 4 : If you already have above package installed make sure to upgrade to latest version by installing this package - pip install -U ydata-profiling

# Follow below code
#Perform an EDA of dataset subject_info using YDATA Profiling.
#Install below library
#!pip install ydata-profiling
#pip install -U ydata-profiling

#import below libraries
import pandas as pd
from ydata_profiling import ProfileReport

#To read .csv file
df1 = pd.read_csv("subject-info.csv")
#df1.info()

#generates an in-memory profiling report object for your dataset (df1).
profile = ProfileReport(df1, title="Profiling Report")

#display profile report output
profile.to_notebook_iframe()

#export report to html file
profile.to_file("subject_info_report.html")


