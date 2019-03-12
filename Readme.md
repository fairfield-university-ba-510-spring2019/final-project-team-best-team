# Read Me

#### 1. Designed an ERD [CourseDataERD](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/SourceData/docs/CourseDataERD.pdf)
* Studied the data in *SourceData* repository. Translated all the data from the csv files CourseCatalog2017_2018.csv, CourseCatalog2018_2019.csv, courses.csv, course_meetings.csv into a normalized relational database.   
* Documented the design with an ERD *CourseDataERD.pdf* which illustrates the relationship between the ERD tables as well as the primary keys and foreign keys for each table.   
* Each table of the ERD complies with the Boyce Codd normal form (BCNF)

#### 2. Created data dictionary [CourseDataDictionary](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/SourceData/docs/CourseDataDictionary.md)
* The data dictionary is in alignment with the CourseDataERD.
* It defines all the columns of each table in the ERD.

#### 3. Created an SQLite database [CourseData.db](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/CourseData.db)
* Create a database aligned with the ERD. 
* Populated the import tables with raw source data from the csv files and dropped the tables after the database was created.
* Created the ERD tables and inserted data into it from our database. Assigned a primary keys to each table and implemented FOREIGN KEY constraints. 

#### 4. Created [CourseDataETL](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/CourseDataETL.ipynb) to extract, translate and load data.
* *CourseDataETL* supports the codes to extracting data from the database
* All the SQL DDL and DML code for the database *CourseData.db* as well as for creating and populating the ERD tables is captured in this notebook.

#### 5. Tested the integrity of database in [CourseDataTests](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/CourseDataTests.ipynb)
* Ensured integrity checks for Domain integrity, Entity integrity and Relational integrity.
* Domain integrity: Checked the datatypes for all the columns in each table of the database to ensure there were no truncation or translation errors. 
* Entity integrity: Checked for duplicated records in the tables.
* Relational integrity: Checked if the Foreign Key joins were compatible with the Primary Keys to ensure each relationship is implemented correctly.

#### 6. Created a [Star Schema](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/SourceData/docs/StarSchema.pdf)
* Frames the fact tables and dimesions of the datawarehouse.
* Designed it into to create a star schema to document the fact table and associated dimensions as a separate ERD. 

#### 7. Design and build data warehouse [CourseDataWarehouse.db](link)
* Created a star schema design to frame our dimensions and fact tables. 
* Documented the fact table and associated dimensions as a separate ERD. 
* Populated the fact and dimensions table in *CourseDataWarehouse.db* by extracting data from *CourseData.db*.

#### 8. Tested the integrity of [CourseDataWarehouseTest](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/CourseDataWarehouseTest.ipynb)
* Similar to *CourseDataTests* ensured integrity checks for Domain integrity, Entity integrity and Relational integrity.

#### 9. Demo of the CourseDataWarehouse [CourseDataWarehouse Demo](https://github.com/fairfield-university-ba-510-spring2019/final-project-team-best-team/blob/master/CourseDataWarehouseDemo.ipynb) 
* Created a demo file to test the uselfulness of *CourseDataWarehouse*. 
* Used SQL queries to analyse data from our *CourseDataWarehouse*.
* The queries illustrated how the CourseDataWarehouse can be helpful in providing information related to the courses. 

