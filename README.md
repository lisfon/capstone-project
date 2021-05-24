####Capstone Project - Starbucks ####

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions and Instructions](#files)
4. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

The code should run with no issues using Python versions 3.* All extra libraries to be imported are listed in the Jupyter Notebook. Pandas must be upgraded to the most recent version.

## Project Motivation<a name="motivation"></a>

The goal of this project, which is the capstone project of the Data Scientist Nanodegree Program, is to identify patterns of behaviour of customers purchasing through the Starbucks app. By analysing the response of each demographic group to the various offers it is possible to optimize the offers pushed to each customers and consequently to positively influence their purchasing behaviour.

## File Descriptions and Instructions <a name="files"></a>

Overall structure of the repository:

app<br>
| - template<br>
| |- master.html # main page of web app<br>
| |- go.html # classification result page of web app<br>
|- run.py # Flask file that runs app<br>
data<br>
|- disaster_categories.csv # data to process<br>
|- disaster_messages.csv # data to process<br>
|- process_data.py<br>
|- DisasterResponse.db # database to save clean data to models<br>
|- train_classifier.py<br>
|- classifier.pkl # saved model<br>
README.md<br>

In detail the folders are containing the following scripts and files: 
- app: containing the script for a web app showing visualizations of the data and a classification function, as well as the folder templates with the master and go html files for the structures and visualizations in the app
- data: containing the two datasets used as input as well as the cleaned and prepared dataset obtained from their merge and the Python code for the data preparation. The detailed process can be viewed in the ETL Pipeline Preparation Jupyter notebook, while the final script to be run is saved as process_data.py.
- models: containing the machine learning pipeline to categorize the disaster events. The detailed process of evaluation and selection of the most suitable machine learning algorithm can be viewed in the ML Pipeline Preparation Jupyter notebook, while the final script with the tuned model is saved as train_classifier.py.

Instructions for running the scripts and using the web app:

- ETL pipeline: to clean data and store the processed data in the database the script to be run is: <br>python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
- ML pipeline: to load data from DB, train classifier and save the classifier as a pickle file the script to be run is: <br>python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
- The classification web app and the data visualizations are available in the Flask web app, which can be accessed at the address http://0.0.0.0:3001/ after running the script     python run.py in the app folder.
  The web app consists of a search bar where messages can be inputted for classification and descriptive visualisations of the dataset used for this project.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Credit for the data and the project initiative goes to Figure Eigth and Udacity.
