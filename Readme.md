<img src="https://i.imgur.com/SsfgzAq.png" width=50%/> <br>

# BA 510 Course Data Project
__Spring 2020__

___

<b> Step 1 </b> : Design an Entity Relationship Diagram [link](./docs/CourseDataERD.pdf) <br>

<b> Step 2: </b> Build the Operational Database [link](CourseDataETL.ipynb) <br>
1. Create Import Tables
2. Extract data from CSV files, Transform, Load into Import Tables
    - Clean Datasets
3. Create Tables from ERD
4. Populate the ERD Tables from The Imported Data Tables
5. Empty out the Import Tables to reclaim storage space
    
<b> Step 3: </b> Test the Operational Database [link](CourseDataTest.ipynb) <br>

<b> Step 4: </b> Create a Demo [link](http://mayosql.me) <br>

<b> Step 5: </b> Design A Star Schema [link](./docs/fact-table-management.pdf) <br>
- Create a Fact Table: COURSES_FACT
- Create 4 Dimension Tables: PROGRAMS_DIM, LOCATIONS_DIM, FACULTY_DIM, COURSE_CATALOGS_DIM
    
<b> Step 6: </b> Build the DataWarehouse [link](CourseDataWarehouseTest.ipynb) <br>
    - Rebuilding the missing catalog years [link](./fixing_catalog_years/fixing_missing_program_name_and_code.ipynb)
    
<b> Step 7: </b> Test the DataWarehouse [link](CourseDataWarehouseTest.ipynb) <br>

<b> Step 8: </b> Create a Demo with 3 queries [link](CourseDataWarehouseDemo.ipynb)
