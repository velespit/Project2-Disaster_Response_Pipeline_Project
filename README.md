### Disaster Response Pipeline Project

#Project Motivation

Apply Data Engineering to Build ETL; NLP Pipelines and Create an App for Disaster Relief using Flask

In this project, I am applying Data Engineering & Data Science skills to analyze disaster data from Udacity to build a model for an API that classifies disaster messages.

The project contains data set containing real messages that were sent during disaster events.
I am creating a machine learning pipeline to categorize these events so that it can be sent to an appropriate disaster relief agency.

Project includes a web app where an emergency worker can input a new message and get classification results in several categories. The web app displays visualizations of the data.

# Instructions to Run the Python Scripts

1. Run the following commands in the project's root directory to set up your database and model.
	- To run ETL pipeline that cleans data and stores in database:
	`python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`

	- To run ML pipeline that trains classifier and saves it:
	`python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run the web app.
	- 	`python run.py`

3. Go to `http://0.0.0.0:3001/`

### There are three components in this project.

1) ETL Pipeline
A Python script, process_data.py, a data cleaning pipeline that:

- Loads the messages and categories datasets
- Merges the two datasets
- Cleans the data
- Creates a vocabulary
- Stores the data and vocabulary in a SQLite database

2) ML Pipeline
A Python script, train_classifier.py, a machine learning pipeline that:

- Loads data from the SQLite database
- Splits the dataset into training and test sets
- Builds a text processing and machine learning pipeline
- Trains and tunes a model using GridSearchCV
- Outputs results on the test set
- Exports the final model as a pickle file

3) Flask Web App
run.py
- Loads data from the SQLite database
- Loads classification model
- Extract data for visualisations 
- Runs the web app

#Volkan#