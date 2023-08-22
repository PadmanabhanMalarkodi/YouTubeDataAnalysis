# YouTube Data Harvesting and Warehousing

YouTube has emerged as a treasure trove of information, offering a plethora of insights into user behavior, content trends, and engagement metrics. Let's delve into a brief overview of this project.

## Introduction

YouTube data harvesting involves the systematic collection of data from this sprawling video-sharing platform. We're not just talking about videos, but also user interactions, comments, and more. This rich repository of structured (metadata, metrics) and unstructured (comments, content) data presents us with a goldmine of information waiting to be explored.

### 1. Tools Installed

* Virtual Studio code
* Jupyter notebook
* Python 3.11.3 or higher
* MySQL
* MongoDB
* Youtube API key

### 2. Required Libraries

* pip install google-api-python-client, pymongo, mysql-connector-python, sqlalchemy, mysql workbench, pymysql, pymysql, pandas, numpy, 
  plotly-express, streamlit.
  
 ( pip install google-api-python-client pymongo mysql-connector-python sqlalchemy pymysql pandas numpy plotly-express streamlit )
 
### 3. Import Libraries

**Youtube API libraries**
* from googleapiclient.discovery import build

**File handling libraries**
* import json
* import re

**MongoDB**
* import pymongo

**SQL libraries**
* import mysql.connector
* import sqlalchemy
* from sqlalchemy import create_engine
* import pymysql

**pandas, numpy**
* import pandas as pd

**Dashboard libraries**
* import streamlit as st
* from streamlit_option_menu import option_menu

### 4. E T L Process

#### a) Extract data

* Extract the particular youtube channel data by using the youtube channel id, with the help of the youtube API developer console.

#### b) Process and Transform the data

* After the extraction process, takes the required details from the extraction data and transform it into JSON format.

#### c) Load  data 

* After the transformation process, the JSON format data is stored in the MongoDB database, also It has the option to migrate the data to MySQL database from the MongoDB database.

### 5. E D A Process and Framework

#### a) Access MySQL DB 

* Create a connection to the MySQL server and access the specified MySQL DataBase by using pymysql library and access tables.

#### b) Filter the data

* Filter and process the collected data from the tables depending on the given requirements by using SQL queries and transform the processed data into a DataFrame format.

#### c) Visualization 

* Finally, create a Dashboard by using Streamlit and give dropdown options on the Dashboard to the user and select a question from that menu to analyse the data and show the output in Dataframe Table.


## User Guide

#### Step 1. Data collection Tab

* I have provided 10 channel ids in a table format for my convenience. We can also extract channel ids from YouTube page source.

#### Step 2. Select and Store Tab

* In **Enter a channel_id** copy and paste channel id in the input box, press enter and click **Store data in MongoDB** button in the **Select and Store Tab**.

#### Step 3. Migration of Data Tab

* Select the **channel name** and click the **Migrate to MySQL** button to migrate the specific channel data to the MySQL database from MongoDB in the **Migration of Data Tab**.

#### Step 4. Data Analysis Tab

* **Select a Question** from the dropdown option and you can get the results in **Dataframe format**.

