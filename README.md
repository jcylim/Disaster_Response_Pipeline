# Disaster Response Pipeline Project

## Table of Contents

1. [Installation](#installation)
	* [Dependencies](#depencies)
	* [How to run project](#run_project)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Licensing, Authors, and Acknowledgements](#licensing)

### Installation: <a name="installation"></a>
#### Dependencies <a name="dependencies"></a>
In addition to the Anaconda distribution of Python versions 3.5+, please install the following packages: 
* NumPy, SciPy, Pandas, Sciki-Learn, NLTK
* Flask, Plotly 
* SQLAlchemy

#### How to run project <a name="run_project"></a>
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

### Project Motivation: <a name="motivation"></a>
In this project,I have applied data engineering, natural language processing, and machine learing skills to analyze disaster data from Figure Eight to build a machine learning pipeline that contains a model used to classify disaster messages and send the messages to an appropriate disaster relief agency. Also, this project includes a web app where an emergency worker can input a new message and get classification results in several categories.  

### File Description: <a name="files"></a>
There are a total of three folders in this project as shown below:
1. **app**
	* **template**: Folder contains the two HTML files (go.html and master.html) that the Flask web app uses to load content. 
	* **run.py**: Python code that runs the web app.  
2. **data**
    * **disaster_categories.csv**: CSV file that contains data about disaster categories.  
	* **disaster_messages.csv**: CSV file that contains data about recorded disaster messages.
	* **DisasterResponse.db**: SQLite database that contains the dataset for purpose of this project.
    * **ETL Pipeline Preparation.ipynb**: Jupyter notebook used to write and test code for "process_data.py".
    * **ETL Pipeline Preparation.html**: Exported HTML file from "ETL Pipeline Preparation.ipynb".
    * **process_data.py**: Python code that extracts, transforms/cleans, and saves processed dataset to SQLite database.
3. **models**
	* **classifier.pkl**: Pickle file that contains the machine learning pipeline.
    * **ML Pipeline Preparation.ipynb**: Jupyter notebook used to write and test code for "train_classifier.py".
    * **ML Pipeline Preparation.html**: Exported HTML file from "ML Pipeline Preparation.ipynb".
	* **train_classifier.py**: Python code that builds and trains a machine learning pipeline to output a final model for multi-output classification of disaster messages.  

### Licensing, Authors, Acknowledgements<a name="licensing"></a>
Must give credit to Figure Eight for the data.  You can find more information about Figure Eight at the link available [here](https://www.figure-eight.com/).  Otherwise, feel free to use the code here as you would like! 
