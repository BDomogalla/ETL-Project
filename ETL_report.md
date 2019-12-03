Extract: your original data sources and how the data was formatted (CSV, JSON, pgAdmin 4, etc).
We found a craft beers dataset from Kaggle that includes a list of 2,410 US craft beers and 510 craft breweries. The dataset was collected in January 2017 from CraftCans.com. The dataset includes 2 CVSs: one that contains information about all the beers and one that contains information on all the breweries. These datasets are linked be brewery ID. We wanted to supplement this dataset, so we scraped data from brewersassociation.org that has data on the state level about production, consumption and sales for each state. We were able to merge this with our brewery level dataset on the common column of state.

Transform: what data cleaning or transformation was required.
We combined the data from Kaggle and made a DataFrame based on the data we scraped and loaded all of that into a SQL database: brew.sqlite. The datasets were well structured and very clean, so we only needed to filter out columns that we were not going to use. In the original craft breweries dataset from Kaggle, the states are listed as their two letter abbreviations and the data we scraped had the full state name, so we had to convert all abbreviations to full state names to get our final tables. After loading our data into SQL, we did some summary statistics at the state level including brewery count, beer count, beer style count, average ABV and average IBU. 

Load: the final database, tables/collections, and why this was chosen.
We loaded it into a SQL database, and we used SQLite because it was fast, easy and simple to do in the same notebook as all the other work. The SQLite file is under Resources/brew.sqlite. We also chose to use SQLite because anyone can run the notebook without having to change the Postgres login information or uploading login credentials to GitHub. The final table gives a state level overview of beers focusing on production in terms of quantities, types, sales and number of breweries. 



