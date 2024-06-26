# phonepe-pulse-data-visualisation-and-exploration
# What is PhonePe Pulse?
PhonePe Pulse is a feature offered by PhonePe, a popular digital payments platform in India. PhonePe Pulse provides users with insights and trends based on transactions made through the PhonePe platform. It offers data-driven analytics and visualizations, allowing users to track their spending habits, view popular merchants, understand market trends, and more.

PhonePe Pulse aims to empower users by providing them with valuable information about their financial transactions and behaviors. By offering insights into their spending patterns and preferences, PhonePe Pulse helps users make informed decisions regarding their finances and budgeting.

It's worth noting that features and offerings may evolve over time, so I recommend checking the latest information from PhonePe or their official communication channels for the most up-to-date details on PhonePe Pulse.
# Data set link: https://github.com/PhonePe/pulse#readme
# Libraries/Modules needed for the project!
Plotly - (To plot and visualize the data)
Pandas - (To Create a DataFrame with the scraped data)
mysql.connector - (To store and retrieve the data)
Streamlit - (To Create Graphical user Interface)
json - (To load the json files)
git.repo.base - (To clone the GitHub repository)
# Workflow

# Step 1:
Importing the Libraries:

Importing the libraries. As I have already mentioned above the list of libraries/modules needed for the project. First we have to import all those libraries. If the libraries are not installed already use the below piece of code to install.
    !pip install ["Name of the library"]
  If the libraries are already installed then we have to import those into our script by mentioning the below codes.
      import pandas as pd
    import mysql.connector as sql
    import streamlit as st
    import plotly.express as px
    import os
    import json
    from streamlit_option_menu import option_menu
    from PIL import Image
    from git.repo.base import Repo
# Step 2:
Data extraction:

Clone the Github using scripting to fetch the data from the Phonepe pulse Github repository and store it in a suitable format such as JSON. Use the below syntax to clone the phonepe github repository into your local drive.
    from git.repo.base import Repo
    Repo.clone_from("GitHub Clone URL","Path to get the cloded files")
    
# Step 3:
Data transformation:

In this step the JSON files that are available in the folders are converted into the readeable and understandable DataFrame format by using the for loop and iterating file by file and then finally the DataFrame is created. In order to perform this step I've used os, json and pandas packages.

# Give any column names that you want
columns1 = {'State': [], 'Year': [], 'Quarter': [], 'Transaction_type': [], 'Transaction_count': [],'Transaction_amount': []}

# Step 4:
Database insertion:

To insert the datadrame into SQL first I've created a new database and tables using "mysql-connector-python" library in Python to connect to a MySQL database and insert the transformed data using SQL commands.

Creating tables
   mycursor.execute("create table 'Table name' (col1 varchar(100), col2 int, col3 int, col4 varchar(100), col5 int, col6 double)")

# Step 5:
Dashboard creation:

To create colourful and insightful dashboard I've used Plotly libraries in Python to create an interactive and visually appealing dashboard. Plotly's built-in Pie, Bar, Geo map functions are used to display the data on a charts and map and Streamlit is used to create a user-friendly interface with multiple dropdown options for users to select different facts and figures to display.

# Step 6:
Data retrieval:

Finally if needed Using the "mysql-connector-python" library to connect to the MySQL database and fetch the data into a Pandas dataframe.

  
