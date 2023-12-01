SQLite3 Database Utility Functions
=====================================

A set of Python functions to interact with SQLite3 databases. These
functions cover various database operations, including table
manipulation, data insertion, selection, update, and deletion.

Function Definitions
--------------------
from sqlite3utils import list_tables 

database_url = "mydatabase.db"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Returns a database_url which needs to pass for all the further functions

``list_tables(database_url)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Returns a list of tables in the specified SQLite3 database.

``create_table(database_url, table_name, columns)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Creates a new table in the database with the given name and columns.

``insert(database_url, table_name, data)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Inserts a single row of data into the specified table.

``insert_many(database_url, table_name, data_list)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Inserts multiple rows of data into the specified table.

``select_all(database_url, table_name)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Selects all rows from the specified table.

``select_with_pagination(database_url, table_name, from_index, to_index)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Selects a range of rows from the specified table with pagination.

``select_by_column(database_url, table_name, column_name, column_value)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Selects rows from the specified table where a specific column matches a
given value.

``select(database_url, table_name, where_dict)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Selects rows from the specified table based on the provided conditions.

``update(database_url, table_name, update_dict, where_dict)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Updates rows in the specified table based on the provided conditions
with new values.

``delete(database_url, table_name, where_dict)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Deletes rows from the specified table based on the provided conditions.

``truncate(database_url, table_name)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Truncates (removes all rows from) the specified table.

``delete_table(database_url, table_name)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Deletes the specified table from the database.

``sql_query(database_url, raw_sql_query)``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Executes a raw SQL query on the specified database and returns the
result.

Example Usage
-------------

Below are examples illustrating the usage of some functions. Note that
you need to replace the placeholder values with your actual database
details.

\```python # Example usage of get_database_url database_url =
get_database_url(“localhost”, “5432”, “test”, “root”, “password”)

Example Usage of list_tables
============================

list_of_tables = list_tables(database_url) print(“List of Tables:”,
list_of_tables)

Example Usage of create_table
=============================

create_table(database_url, “new_table”, [“column1 INT”, “column2
VARCHAR(50)”])

Example Usage of insert
=======================

insert(database_url, “existing_table”, {“column1”: 123, “column2”:
“example_data”})

Example Usage of insert_many
============================

data_to_insert_many = [ {“column1”: 456, “column2”: “more_data”},
{“column1”: 789, “column2”: “additional_data”}]
insert_many(database_url, “existing_table”, data_to_insert_many)

Example Usage of select_all
===========================

all_rows = select_all(database_url, “existing_table”) print(“All Rows:”,
all_rows)

Example Usage of select_with_pagination
=======================================

selected_rows = select_with_pagination(database_url, “existing_table”,
1, 5) print(“Selected Rows:”, selected_rows)

Example Usage of select_by_column
=================================

selected_rows_by_column = select_by_column(database_url,
“existing_table”, “column1”, 456) print(“Selected Rows by Column:”,
selected_rows_by_column)

Example Usage of select
=======================

conditions = {“column1”: 123} selected_rows_with_conditions =
select(database_url, “existing_table”, conditions) print(“Selected Rows
with Conditions:”, selected_rows_with_conditions)

Example Usage of update
=======================

update_conditions = {“column1”: 123} update_values = {“column2”:
“updated_data”} update(database_url, “existing_table”, update_values,
update_conditions)

Example Usage of delete
=======================

delete_conditions = {“column1”: 123} delete(database_url,
“existing_table”, delete_conditions)

Example Usage of truncate
=========================

truncate(database_url, “existing_table”)

Example Usage of delete_table
=============================

delete_table(database_url, “existing_table”)

Example Usage of sql_query
==========================

raw_sql_query = “SELECT \* FROM example_table WHERE age > 25” result =
sql_query(database_url, raw_sql_query) print(result)