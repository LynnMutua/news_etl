This code defines a Python-based ETL (Extract, Transform, Load) pipeline that automates news data collection. It fetches popular news articles about Apple, cleans the structure, and stores them in a PostgreSQL database.
Extract- Uses the requests library to fetch JSON data from the NewsAPI everything endpoint, searching for articles containing "Apple" filtered by popularity.

Transform - Converts the raw article list into a Pandas DataFrame. It cleans the dataset by removing the complex source object column and the urlToImage string column.

Load - Connects to a PostgreSQL database using SQLAlchemy and the psycopg2 driver to overwrite or create a table named articles_main with the new data.Orchestration: The main() function executes the functions in sequence and prints a success message upon completion. 

Environment File (.env)This pipeline relies on a .env file in the root directory to securely manage API keys and database credentials.
# news_etl

