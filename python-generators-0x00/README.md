# MySQL Database Script: README

This project contains a Python script to manage a MySQL database, create tables, and insert data from a CSV file. The script is designed to set up and manage a database named **`ALX_prodev`** and a table **`user_data`**, with functionality for data insertion and table creation.

---

## Features

- **Database Connection**: Establishes a connection to the MySQL server and creates a database if it doesn't exist.
- **Table Creation**: Creates a table `user_data` with columns for user details such as ID, name, email, and age.
- **CSV Data Insertion**: Reads data from a CSV file and inserts it into the database, ensuring no duplicate email entries.
- **Error Handling**: Handles exceptions such as database connection errors, file not found, and SQL errors.

---

## Prerequisites

1. **MySQL Server** installed and running on your machine.
2. **Python 3.x** installed.
3. The `mysql-connector-python` module installed. Use the following command to install:
   ```bash
   pip install mysql-connector-python
   ```
4. A CSV file containing the user data with columns:
   - `name`
   - `email`
   - `age`

---

## Usage

### 1. Configure the Script

- Update the database credentials in the script:
  ```python
  host="localhost",
  user="your_mysql_username",
  password="your_mysql_password"
  ```
  Replace `your_mysql_username` and `your_mysql_password` with your MySQL username and password.

### 2. Run the Script

1. Connect to the MySQL server:
   - The `connect_db()` function establishes a connection to the server.
   - The `create_database()` function creates the `ALX_prodev` database if it doesn't exist.

2. Connect to the `ALX_prodev` database:
   - The `connect_to_prodev()` function connects to the `ALX_prodev` database.

3. Create the `user_data` table:
   - The `create_table()` function ensures the table is created if it doesn’t exist.

4. Insert data into the table:
   - The `insert_data(connection, csv_file)` function reads a CSV file and populates the `user_data` table.

### 3. Command-Line Execution

Save the script as `manage_database.py`, then run it with the following steps:

- Set up the database:
  ```bash
  python manage_database.py
  ```

- Use the function `insert_data()` to provide the path to your CSV file:
  ```python
  insert_data(connection, "path/to/your/user_data.csv")
  ```

---

## CSV Format Example

The CSV file should follow this structure:

| name       | email             | age |
|------------|-------------------|-----|
| John Doe   | john.doe@test.com | 30  |
| Jane Smith | jane.smith@test.com | 25  |

---

## Functions Overview

1. **`connect_db()`**
   - Connects to the MySQL server.
   - Returns a connection object.

2. **`create_database(connection)`**
   - Creates the `ALX_prodev` database if it doesn't exist.

3. **`connect_to_prodev()`**
   - Connects to the `ALX_prodev` database.
   - Returns a connection object.

4. **`create_table(connection)`**
   - Creates the `user_data` table.

5. **`insert_data(connection, csv_file)`**
   - Inserts data into the `user_data` table from a CSV file.

---

## License

This script is open-source and can be modified or redistributed under the terms of the MIT license.

---

Feel free to enhance this script to suit your project needs! 🚀