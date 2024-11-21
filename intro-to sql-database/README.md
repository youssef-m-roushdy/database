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