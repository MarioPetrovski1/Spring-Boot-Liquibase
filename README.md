# Spring-Boot-Liquibase
Spring Boot integration with Liquibase.


Liquibase is Java based open source tool for managing and versioning database
schema changes.

It supports four different formats:
SQL
XML
YAML
JSON

Liquibase uses table called DATABASECHANGELOG which tracks changes that have or have not been deployed.
It consist of ID,Author,filename,date when it is executed,order of execution,description,comments,tag and deployment id.

It supports many database some of them are :
MySQL
MariaDB
PostgreSQL
Oracle
SQL Server
HSQL
H2

This is a sample spring boot application with liquibase.
I am using MySQL.

1. Clone this repo
2. Change URL,username,password according to your credentials in pom.xml and
application.properties
   
3. If you want to add more migrations just add the files in db/migrations and include them in changelog-master.

For rollback the command is : mvn liquibase:rollback -Dliquibase.rollbackCount=1.

This will rollback 1 change,you can modify it.

And that's it just run the application like any Spring Boot application.

To run it with maven open command line in the project's folder and run this 
command: mvn spring-boot:run

If you want to have a look at the whole blog post you can find it here : https://iwconnect.com/database-versioning-with-spring-boot-and-liquibase/



