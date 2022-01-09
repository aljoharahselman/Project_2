# Disaster Response Pipeline Project

# -DisasterResponsePipelines
Introduction:
After every natural disaster, people start to send out messages to ask for help in my channels such as social media to ask for food and water support or they're simply trapped somewhere, and the goverment doesn't have enough time to save everyone during this.
This the second  project in data science nanodegree program of udacity and meant to analyze people messages to respond to disasters, The dataset contains pre-labelled tweets from real life disasters. the goal of the project is to build a Natural language processing tool that categorize tweets and messages. 

We can divid the project into these sections:
processing data, ETL Pipline where we extracting data from it source, cleaing and saving the data in proper structure.
Machine learining Pipline for the training model to classify messages into defined categories. 
Wep application to show the model results in real time.

File and folders of data: contains sample messages and the categories in CSV format 
|- DisasterCategories.csv #date to process
|- Disasternessages.csv #date to process
|- process_data.py #the python code that is taken as an inpout CVS files (the message data and categories datasets) clean and then creates a SQL database 
|- insertdatabaseName.db #a data base that is used to save data to
application: where the run.py to deploy the web application
|- template
|-|- master.html #the main page of the web application 
|-|- Run.html #classification results of the web application 
|- run.py #flask file that runs application models 
|-| trained_classifier.py #A code used to train the mechine learning model with SQL database
|- classifier.pkl #to save the model to 
|- ETL Pipline preparation.ipynb: process_data.py development
|- Mechine learning Pipeline preparation.ipynb: train_classifier.py development 
README.md
installation
python (more than =>3.6)
panadas
numpy 
sqlalchemy
plotly
sklearn
joblib
sys
flask 
nltk 

Instructuins that I highly recommend

1- Run the commands in the project root directory to set up your database and model properely 
2- To run ETL pipline that cleans and stores in the database python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
3- To run mechain learning pipline that train the classifier and save python models/train classifier.py data/disasterresponse.db models/classifier.pkl
4- Run the command in the app directory to run the web application pythinrun.py

Axknowledgements:
Ian thankful for udacity for their informative course 
Figure Eight for the dataset to train my model 

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
