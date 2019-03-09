# Data Dictionary
## Catalog_Program

* CP_ID (PK): Surrogate Key <br>
* Program_Code: Code of the Program name <br>
* Program_Name: Program or department name <br>
* Course_Title: Name of the course <br>

## Catalog_Courses

* CC_ID (PK): Surrogate Key <br>
* CRN: Course Reference Number <br>
* Course_Title: Name of the course <br>
* CP_ID (FK): Foreign key referencing Catalog_Program table <br>
* Pre_Reqs: Prerequisite for the course <br>
* Co_Reqs: Corequisite for the course <br>
* Credits: Number of credits for the course <br>
* Fees: Course cost <br>

## Course_Offerings

* CO_ID (PK): Surrogate Key <br>
* CRN: Course Reference Number <br>
* CC_ID (FK): Foreign key referencing Catalog_Courses table <br>
* Section: Section of the course <br>

## Course_Meetings

* CM_ID: Surrogate Key <br>
* CRN: Course Reference Number <br>
* Cap: Capacity of number of students allowed to enroll <br>
* Act: Actual number of students who enrolled <br>
* Rem: Remaining seats available <br>

## Term

* Term_ID (PK): Surrogate Key <br>
* Term_Name: The specific term/semester for the course <br>
* CC_ID (FK): Foreign key referencing Catalog_Courses table <br>
* Start: Start date of the course in ISO <br>
* End: End date of the course in ISO <br>

## Instructor
* I_ID (PK): Surrogate Key <br>
* Name: Name of the instructor teaching the course <br>
* CRN: Course Reference Number <br>
* CO_ID (FK): Foreign key referencing Course_Offerings table  <br>

## Timecodes
* Time_ID (PK): Surrogate Key <br>
* CO_ID (FK): Foreign key referencing Course_Offerings table  <br>
* Start_Time: Starting time of the course in ISO <br>
* End_Time: Ending time of the course in ISO <br>

## Location
* Room_ID (PK): Surrogate Key <br>
* Bldng_Name: Building and room information from 'Location' <br>
* CM_ID (FK): Foreign key referencing Course_Meetings table <br>