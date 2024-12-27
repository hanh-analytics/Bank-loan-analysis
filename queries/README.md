# SQL Queries for Business Analytics Project

This project uses **SQLite** as the database management system. Please note that some SQL syntax or features may differ slightly if you are using other systems like **MySQL** or **PostgreSQL**. For example:

- SQLite uses **AUTOINCREMENT** for auto-incrementing columns, while MySQL uses **AUTO_INCREMENT**.
- The data types in SQLite are more flexible, so be sure to adjust if you're using MySQL (e.g., SQLite uses `TEXT` for strings, while MySQL might use `VARCHAR`).

- **/queries/sqlite/**: Contains SQL queries optimized for SQLite.

## Purpose of the Queries

The queries in this folder are used for:
- **Data retrieval**: Selecting, filtering, and aggregating data from the database.
- **Data transformation**: Joining tables, grouping data, and performing other data manipulation tasks.
- **Analytics**: Performing basic analysis to gain insights into the dataset (e.g., calculating loan approval rates, customer demographics, etc.).

## Instructions

### SQLite Users
If you're using SQLite, navigate to the `/queries/sqlite/` folder. The SQL queries in this folder are tailored for SQLite's syntax and features, such as `AUTOINCREMENT` for auto-incrementing fields.

To set up the database:
1. Make sure you have SQLite installed.
2. Run the SQL queries in the `/queries/sqlite/` folder to create tables, insert data, and perform analysis.


## How to Use the Queries
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/hanh-analytics/Bank-loan-analysis
2. Navigate to the queries folder based on your platform:
```bash
cd business-analytics-project/queries/sqlite or /mysql, /postgresql
```
3. Execute the SQL queries in the appropriate database system using your preferred client or IDE
# Important Notes:
- Make sure you adjust the SQL syntax based on the platform you're using. Some functions and data types may vary between _SQLite, MySQL, and PostgreSQL, or any other SQL syntax_.
- Always review the queries before executing them to ensure compatibility with your database setup.



