# ETL-Project
What data sources are you using?

https://www.kaggle.com/nickhould/craft-cans#beers.csv  (craft beer data at the beer and brewery level)

  
Scrape data from:

https://www.brewersassociation.org/statistics-and-data/state-craft-beer-stats/  (To get more state level data)




What’s the end product you want to create?


End product would be a searchable, filterable database containing detailed info on both the beers themselves and their brewery/ state sales figures


How will you store it?


We will store the data in postgres as multiple tables corresponding to the beers, breweries and state level beer statistics


How will you transform the data?


We will aggregate individual beer data to the brewery level and then merge the brewery data with state level statisics.


What additional challenges will you give yourself if you have time?


Some data analysis and visualization and Flask app to display state level data

