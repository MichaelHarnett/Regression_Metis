# Metis Linear Regression Module
This repository was created as a project for METIS to learn the principles behind web scraping and linear regression. I chose to try and predict the popularity of video games, based on ownership. Data was aquired with a combination of selenium and beautiful soup, through scraping the Steam Game Store and SteamSpy.com, supplemented by data aquired through SteamSpy's API. A combination of StatsModels and Sci-Kit Learn was then used to find the most accurately predictive model, with the lowest error cost.  

## Description of included Jupyter notebooks
This is a working notebook, and is not fully cleaned and organized, at this point, the notebooks should be followed in this order to see workflow from start to finish:
<br>
<br>
<b>steam_scraping</b> - All of the code used to scrape data from Steam Game Store, and transform it into a data frame. The final data frame from this is saved in the data folder as totaldf.csv<br>
<b>final_df_editing</b> - EDA and cleaning on data scraped from Steam Game Store. Final result saved as reviewsdf.csv<br>
<b>steamspy_api_scraping</b> - The code used to aquire information from SteamSpy's API. This was done before scraping SteamSpy, to see if the data would provide meaningful features to improve the linear regression model. The data provided from the API is more general than on the actual site, so this was a preliminary step.<br>
<b>steamspy_scraping</b> - The code used to scrape more exact data from SteamSpy's actual website. <br>
<b>merging_modeling</b> - *likely to be removed* preliminary merging of all data sources, and base-line modeling.<br>
<b>target_transformations</b> - The target (owners) was unevenly distributted, this notebook shows different transformations on the target variable, without feature selection or engineering, to see which transformation would be the best to move forward with. Models were scored using r^2, mean absolute error, and root mean squared error.



## Data included in data folder

<b>totaldf.csv</b> - Data frame from all Steam Game Store scraping<br>
<b>reviewsdf.csv</b> - Cleaned versoin of totaldf, after handling nulls and categorical data<br>
<b>steamspyapi.csv</b> - All information aquired through the SteamSpy api<br>
<b>spyscraped.csv</b> - All data scraped from SteamSpy.com<br>
<b>ownerdf.csv</b> - A merge of steamspyapi.csv onto reviewsdf.csv<br>
<b>nicedf</b> - *likely to be removed/updated* Dataframe of all 3 information sources
