# Disaster-Management-Response

Disaster_Response_project
Web API that classifies disaster messages.

![image](https://user-images.githubusercontent.com/109017256/192577353-e759a63f-8f67-405f-add2-526d115eb132.png)
![image](https://user-images.githubusercontent.com/109017256/192577391-9792944f-7d70-4a97-8445-91b682b4e5f9.png)


Project Motivation
Project Summary
Project Components
File Descriptions
Installation & Run
Results
1. Project Motivation
I recently gained some data engineering skills So, I found out this project can help me build an overall intution about Data engineering. I applied these skills to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages.

2. Project Summary
So, how this application helps people or organisation during disaster?. After running the app in the browser you have to put a message/query that you want process afte a while you will see to which departmen it belongs to. For eg your if your message goes like this "We need food and shelter" then it would recognize it belongs to food,shelter, or any helth emergency.

3. Project Components
This project basically divided into three sections as follows:

ETL (Extract Transform Load) Pipeline
Loads the messages and categories datasets
Merges the two datasets
Cleans the data
Stores it in a SQLite database
Machine Learning Pipeline
Loads data from the SQLite database
Splits the dataset into training and test sets
Builds a text processing and machine learning pipeline
Trains and tunes a model using GridSearchCV
Outputs results on the test set
Exports the final model as a pickle file
Flask Web App
Load the pickle file
Clean(Tokenize) a query
Predict the model
Make visualization of data
Produce the final result
4. File Structure & Description
app

| - template

| |- base.html #my-dashboard's base page

| |- home.html #my-dashbord's welcome page

| |- master.html # main page of web app

| |- go.html # classification result page of web app

|- run.py # Flask file that runs app

data

|- disaster_categories.csv # data to process

|- disaster_messages.csv # data to process

|- process_data.py

|- disaster_response.db # database to save clean data to

models

|- train_classifier.py

|- trained_model.pkl # saved model

README.md

Data Directory
This folder contains "process_data.py" which has all ETL code and perform pipeline tasks which takes input files "message.csv" & "categories.csv" produces database file for our model.
Model Directory
This folder has "train_classifier.py" which takes database file perform ML pipeline and produces pickle file to use it in our flask app.
App directory
this folder contains web page code. "run.py" takes care of running server & all our code. upper folders are templetes and static which contain html & css, java files respectively.
5. Installation & Run
After downloading you need to have your fav code editor, I use pycharm. It's your choice what to use.

At very first go to the data folder & run process_data.py file. Check out file description above & documentation in the file for guidence.
Second is the model folder which has train_classifier.py file which you have to run. Check out file description above & documentation in the file for guidence.
thirdly run app.py file from app folder which runs the whole web app. Check out file description above & documentation in the file for guidence.
5. Results
I tried with couple of algorithms, with various parameters & also with custom estimators after examining all those things I come with this solution which outputs better results and performs faster compare to all those methods. If you wanna see those Exploratory analysis then checkout that repo. It performs with 94.85 accuracy I have also provided classification reports.

Also check out output.txt file for the full result.

Screenshot (260)
