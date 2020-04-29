# BA 510 Course Data Project
__Spring 2020__ <br>
___

%%html
<style>
    table {
        display: inline-block
    }
</style>


## Course Data Dictionary:

### COURSE TABLE
| **Key**     | **Field**   | **Data Type** | **Description**                                                                                                                       |
|-------------|-------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Primary Key | CID         | INTEGER       | Course ID \(Surrogate Key\)                                                                                                           |
| Foreign Key | PID         | INTEGER       | Program ID \(Surrogate Key\)                                                                                                          |
|  <br>       | CatalogID   | TEXT          | Identifies the department and course number for a particular course                                                                   |
|  <br>       | CatalogYear | TEXT          | The academic year for a particular Catalog ID                                                                                         |
|  <br>       | CourseTitle | TEXT          | Official Title of the Course                                                                                                          |
|  <br>       | Credits     | TEXT          | Number of credits given for a particular course which gives weighting to: the value, level or time requirements of an academic course |
|  <br>       | Prereqs     | TEXT          | Prerequisits for a particular course                                                                                                  |
|  <br>       | Coreqs      | TEXT          | A course or other requirement that a student must take at the same time as another course or requirement\.                            |
|  <br>       | Fees        | TEXT          | Material fees related to a particular course                                                                                          |
|  <br>       | Attributes  | TEXT          | Attributes related to a particular course providing additional information                                                            |
|  <br>       | Description | TEXT          | Description of a particular course                                                                                                    |

### COURSE_OFFERING TABLE
| **Key**     | **Field** | **Data Type** | **Description**                                                                                                                                                        |
|-------------|-----------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Primary Key | COID      | INTEGER       | Course Offering ID \(Surrogate Key\)                                                                                                                                   |
| Foreign Key | CID       | INTEGER       | Course ID \(Surrogate Key\)                                                                                                                                            |
| Foreign Key | FID       | INTEGER       | Faculty ID \(Surrogate Key\)                                                                                                                                           |
|  <br>       | CRN       | INTEGER       |  Course Reference Number, is the 5\-digit number that is assigned to each course                                                                                       |
|  <br>       | Semester  | TEXT          | A half\-year term, typically lasting fifteen weeks\. An academic term which is a portion of an academic year, the time during which Fairfield University holds classes |
|  <br>       | Year      | INTEGER       | The year referencing the year of the semester during which classes are held                                                                                            |
|  <br>       | Title     | TEXT          | Official Title of the Course                                                                                                                                           |
|  <br>       | Meetings  | TEXT          | Meetings for a particular course: 'days':<day of the week>, 'times':<hhmm\(<am/pm>\)>\-<hhmm\(<am/pm>\)>, 'dates': <mm/dd\-mm/dd>, 'location': <location>              |
|  <br>       | Timecodes | TEXT          | Timecodes for a particular course: <day of the week, times, dates, location>                                                                                           |
|  <br>       | Section   | TEXT          | Identifier for the section of a particular course \(to be able to distinguish multiple sections taught for the same course\)                                           |
|  <br>       | Cap       | INTEGER       | Capacity for the number of students of a particular course                                                                                                             |
|  <br>       | Act       | INTEGER       | Actual enrollment of students of a particular course                                                                                                                   |
|  <br>       | Rem       | INTEGER       | Remaining number of spots available for a particular course                                                                                                            |

### CLASS_MEETINGS TABLE
| **Key**     | **Field** | **Data Type** | **Description**                                                                                                                                                        |
|-------------|-----------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Primary Key | CMID      | INTEGER       | Class Meetings ID \(Surrogate Key\)                                                                                                                                    |
| Foreign Key | COID      | INTEGER       | Course Offering ID \(Surrogate Key\)                                                                                                                                   |
| Foreign Key | LID       | INTEGER       | Location ID \(Surrogate Key\)                                                                                                                                          |
|  <br>       | Day       | TEXT          | Day of the week for the scheduled class meeting: \(M=Monday, T=Tuesday, W=Wednesday, R=Thursday, F=Friday, S=Saturday, U=Sunday\)                                      |
|  <br>       | Start     | TEXT          | Start date and time of a particular course:  <yyyy\-mm\-ddTHH:MM:SS>                                                                                                   |
|  <br>       | End       | TEXT          | End date and time of a particular course:  <yyyy\-mm\-ddTHH:MM:SS>                                                                                                     |
|  <br>       | Semester  | TEXT          | A half\-year term, typically lasting fifteen weeks\. An academic term which is a portion of an academic year, the time during which Fairfield University holds classes |
|  <br>       | Year      | INTEGER       | The year referencing the year of the semester during which classes are held                                                                                            |

### PROGRAMS TABLE
| **Key**     | **Field**   | **Data Type** | **Description**                                                                                                                                                                               |
|-------------|-------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Primary Key | PID         | INTEGER       | Program ID \(Surrogate Key\)                                                                                                                                                                  |
|  <br>       | ProgramCode | TEXT          | Unique identifier for the program code: \(length of 2 or more capitalized letters \[A\-Z\]\)                                                                                                  |
|  <br>       | ProgramName | TEXT          | Academic program name: representing any combination of courses and/or requirements leading to a degree or certificate, or to a major, co\-major, minor or academic track and/or concentration |

### FACULTY TABLE
| **Key**     | **Field**         | **Data Type** | **Description**              |
|-------------|-------------------|---------------|------------------------------|
| Primary Key | FID               | INTEGER       | Faculty ID \(Surrogate Key\) |
|  <br>       | instructor\_fname | TEXT          | Instructor's First Name      |
|  <br>       | instructor\_lname | TEXT          | Instructor's Last Name       |

### LOCATION TABLE
| **Primary Key** | **LID**      | **INTEGER** | **Location ID (Surrogate Key)**                                                                                         |
|-----------------|--------------|-------------|-------------------------------------------------------------------------------------------------------------------------|
|  <br>           | BuildingRoom | TEXT        | Unique identifier for the building room: 1 or more letters \[A\-Z\] and optionally a room number \(divided by a space\) |
|  <br>           | BuildingName | TEXT        | Full Name of the University's building                                                                                  |
