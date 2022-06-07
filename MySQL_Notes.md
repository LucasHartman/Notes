# MySQL_Notes

# version
mysql --version

# Open MySQL in command prompt
mysql.exe -uroot -p

# Create database
CREATE DATABASE [Database_Name];

# Show Databases
SHOW DATABASES;

# Select Database
USE DatabaseName;

# Show all tables
SHOW TABLES;

# Create Table
CREATE TABLE Employees(id int, firstName varchar(255), lastName varchar(255), email varchar(255));

# Insert data 
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...); 
# note: check ‘ ‘

# Show table data
SELECT * FROM database.table;

# Delete Database
DROP DATABASE DBName;

# create user
CREATE USER lucas@'localhost' IDENTIFIED BY 'password';

# grant user all privileges
GRANT ALL PRIVILEGES ON *.* TO 'lucas'@'localhost';

# reload the grant tables to ensure that the new privileges are put into effect
FLUSH PRIVILEGES;

# show all users
SELECT user FROM mysql.user;

# show current user
SELECT user();

# close mysql
exit

# close command-prompt
exit
