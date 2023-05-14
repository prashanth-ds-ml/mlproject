Learning from Krish naik on how to develop a End to End project going through the youtube tutorials

Step - 1

a. create a github repo
b. create a project folder and create a conda environment with in that folder
c. clone that github repo into the project folder
d. git config with email and username if its not done
e. create a readme file to track the steps in the project
f. create a setup.py and requirements.txt files

Folder structure after step 1

ML_project/
|__src/
  |__ __init__.py/
|__venv/
|__.gitignore
|__README.md
|__setup.py
|__requirements.txt

Step - 2

a. create a folder components inside src and add a init.py inside components
b. create a data_ingestion.py file in components folder
c. create a data_transformation.py file in components folder
d. create a model_trainer.py file in components folder
e. create a folder pipeline inside src and add a init.py inside components
f. create a predict_pipeline.py file in pipeline folder
g. create a train_pipeline.py file in pipeline folder
h. create a exception.py file in src folder
    change `from src.logger import logging` to `from logger import logging` if you are working in [WSL:UBUNTU] to get the log file
i. create a logger.py file in src folder
j. create a utils.py file in src folder code is written as per requirement along the way of project

Folder structure after step - 2

ML_project/
|__ logs/
|__ MLproject.egg-info/
|__ src/
  |__ __init__.py/
  |__ components/
    |__ __init__.py/
    |__ data_ingestion.py/
    |__ data_transformation.py/
    |__ model_trainer.py/
  |__ pipeline/
    |__ __init__.py/
    |__ predict_pipeline.py/
    |__ train_pipeline.py/
  |__ exception.py/
  |__ logger.py/
  |__ utils.py/
|__venv/
|__.gitignore
|__README.md
|__setup.py
|__requirements.txt


Step - 3

a. Download the data and notebooks from github
b. create a new folder Notebook and add the data folder and EDA student performance and model training.ipynb notebooks
c. go through the EDA notebook and understand the data
d. go through the model training notebook as well


ML_project/
|__ logs/
|__ MLproject.egg-info/
|__ Notebook/
  |__data/
  |__ EDA student performance.ipynb/
  |__ model training.ipynb
|__ src/
  |__ __init__.py/
  |__ components/
    |__ __init__.py/
    |__ data_ingestion.py/
    |__ data_transformation.py/
    |__ model_trainer.py/
  |__ pipeline/
    |__ __init__.py/
    |__ predict_pipeline.py/
    |__ train_pipeline.py/
  |__ exception.py/
  |__ logger.py/
  |__ utils.py/
|__venv/
|__.gitignore
|__README.md
|__setup.py
|__requirements.txt

Step - 4

a. write code in data_ingestion.py file for data ingestion configuration
b. using sklearn train_test_split split the data into train and test and store them in artifacts folder which is created using `makedirs` and join the path of the tain and test using `train_data_path: str = os.path.join('artifacts','train.csv')` and for test also similar line of code
c. add logging so that we can check weather the data ingestion started or completed

after this step the folder structure should be some thing like this

ML_project/
|__ artifacts/
  |__ data.csv/
  |__ test.csv/
  |__ train.csv/
|__ logs/
|__ MLproject.egg-info/
|__ Notebook/
  |__data/
  |__ EDA student performance.ipynb/
  |__ model training.ipynb
|__ src/
  |__ __init__.py/
  |__ components/
    |__ __init__.py/
    |__ data_ingestion.py/
    |__ data_transformation.py/
    |__ model_trainer.py/
  |__ pipeline/
    |__ __init__.py/
    |__ predict_pipeline.py/
    |__ train_pipeline.py/
  |__ exception.py/
  |__ logger.py/
  |__ utils.py/
|__venv/
|__.gitignore
|__README.md
|__setup.py
|__requirements.txt