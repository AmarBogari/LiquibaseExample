# POC for Maintain Database versions using Liqubase :

## Requirements

1. Java - 1.8.x

2. Gradle - 6.2.x

## Steps to Setup

**1. Clone the application**

```bash
git clone https://github.com/AmarBogari/LiquibaseExample.git
```

**2. Run the Application**
```bash
It supported two databases 1) H2 (default) (2) Postgressql.
When run the application its going create database with springbootdb and userschema schema and run all changeset querries from xml files.

Changes required H2 to Postgressql:
1) comment h2 related properties in application.properties and enable postgressql related sqls.
2) comment h2 dependency in build.gradle and enable postgressql dependency.
3) Required to create springbootdb database in postgressql.
```

```bash
This poc covered  following points : 

1) Liquibase mulitple database (H2 and Postgressql)
2) Create Direct sql querries. (00-changelog.xml have created schema.)
3) Created different tables with different columns with different datatypes.
4) Added primary key and ForeignKeyConstraint.
5) rename table.
6) add column.
7) dropColumn.
8) preConditions with no columnexist then its going to create column.
9) preConditions with no table exist then its going to create table.
10) Insert records.

```
