# [Applied Data Science Capstone](https://github.com/aaysul/applied-data-science-capstone)

This repository holds the notebooks that were completed during the Capstone Project for the **IBM Data Science Professional Certificate** on Coursera. The aim is to predict whether the SpaceX Falcon 9 first stage will land based on the data from previous launches. The data supporting the prediction is gathered using various sources. The project involves various steps to gather, clean and analyze data and then use it to predict the outcome of a first stage booster landing. The project alos requires a presentation in order to share the findings. Following is the step by step breakdown of the project.

  1. Data Collection
  2. Data Wrangling 
  3. Exploratory Data Analysis (EDA) with SQL
  4. Exploratory Data Analysis (EDA) with Visualization
  5. Interactive Visual Analytics and Dashboards
  6. Predictive Analysis (Classification)
  7. Final Presentation
  
## 1. Data Collection  
   The data collection process involves using different methods to acquire data. These include using API or web scraping.
   * **Using SpaceX API** \
  This is the first lab for the data collection process. It involves data collection on SpaceX launches using the API. The notebook for the lab is available [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex-data-collection-api.ipynb). The data through API is available as follows,
      - Booster version details are available at https://api.spacexdata.com/v4/rockets/
      - Launch Site details are at https://api.spacexdata.com/v4/launchpads/
      - Payload data is available at https://api.spacexdata.com/v4/payloads/
      - Cores data is at https://api.spacexdata.com/v4/cores/
   * **Using Web Scraping** \
   This is the second lab for the data collection process. It involves data collection through web scraping. The notebook for this lab is available [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex-data-collection-webscraping.ipynb). The data is available as follows,
      - SpaceX Falcon9 and Falcon Heavy launch data available at https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches
## 2. Data Wrangling
   The purpose of this lab is to perform exploratory data analysis (EDA) to find patterns in data and determining the training labels for supervised learning model. The notebook for this lab is [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex-data-wrangling.ipynb). Following tasks are performed,
   * Explore number of Launches per Launch Site
   * Explore number of Launches per Orbit
   * Create landing outcome Labels for Training
   
The landing outcomes were converted to landing class.

| **Outcome**       | **Class**   |
| ------------------|------------:|
| Success           | 1           |
| Failure           | 0           |
        
## 3. Exploratory Data Analysis (EDA) with SQL
   This lab involves using SQL within the python environment as the primary language for manipulation. The lab notebook is [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex-eda-sql-coursera_sqllite.ipynb). Following launch information is explored,
   * Landing Outcomes by Launch Sites
   * Landing Outcomes by Landing Platforms
   * Landing Outcomes by Dates
   * Payload Mass by Booster Versions
   * Ranking of Landing Outcomes within given period

## 4. Exploratory Data Analysis (EDA) with Visualization
   The jupyter notebook for the lab is [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex-eda-dataviz.ipynb). In this lab two of the popular python libraries are used,
   * Pandas
   * Matplotlib

   Following relationships are explored using visualization,
   * Flight No. and Launch Site
   * Payload and Launch Site
   * Success rate and Orbit type
   * Success class, Flight No. and Orbit type
   * Payload and Orbit type
   * Yearly trend for Launch Success
   * Feature Engineering (one-hot-encoding) for categorical variables
   
     - Orbit
     - Launch Site
     - Landing Pad
     - Serial
 
## 5. Interactive Visual Analytics and Dashboards
   Visualizing site locations and building dashboards is the next step. This phase included following tasks,
   * Plot markers on map using Folium
     - Mark all site locations on the map
     - Mark successful / failed launches for each site on the map
     - Calculate the distances from launch sites to its proximities
      
     The associated notebook is [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex_launch_site_location.ipynb).
      
   * Build an interactive dashboard with Plotly Dash.
   
     It involves creating a dash application consisting of the following dashboard elements,
     - A drop-down menu to select all launch sites or a specific one
     - A pie chart to show success count for all sites or the success rate for a specific site as selected from the drop-down
     - A slider control to select payload mass range
     - A scatter chart updated as a result of user selection from drop-down or the payload mass slider
     
     The notebook can be viewed [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/spacex_dash_app.ipynb). 

## 6. Predictive Analysis (Classification)
   Finally we use various classifiers to predict if the landing will be successful. The notebook can be viewed [here](https://github.com/aaysul/applied-data-science-capstone/blob/main/SpaceX_Machine%20Learning%20Prediction.ipynb). Following classification techniques have been used,
   * Logistic Regression
   * Support Vector Machine
   * Decision Tree
   * K-Nearest Neighbours
   
   Each of the classifier score is obtained. Confusion matrix is plotted to identify false outcomes. Decision Tree Classifier is found to work best.
   
## 7. Final Presentation
   In the end the entire working is shared in the form a presentation that explain the data acquisition, organizing, cleaning and processing tasks. The methodology is explained and the insights into the data are shared with visualizations. The conclusion details the findings of the study. Follow the link to view the presentation.
