{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Data Dictionary"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Catalog_Program"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* CP_ID (PK): Surrogate Key <br>\n",
    "* Program_Code: Code of the Program name <br>\n",
    "* Program_Name: Program or department name <br>\n",
    "* Course_Title: Name of the course <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Catalog_Courses"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* CC_ID (PK): Surrogate Key <br>\n",
    "* CRN: Course Reference Number <br>\n",
    "* Course_Title: Name of the course <br>\n",
    "* CP_ID (FK): Foreign key referencing Catalog_Program table <br>\n",
    "* Pre_Reqs: Prerequisite for the course <br>\n",
    "* Co_Reqs: Corequisite for the course <br>\n",
    "* Credits: Number of credits for the course <br>\n",
    "* Fees: Course cost <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Course_Offerings"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* CO_ID (PK): Surrogate Key <br>\n",
    "* CRN: Course Reference Number <br>\n",
    "* CC_ID (FK): Foreign key referencing Catalog_Courses table <br>\n",
    "* Section: Section of the course <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Course_Meetings"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* CM_ID: Surrogate Key <br>\n",
    "* CRN: Course Reference Number <br>\n",
    "* Cap: Capacity of number of students allowed to enroll <br>\n",
    "* Act: Actual number of students who enrolled <br>\n",
    "* Rem: Remaining seats available <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Term"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* Term_ID (PK): Surrogate Key <br>\n",
    "* Term_Name: The specific term/semester for the course <br>\n",
    "* CC_ID (FK): Foreign key referencing Catalog_Courses table <br>\n",
    "* Start: Start date of the course in ISO <br>\n",
    "* End: End date of the course in ISO <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Instructor"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* I_ID (PK): Surrogate Key <br>\n",
    "* Name: Name of the instructor teaching the course <br>\n",
    "* CRN: Course Reference Number <br>\n",
    "* CO_ID (FK): Foreign key referencing Course_Offerings table  <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Timecodes"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* Time_ID (PK): Surrogate Key <br>\n",
    "* CO_ID (FK): Foreign key referencing Course_Offerings table  <br>\n",
    "* Start_Time: Starting time of the course in ISO <br>\n",
    "* End_Time: Ending time of the course in ISO <br>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Location"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "* Room_ID (PK): Surrogate Key <br>\n",
    "* Bldng_Name: Building and room information from 'Location' <br>\n",
    "* CM_ID (FK): Foreign key referencing Course_Meetings table <br>"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
