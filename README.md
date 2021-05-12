# Metis Linear Regression Module
This repository was created as a project for METIS to learn the principles behind web scraping and linear regression. I chose to try and predict the popularity of video games, based on ownership. Data was aquired with a combination of selenium and beautiful soup, through scraping the Steam Game Store and SteamSpy.com, supplemented by data aquired through SteamSpy's API. A combination of StatsModels and Sci-Kit Learn was then used to find the most accurately predictive model, with the lowest error cost.  

## Description of included Jupyter notebooks
This is a working notebook, and is not fully cleaned and organized, at this point, the notebooks should be followed in this order to see workflow from start to finish:
<br>
<br>
steam_scraping - All of the code used to scrape data from Steam Game Store, and transform it into a data frame. The final data frame from this is saved in the data folder as totaldf.csv<br>
final_df_editing - EDA and cleaning on data scraped from Steam Game Store. Final result saved as reviewsdf.csv<br>
steamspy_api_scraping - The code used to aquire information from SteamSpy's API. This was done before scraping SteamSpy, to see if the data would provide meaningful features to improve the linear regression model. The data provided from the API is more general than on the actual site, so this was a preliminary step.<br>
steamspy_scraping - The code used to scrape more exact data from SteamSpy's actual website. <br>
merging_modeling - *likely to be removed* preliminary merging of all data sources, and base-line modeling.<br>
target_transformations - The target (owners) was unevenly distributted, this notebook shows different transformations on the target variable, without feature selection or engineering, to see which transformation would be the best to move forward with. Models were scored using r^2, mean absolute error, and root mean squared error.



## data included in data folder

gamesdf1 - list of games, and their page links,  from scraping the list from steam's site<br>
games_joined - final concat list of all scraped pages<br>
totaldf - gamesdf1 and games_joined into to final df with all desierd features<br>
prelimdf - totaldf filtered to only inlcude rows that have total reviews, and only include numerical features, to create a base model for MVP<br>
reviewsdf - dataframe of just games with total reviews listed, including columns for rating value and top 10 publisher list<br>
prelimdf2 - second preliminary dataframe. upadted rating to numeric value, included year released.<br>
prelimdf3 - updated prelimdf2 to include number of languages offered in and first run at dummy variables (publisher, broken down by top 10 and other)<br>
finaldf - final dataframe of all data after dummifying<br>
modlingdf - final usable df used for all modeling

