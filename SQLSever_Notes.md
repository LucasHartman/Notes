# SQLSever_Notes

# Version
MSSMS > Object Explorer: (SQL Server 15.0.0.4153)

or 

sqllocaldb v

# List Local Databases
sqllocaldb info

# Create Database
sqllocaldb create MSSQLLocalDB -s

# Delete Database
sqllocaldb delete MSSQLLocalDB

# Connect Server in MSSMS
1. (localdb)\MSQLLocalDB
2. Connect

# MSSMS: Create Database 
1. Database Directory >RMB > New Database

# MSSMS: Create Login
1. Security Directory > RMB > New Login
2. Login name: root
3. SQL Sever authentication
    - set Password: root
    - Enforce password expiration: Disabled
    - User must change password at next login: Disabled
    - Default database: [databaseName]
4. Select a page > User Mapping:
- User mapped to this login: [databaseName]
- Database role membership for: public, db_owner

# Visual Studio Setup
1. Create SQLControl
- Solution Explorer > rmb[projectName] > Add > Class

"Server=(localdb)\MSQLLocalDB"