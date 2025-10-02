# Data_Analyst_Day_7_Task_7
Seventh Task of Data Analyst  Internship @ Elevate Labs

Steps for this task:

1. Install Required Libraries

psycopg2-binary and sqlalchemy → PostgreSQL connection

pandasql → Run SQL queries on Pandas DataFrames

2. Import Libraries

sqlite3 → For SQLite operations

psycopg2 → Connect to PostgreSQL

pandas → Data manipulation

matplotlib.pyplot → Basic plotting

seaborn → Advanced plotting and line charts

3. Connect to PostgreSQL

Use psycopg2.connect() to connect to the database.

Specify host, database, user, password, and port.

4. Query Data from PostgreSQL

Example: Summarize sales by product (SUM(quantity) and SUM(quantity*price)).

Load results into a Pandas DataFrame using pd.read_sql_query().

Close the database connection.

5. Load CSV Data

Read local CSV file using pd.read_csv().

Preview data with .head().

6. Set up pandasql

Define pysqldf = lambda q: sqldf(q, globals()) to run SQL queries on DataFrames.

Test query: SELECT * FROM car_sales_df.

7. Clean Column Names

Remove spaces, special characters, and parentheses from column names.

Example: car_sales_df.rename(columns=lambda x: x.strip().replace(' ', '_').replace('($)', '').replace(')', ''), inplace=True).

8. Sales Analysis by Company

SQL query: SUM(Price_) grouped by Company.

Plot bar chart of total sales per company.

9. Sales Analysis by Model

SQL query: Summarize SUM(Price_) and COUNT(*) grouped by Model.

Limit top 10 models.

Plot bar charts for total sales and total cars sold per model.

10. Sales Analysis by Transmission

SQL query: SUM(Price_) grouped by Transmission.

Plot pie chart showing sales distribution by transmission type.

11. Sales Analysis by Body Style

SQL query: SUM(Price_) grouped by Body_Style.

Plot pie chart to visualize contribution of each body style.

12. Sales Analysis by Dealer Region

SQL query: SUM(Price_) grouped by Dealer_Region.

Plot pie chart for sales distribution across regions.

13. Prepare Date for Time-Series Analysis

Convert Date column to datetime using pd.to_datetime().

Format datetime as YYYY-MM-DD for SQLite compatibility.

14. Monthly Sales Trend

SQL query: Group by month using strftime('%Y-%m', Date)

Aggregate SUM(price_) and COUNT(*).

Plot line chart using Seaborn for monthly sales trends.

15. Key Concepts

Using SQL queries directly on Pandas DataFrames (pandasql).

Aggregating data (SUM, COUNT) for insights.

Cleaning columns for easier querying.

Visualizing data with bar charts, pie charts, and line charts.

Performing time-series analysis for monthly trends.
