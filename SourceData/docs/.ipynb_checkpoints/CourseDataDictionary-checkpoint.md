# Data Dictionary
## Catalog_Program

* Catalog_ID (PK): Surrogate Key <br>
* Program_Code: Code of the Program name <br>
* Program_Name: Program or department name <br>
* Course_Title: Name of the course <br>

## Catalog_Course

* CC_ID (PK): Surrogate Key <br>
* Course_Title: Name of the course <br>
* Catalog_ID (FK): Foreign key referencing Catalog_Program table <br>
* Pre_Reqs: Prerequisite for the course <br>
* Co_Reqs: Corequisite for the course <br>

## Course_Offering

* CO_ID (PK): Surrogate Key <br>
* CRN: Course Reference Number <br>
* Section: Section of the course <br>
* Course_Title (FK): Foreign key referencing Catalog_Courses table <br>
* Credits: Number of credits for the course <br>

## Course_Meeting

* CM_ID: Surrogate Key <br>
* CRN: Course Reference Number <br>
* Section(FK): Foreign key referencing Course_Offering table <br>
* Cap: Capacity of number of students allowed to enroll <br>
* Act: Actual number of students who enrolled <br>
* Rem: Remaining seats available <br>

## Term

* Term_ID (PK): Surrogate Key <br>
* Term_Name: The specific term/semester for the course <br>
* CRN(FK): Foreign key referencing Course_Offering table <br>

## Instructor

* I_ID (PK): Surrogate Key <br>
* Name: Name of the instructor teaching the course <br>
* Course_Title (FK): Foreign key referencing Course_Offerings table  <br>
* CRN: Course Reference Number <br>

## Time_Code

* Time_ID (PK): Surrogate Key <br>
* CRN (FK): Foreign key referencing Course_Offerings table  <br>
* Start_Time: Starting time of the course in ISO <br>
* End_Time: Ending time of the course in ISO <br>

## Location

* Room_ID (PK): Surrogate Key <br>
* Room_No: Building and room information from 'Location' <br>
* CRN (FK): Foreign key referencing Course_Meetings table <br>