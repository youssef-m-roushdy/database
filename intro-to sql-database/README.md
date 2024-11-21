# Itroduction To Database

  * A databse is information that is set up for easy access management and updating
  * It is an organized collection data
  * Generally stored and accessed electronically from a computer system
  * It supports the storage and manipulation of data
  * In other words databases are used by organization as a method of storing and managing and retrieving information
  * To manage these database, Database Management System(DBMS) are used

## Advantages Database Provide

  * Reduced data redundancy
  * Reduced updating errors and increased consistenct
  * Greater data integrity and independence from application programs
  * Improved data access to users through the use of host and query languages
  * Improved data security
  * Reduce data entry storage and retrieval costs

## Key Features of DBMS

  * Data Definition
  * Data Manipulation
  * Data Security
  * Data Integrity
  * Data Backup and Recovery

## Introduction To SQL Server

  * SQL Server is relational database management system(RDBMS) by Microsoft
  * It supports SQL along with additional features known as T-SQL or Transact-SQL
  * Microsoft provides set of tools to manage local or remote SQL Server database such as   SSMS(SQL Server Managent Studio), SQL Server Agent, SQL Server Analysis Service, SQL server Reporting Service SQL Server Integration Service, etc

## Types Of Databases

  * `Relational`
    * Stores information in tables containing specific pieces and types of data
    * This form of data storage is often called structured data, Using structured Query Language(SQL)
    * Relational database usually contains table consisting of columns and rows
  * `Non-Relational`
    * Are often called No SQL databases
    * Data stored in a Non-tebular form
    * Non-Relational databases might be based on data structures like documents
    * A document can be highly detailed while containing a range of different types of information in different formats

## SQL Server Commands 

  * `Data Definition Language(DDL)`
    * Used to create and modify the structure of database objects in database
    * Commands:
      * `CREATE`: Create objects in database
      * `ALTER`: Alters objects in database
      * `DROP`: Deletes objects in database
      * `TRUNCATE`: Deletes all records and resets table intial stage
  * `Data Maniplation Language(DML)`
    * Is reponsible for all form of changes in the database
    * Commands:
      * `INSERT`: Used to insert data into the row table
      * `UPDATE`: Used to update or modify the value of a column in table
      * `DELETE`: Used to remove one or more row from a table
  * `Data Control Language(DCL)`
    * Used to grant and take back auhority from any database user
    * Commands:
      * `Grant`: Used to give user access privileges to a database
      * `Revoke`: Used to take back permission from the user
  * `Transaction Control Language(TCL)`
    * Use to roll back of some commands use with DML commands like INSERT, DELETE, and UPDATE only
    * Commands:
      * `COMMIT`: Used to save all the transactions to the database
      * `ROLLBACK`: Used to undo all transactions that have not already been saved to database
      * `SAVEPOINT`: Used to roll transaction back to certain point without rolling back the entire transaction
  * `Data Query Language(DQL)`
    * Used to fetch data from the database
    * Commands:
      * `SELECT`: Used to select attribute based on the condition described by WHERE 
      
## SQL Server Tables

  * Tables are database objects that contain all the data in a database
  * In table data logically organized in rows and columns
  * Each column represents a field and each row represents a unique record
  * Each column has data type associated with it reprents the type of data in that column
  * Each table is uniquely named in database 
  * Three steps to create Table in databse:
    * Name of the table
    * Name of the fields
    * Definitions for each field

## SQL Server Constraints

  * In database we can add some rules to column known as constraints, These rules control the that can be stored in a column
  * Insert operation will be terminated if inserted data violates the defined constraint
  * They are responsible for ensuring column data accuracy, integrity, and reliability inside table
  * Example if a column has NT NULL constraint it means the column cannot store NULL values
  * SQL Server categorize the consrains into two types
    * Table level constraints:
      * These constraint apply to entire table that limit the types of data that are entered into table
      * Its definitions are specified after creating the table using the ALTER statement
    * Column level constraints
      * These constraints is apply to the single or multiple columns to limit the types of data that can be entered into the column
      * Its definetion is specified while creating the tables
    * Constraint used in SQL Server are
      * `NOT NULL`: Means you must enter value to this field
        * Syntax: `CREATE TABLE table_name( column_name data_type NOT NULL);`
      * `UNIQUE`: The value should not be duplicated 
        * Syntax: `CREATE TABLE table_name( column_name data_type UNIQUE);`
      * `PRIMARY KEY`: Means field should have a unique value and not empty
        * Syntax:
        ```CREATE TABLE table_name(
        column1 data_type,
        ...,
        [CONSTRAINT constraint_name] PRIMARY KEY (column1)
        );```
      * `FOREIGN KEY`: Is key define a relation between two tables has unique value and connot be null and refers to primary key in parent table
        * Syntax:
        ```
        CREATE TABLE table_name (
            column1 data_type,
            column2 data_type,
            ...,
            FOREIGN KEY (column_name)
            REFRENCES referenced_table_name (refrenced_column_name)
        )
        ```
      * `CHECK`: Define limit or range of values in a column
        * Syntax:
        ```
        CREATE TABLE table_name (
            column1 data_type CHECK(condition)
        );
        ```
      * `DEFAULT`: Default value in the column when the user does not specify any value for that column
        * Syntax:
        ```
        CREATE TABLE table_name (
            column1 data_type DEFAULT default_value
        );
        ```

## SQL Server Clauses

  * SQL clauses help us to retrieve a set of records or bundle from the table
  * It help us to specify a condition on the columns or the records of a table
  * A clause is nothing but a built-in function that helps to fetch the required records or tuples from a database table
  * Most of the clauses are conditional clauses where the large amount of data is stored in the database and clauses helps us to filter and analysis the queries as well
  * Clauses Examples
    * WHERE CLAUSE
    * GROUP BY CLAUSE
    * HAVING CLAUSE
    * ORDER BY CLAUSE

## SQL Server Data Types

  * Datatype specifies the type of the data that the object can store, or a column can store. This type can be integer data, string data, date and time, binary strings, etc
  * Assigning an appropriate data type to columns in a table is crucial while designing a database
  * It affects the performance and effeciency of the database and the application using the database
  * SQL Server provides built-in data types for all kind of data that you can store within the SQL Server database
  * Additionally, you can also define your own data type that's a generic type in T-SQL
  * Variable are the object which act as a placeholder to a memory location
  * It hold single data value
  * A variable allows a programmer to store data temporaily during the execution of code
  * Syntax: `DECLARE {@LOCAL_VARIABLE data_type [ = vlaue]}

### Variables Type in SQL Server
 
  * Local Variable
    * A user declares local variable
    * By default local variable starts with `@`
    * Every local variable scope has the restriction to the current batch or procedure within any givin session 
  * Global Variable
    * The system maintains the global variable. A user cannot declare them
    * The global variable starts with `@@`
    * It stores session related information 

## SQL Server Operators

  * The operators are symbols that are used to perform operations with values
  * These operators are used with SQL clauses sech as: `WHERE, SELECT, ON etc`
  * The operators in SQL ca be categorized as:
    * Arithmetic operators: `+, -, *, /, %`
    * Comparison operators: `=, < ,>, <=, >=, <>, !=`
    * Logical operators: `AND and ALL, AND, OR and NOT, BETWEEN, EXISTS, IN, LIKE, IS NULL`