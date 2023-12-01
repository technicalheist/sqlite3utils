# SQLite3Utils

A comprehensive SQLite3 utility package simplifying database interactions. Perform CRUD operations effortlessly and manage tables with ease. Enhance your Python projects with seamless SQLite3 integration using our collection of convenient functions

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
- [Contributing](#contributing)
- [License](#license)

## Installation

## SQLite3 Installation 
SQLite comes bundled with most programming languages, and you can interact with it using libraries specific to the language you're using. However, if you want to use the `sqlite3` command-line tool, you might need to install it separately.

Here are instructions for common operating systems:

### For Linux (Ubuntu/Debian):
```bash
sudo apt-get update
sudo apt-get install sqlite3
```

### For macOS (using Homebrew):
```bash
brew install sqlite3
```

### For Windows:
1. Download the SQLite tools from the SQLite website: https://www.sqlite.org/download.html
2. Choose the appropriate precompiled binaries for Windows.
3. Extract the downloaded ZIP file and add the path to the `sqlite3.exe` executable to your system's PATH environment variable.

After installation, you can test it by opening a command prompt or terminal and typing `sqlite3`. If installed successfully, it should open the SQLite command-line shell.

Remember that if you are using SQLite in a specific programming language like Python, you usually don't need to install SQLite separately, as it is often included with the language's standard library or easily installable using a package manager specific to that language (e.g., `sqlite3` module for Python).

1. Clone the repository:

    ```bash
    pip install sqlite3utils
    ```

2. Navigate to the project directory:

    ```bash
    from sqlite3utils import list_tables ...
    ``

3. Create app.py and set up your SQLite database:

    ```bash
    from sqlite3utils import list_tables
    database = "mydb.db"
    print(list_tables(database))
    ```


## Usage

Explain how to use your project or provide examples.

```bash
python app.py
```

## Functions

List of functions available with brief descriptions:

```python

def list_tables(database_url):
    """List all tables in the SQLite database."""
    # Implementation

def create_table(database_url, table_name, columns):
    """Create a new table in the SQLite database."""
    # Implementation

def insert(database_url, table_name, data):
    """Insert a single record into the specified table."""
    # Implementation

def insert_many(database_url, table_name, data_list):
    """Insert multiple records into the specified table."""
    # Implementation

def select_all(database_url, table_name):
    """Retrieve all records from the specified table."""
    # Implementation

def select_with_pagination(database_url, table_name, from_index, to_index):
    """Retrieve records from the specified table with pagination."""
    # Implementation

def select_by_column(database_url, table_name, column_name, column_value):
    """Retrieve records from the specified table based on a column value."""
    # Implementation

def select(database_url, table_name, where_dict):
    """Retrieve records from the specified table based on conditions."""
    # Implementation

def update(database_url, table_name, update_dict, where_dict):
    """Update records in the specified table based on conditions."""
    # Implementation

def delete(database_url, table_name, where_dict):
    """Delete records from the specified table based on conditions."""
    # Implementation

def truncate(database_url, table_name):
    """Remove all records from the specified table without deleting the table."""
    # Implementation

def delete_table(database_url, table_name):
    """Delete the specified table from the database."""
    # Implementation

def sql_query(database_url, raw_sql_query):
    """Execute a raw SQL query on the database."""
    # Implementation
```

### Example Usage

Provide a simple example or usage of each function.

```python
# Example usage of create_table function
create_table("my_database.db", "employees", ["id INTEGER", "name TEXT", "salary REAL"])
```

## Contributing

If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Make your changes and commit them: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature/new-feature`.
5. Submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
```

