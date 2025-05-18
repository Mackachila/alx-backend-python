 Python MySQL Seeder – seed.py
This project sets up and populates a MySQL database named ALX_prodev with user data from a CSV file. It demonstrates the use of Python with MySQL for database setup, schema creation, and data insertion.

Features
Connects to a MySQL server

Creates a database if it doesn't exist

Creates a user_data table with appropriate schema

Loads and inserts data from a CSV file (user_data.csv)

Prevents duplicate entries using primary key checks

Table Structure: user_data
Field	Type	Constraints
user_id	VARCHAR(36)	Primary Key, Indexed
name	VARCHAR	NOT NULL
email	VARCHAR	NOT NULL
age	DECIMAL	NOT NULL

🛠️ Requirements
Python 3.x

MySQL Server (running locally)

mysql-connector-python (Install with pip install mysql-connector-python)

CSV file named user_data.csv with the following headers:
user_id,name,email,age
 Usage
Prepare the environment:

Edit
pip install mysql-connector-python
Make sure your MySQL server is running and accessible with username root and a valid password.

Place your user_data.csv file in the project root directory.

Run the script via the main driver (0-main.py):


./0-main.py
Example output:


connection successful
Table user_data created successfully
Database ALX_prodev is present 
[('0023...', 'Jared Odhiambo', 'achilajared@gmail.com', 30), ...]
🧠 Functions Overview
connect_db(): Connects to MySQL server (not tied to any specific database).

create_database(connection): Creates ALX_prodev database if it does not exist.

connect_to_prodev(): Connects to the ALX_prodev database.

create_table(connection): Creates the user_data table with required columns and constraints.

insert_data(connection, data): Loads data from user_data.csv and inserts only new records.
