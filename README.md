# Movies-ETL
## Background
Amazing Prime loves the dataset and wants to keep it updated on a daily basis. Britta needs your help to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. You’ll need to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.
## Overview of Project
Wikipedia has a ton of information about movies, including budgets and box office returns, cast and crew, production and distribution, and so much more. Luckily, one of Britta's coworkers created a script to go through a list of movies on Wikipedia from 1990 to 2018 and extract the data from the sidebar into a JSON. Unfortunately, her coworker can't find the script anymore and just has the JSON file. We'll need to load in the JSON file into a Pandas DataFrame.
## Project Deliverables
- Deliverable 1: Write an ETL Function to Read Three Data Files
- Deliverable 2: Extract and Transform the Wikipedia Data
- Deliverable 3: Extract and Transform the Kaggle Data
- Deliverable 4: Create the Movie Database
- Deliverable 5: A written report on the Movie Database analysis README.md.
## Resources and Before Start Notes:
- Data Source: ETL Deliverable 1, ETL Deliverable 2 and ETL Deliverable 3
- Data Tools: PostgreSQL, pgAdmin
## Deliverable 1: Write an ETL Function to Read Three Data Files
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, write a function that reads in the three data files and creates three separate DataFrames.

- An ETL function is written to read in the three data files.
- The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
- The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
- The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.

## Deliverable 2: Extract and Transform the Wikipedia Data
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.

- The TV shows are filtered out, and the wiki_movies_df DataFrame is created.
- A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
- The extraction and transformation of the Wikipedia data in the ETL function does the following:
- A list comprehension is used to keep columns with non-null values.
- The non-null box office data is converted to string values using the lambda and join functions.
- A regular expression is used to match the six elements of "form_one" of the box office data.
- A regular expression is used to match the three elements of "form_two" of the box office data.
- The following columns are cleaned in the Wikipedia DataFrame:
- The box office column
- The budget column
- The release date column
- The running time column​
- The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file.
## Deliverable 3: Extract and Transform the Kaggle Data
Deliverable Requirements:
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, you’ll merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, you’ll merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

- The extraction and transformation of the Kaggle metadata using the ETL function does the following:
- The Kaggle metadata is cleaned.
- The Wikipedia and Kaggle DataFrames are merged.
- The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df:
Unnecessary columns are dropped.
- A function is used to fill in the missing Kaggle data.
- The movies_df DataFrame is filtered to keep specific columns.
- The movies_df DataFrame columns are renamed.
- The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
- The ratings counts are cleaned.
- The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame.
- The empty values in the movies_with_ratings_df DataFrame are filled with “0”.
- The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file
