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

## SQL Server Predicates

  * A predicate is a condition or expression that determines which row of data should be included or excluded from a query result
  * They are used in WHERE clause to filter data based on specific criteria
  * The Transact-SQL language supports the following predicates:
    * In operator
    * Exists function
    * Between operator
    * Like Operator
    * All and any operator

# SQL Server Joins

  * Joins are used to combine rows from two or more tables from based on related column between them
  * Joins are essential for retrieving data that is distributed across multiple tables
  * They allow us to establish relationship between tables
  
### Types Of Joins In SQL

  * Inner Join
    * `INNER JOIN` Keyword selects all rows from both the tables as long as the condition is satisfied
    * This Keyword will create the result-set by combining all rows from both the tables where the condition satisfies value of the common field will be the same
    * Syntax:
    ```
    SELECT table1.column1, table1.column2, table2.coulmn1,.....
    FROM table1
    INNER JOIN table2
    ON table1.matching_column = table2.matching_column;
    ```
  * Self Join
    * As the name signifies in SELF JOIN a table is joined to itself
    * That is each row of the table is joined with itself and all other rows depending on some conditions
    * Syntax
    ```
    SELECT a.column1, b.column2
    FROM table_name a, table_name b
    WHERE some_condition
  * Outer Join
    * Left Outer Join
      * This join returns all the rows of the table on the left side of the join and matches rows for the table on the right side of the join
      * For the rows for which there is no matching row the right side, the result-set will contain null
      * Syntax
      ```
      SELECT table1.column1, table1.column2, table2.coulmn1,....
      FROM table1 LEFT OUTER JOIN table2
      ON table1.matching_column = table2.matching_column;
      ```
    * Right Outer Join
      * This join returns all the rows of the table on the right side of the join and matches rows for the table on the right side of the join
      * For the rows for which there is no matching row the left side, the result-set will contain null
      * Syntax
      ```
      SELECT table1.column1, table1.column2, table2.coulmn1,....
      FROM table1 RIGHT OUTER JOIN table2
      ON table1.matching_column = table2.matching_column;
      ```
    * Full Outer Join
      * Creates the result-set by combining results of both LEFT JOIN and RIGHT JOIN
      * The result-set will contain all the rows from both tables
      * For the rows for which there is no matching the result-set will contain NULL values
      * Syntax
      ```
      SELECT table1.column1, table1.column2, table2.coulmn1,....
      FROM table1 LEFT OUTER JOIN table2
      ON table1.matching_column = table2.matching_column
      UNION
      SELECT table1.column1, table1.column2, table2.coulmn1,....
      FROM table1 RIGHT OUTER JOIN table2
      ON table1.matching_column = table2.matching_column;
      ```
  * Cross Join
    * The CROSS JOIN is also known as CARTESIAN JOIN
    * In a CARTESIAN JOIN there is a join for each row of one table to every row of another table
    * This usually happens when the matching column or WHERE condition is not specified
    * Syntax
    ```
    SELECT table1.column1, table1.column2, table2.coulmn1,....
    FROM table1
    CROSS JOIN table2
    ```

## SQL Server Views

  * A view is a database object that has no value
  * It is virtual table which created according to the result set of an SQL query
  * However, it looks similar to an actual table containing rows and columns
  * Therefore we can say that its contents are based on the base table
  * It is operated similary to the base table but does not contain any data of its own
  * Its name is always unique like tables
  * Views differ from tables as they are definitions that are created on top of other tables
  * If any changes occur int the underlying table, the same changes reflected in the views also
  * Syntax
  ```
  SELECT column1, column2, ....
  FROM table1, table2, table3
  WHERE...
  ```

### Uses Of Views

  * To restrict data access
  * To implement the security access
  * To provide data independence
  * To present different views of the same data

## Types Of Views

  * System Defined View
    * System-defined vies are predefined and existing views stored in SQL server
    * Such as Tempdb, Master, and temp
    * Each system views has its properties and functions
    * They can automatically attach to the user-defined databases
    * System Defined View
      * Information Schema View
        * Are used to display information from DB like tables and columns
        * This type of view start with INFORMATION_SCHEMA
        * Example: `SELECT * FROM INFORMATION_SCHEMA`
      * Catalog View
        * Set of system views that provide metadata about the database objects and server configration
        * This views are part of sys schema and contain information about structure organization, and properties of data and its objects
        * Example: `SELECT * FROM SYS.TABLES`
      * Dynamic Management View
        * Are special types of views that expose internal information and statics about the SQL Server instance
        * DMVs are for monitoring and troubleshooting purposes
        * It provides a real-time insights into the performance resouces usage and internal state of the database engine
        * Example: 
        ```
        SELECT Connection_id, sesssion_id, client_net_address
        FROM SYS.DM_EXEC_CONNECTIONS
        ```
        * Two types of DMVs:
          * Server-scoped Dynamic Management View
            * Stored in master database
          * Database-scoped Dynamic Management View
            * Stored in Each Database
  * User Defined Views
    * User defines these views to meet their specific requirements
    * It can also divide into two types one is the simple view and another is the complex view
    * The simple view is based on the single base table along with using any complex queries
    * The complex view is based on more than one table along with group by caluse order by clause and join conditions

## SQL Server Indexes

  * SQL Indexes are used in relational databases to retrieve data quickly
  * They are similar to indexes at the end of the books whose purpose is quickly finding a topic
  * SQL provides `Create Index, Alter Index, and Drop Index` commands used to create a new index update an existing one and delete an index
  * A SQL Server Index is used on databse table for faster data access
  * An index is mostly created on one or more columns which are commonly used in SELECT clause and WHERE clause

### Types Of Indexes In SQL Server

  * Clustered Indexes
    * The clustered index defines the order in which the table data will be sorted and stored
    * When defined clustred index on a column it will sort data based on column values and store it, Thus helps in faster retrieval of data
    * There can be one clustered index on a table beacuase the data rows can be stored in only one order
    * When you create Primary Key constraint on a table a unique clastred index is automatically created on the table
  * Non-Clustered Indexes
    * The structure of non-clustred indexes is similar to the clustred index except that the actual data is not contained in the leaf nodes
    * A non-clustered index has non-clustred index key values and each key-value entry contains a refrence to the actual data
    * Depending on how the table data is stored it could point to a data value in the clustred index or a heap structure
    * If row locator is a pointer to the row it is a heap structure
    * If row located in clustered index key it is claustred table

## Stored Procedures

  * A stored prodcedure in SQL is a group of SQL statements that are stored together in a database
  * based on the statements in the prodcedure and the parameters you pass it can perform one or multiple DML operations on the database and return value if any
  * It allow you to pass the same statements multiple times, thereby, enabling reusability
  * The SQL Database server stores the stored procedures as named objects
  * Syntax
  ```
  CREATE PROCEDURE prodcedure_name
  As
  sql_statement
  GO;
  ```

### Benefits of Stored Procedures

  * Reusable
  * Easy to modify
  * Securiy
  * Low Network traffic
  * Increases objects

### Types of Stored  Procedure

  * System-Defined Procedures
    * In stored procedures are already defined in SQL Server
    * These are phsically stored in hidden SQL Server Resource Database and logically apear in
    the sys schema of each user-defined and system-defined database
    * This prodedure starts with `sp_prefix`
    * Some of system defined procedure
      * `sp_rename`: It is used to rename a database object like stored procedure, views, table
      * `sp_changeowner`: It is used to change owner of database object
      * `sp_help`: It provides details on any database object
      * `sp_helpdb`: It provides the details of the databases defined in SQL Server
      * `sp_helptext`: It provides the text of stored procedure reside in SQL Server
  * User-Defined Stored Procedures
    * They are precompiled database objects that contain SQL statement and procedural logic
    * They are created by users to encapsulate and execute a sequence operations in the database
    * To create a user-defined stored procedures in SQL Server you use `CREATE PROCEDURE`
    statement
    ```
    CREATE PROCEDURE [ProdcedureName]
      @param1 datatype,
      @param2 datatype
    AS
    BEGIN
    -- procedure logic go here
    -- SQL statements, control structures, variable
    END;
    ```
    * We can create a stored procedure with `SELECT`, `INSERT`, `UPDATE`, and `DELETE` SQL
    statements

## SQL Server Functions

  * Function in SQL Server are similar to functions in other programming languages
  * They contains SQL statements that perform some specific task
  * Function can have a input parameter and must return a single value or multiple records

## Types Of Functions

  * System-Defined Function
    * These functions are defined by SQL Server for different purposes
    * The functions that are defined by the system are known as "system defined functions"
    * Usage of the built-n functions saves much development time while performing certain tasks
    * These function work with SQL select statement to calculate values and manipulated data
    * System Functions:
      * Scalar Functions
        * Operate on a single value and return a single value
        * Below is the is the list of some usefull SQL Scalar functions 
          * `abs(-10.49)`: Return the absolute number of the given number => 10.49
          * `rand(10)`: Generate random number of 10 characters
          * `round(1723,76313, 2)`: Round the given number to 2 places => 1723,76
          * `upper('course')`: Return the uppercase of given string 'COURSE'
          * `lower('COURSE')`: Return The lower case of given string 'course'
          * `Itrim(' course')`: Remove the spaces from the left-hand side of the string => 'course'
          * `convert(int, 25.75)`: Convert given number float value to integer => 25
      * Aggregate Functions
        * `max()`: Returns maximum value from collection of value
        * `min()`: Returns minimum value from collection of value
        * `avg()`: Returns average value from collection of value
        * `count()`: Returns number of items from the collection
  * User-Defined Function
    * Functions are created by the user
    * These functions may accept required parameters and return the processed data
    * This functions help us to simplify the overall database development
    * As it encapsulates the complex buisness logic and making it available for reuse whenever any similar functionality is required
    * The user-defined functions hold the code that is needed to query data a lot easier to write
    * It also improves query readability, accessability, and functionality as well as allows other developers to replicate the same procedures accordingly

### User-Defined Scalar Functions

  * Scalar function always accepts parameters, either single or multiple and returns a single value
  * The scalar functions are useful in simplification of our code 
  * Suppose we might have a complex computation that appears in a number of queries
  * In such case we can we can build a scalar function that encapsulates the formula and uses it in each query instead of in each query
  * Syntax
  ```
  CREATE FUNCTION schema_name.function_name(parameter_list)
  RETURNS data_type AS
  BEGIN
      statements
      RETURN value
  END;
  ```

### SQL Server Table Valued Functions

  * Inline Table Valued Function
    * This UDF function return a table variable based on the action performed by the function
    * A single SELECT statement should be used to determine the value of table variable
    * The below example will create a table-values functions and retrieve the data of employee table:
    ```
    -- It creates a table-values function to get employees
    CREATE FUNCTION fudf_GetEmployee()
    RETURN TABLE
    AS
    RETURN (SELECT * FROM Employees)
    ```
  * Multi-Statement Table Valued Function
    * This UDF function returns a table variable based on the action performed by the function 
    * It can contain single or multiple statements produce the result
    * And it is also a function that returns the result of multiple statements in a tabular
    * It is useful becasue we can execute multiple statements in this function and get aggregated results into the returned table
    * We can define this function by using a table variable as a return value
    * Inside the function we execute multiple queries and insert data into this table variable
    * The following example creates a function name `MULTIVALUED` that returns the `@Employee` table
    * Statement
    ```
    CREATE FUNCTION MULTIVALUED()
    RETURNS @Employee TABLE
    (
      id INT,
      emp_name VARCHAR(50),
      salary INT
    )
    AS
    BEGIN
      INSERT INTO @Employee
      SELECT E.id, E.emp_name, E.salary FROM E;
      UPDATE @Employee SET emp_name = 'Greame smith' WHERE id = 3;
      RETURN
    END
    ```

## SQL Server Triggers

  * A trigger is set of SQL statements that reside in system memory with unique names
  * A trigger is called a special procedure becasue it can not be called directly like a stored procedure
  * The distiniction between trigger and procedure is that:
    * A trigger is called automatically when a data modification event occurs agnaist a table
    * Whereas a stored procedure must be invoked directly
  * Each trigger is always associated with a table
  * Syntax:
  ```
  CREATE TRIGGER schema.trigger_name
  ON table_name
  AFTER {INSERT, UPDATE, DELETE}
  [NOT FOR REPLICATON]
  AS
  {SQL Statements}
  ```
  * Triggers are hellpfull to execute some events automatically on certain desirable scenarios

### Types of SQL Triggers

  * Data Definition Language(DDL) Triggers
    * Fired in response to DDL events such as `CREATE`, `ALTER`, and `DROP` statements
    * We can create these triggers at database level server depending on type of DDL events
    * It can also be executed in response to certain system-defined stored procedures that 
    do DDL-like operations
    * Syntax
    ```
    CREATE TRIGGER trigger_name
    ON {DATABASE | ALL SERVER}
    [WITH ddl_trigger_option]
    FOR {event_typr | event_group}
    AS
    {sql_statements}
    ```
    * Useful in following scenario:
      * Prevent the database scheme from changing
      * Audit changes made in the database schema
      * Respond to change made in the database schema
  * Data Manipulation Language (DML) Triggers
    * Fired in a response to DML events like `INSER`, `UPDATE`, and `DELETE` statements in user's table or view
    * It can also be executed in response to DML-like operations by system-defined stored    procedures 
    * Syntax
    ```
    CREATE TRIGGER [schema_name.]trigger_name
    ON {table_name | view_name}
    {FOR | AFTER | INSTEAD OF} {[INSERT], [UPDATE], [DELETE]}
    [NOT FOR REPLICATON]
    AS
    {sql_statements}
    ```
    * DML Triggers can be:
      * After Triggers
        * Fires when SQL Server completes the the triggering action successfully, that fired it
        * This trigger is executed when a table completes an insert, update, or delete operation
        * It is not supported in views
        * Classify After trigger to:
          * AFTER INSERT trigger
          * AFTER UPDATE trigger
          * AFTER DELETE trigger
        * Syntax
        ```
        CREATE TRIGGER schema_name.trigger_name
        ON table_name
        AFTER {INSERT, UPDATE, DELETE}
        [NOT FOR REPLICATON]
        AS
        BEGIN
          -- Trigger statements
          -- Insert, Updatem or Delete statements
        END;
        ```
        * Instead Of Trigger
          * Instead of trigger fires before SQL Server begins to execute triggering operation that triggered
          * It means that no condition constaint check is needed before the trigger runs
          * As a result even if the constraint check fails this trigger will fire
          * It is opposite of the `AFTER TRIGGER`
          * Classify Instead of trigger to:
            * INSTEAD OF INSERT trigger
            * INSTEAD OF UPDATE trigger
            * INSTEAD OF DELETE trigger
          * Syntax
          ```
          CREATE TRIGGER schema_name.trigger_name
          ON table_name
          INSTEAD OF {INSERT, UPDATE, DELETE}
          [NOT FOR REPLICATON]
          AS
          BEGIN
            -- Trigger statements
            -- Insert, Updatem or Delete statements
          END;
          ```
  * Logon Triggers
    * Fires in response to a LOGON event
    * The LOGON event occurs when a user session is generated with an SQL Server instance
    * Which is made after authentication of logging is completed but beffore stablishing
    a user session
    * As result the SQL Server error log will display all messages created by the trigger
    * Icluding error messages and the PRINT statement messages
    * If authentication fails logon triggers do not execute