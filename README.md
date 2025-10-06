# Oracle PDB Management Assignment

This repository contains my Oracle Database assignment on **creating and managing Pluggable Databases (PDBs)**.  
The project demonstrates how to create, open, close, and drop a PDB using SQL*Plus commands.

---

## Step 1: Task Overview 

**Objective**  
- Create a pluggable database named: `ba_pdb_27189`  
- Create another pluggable database named: `ba_to_delete_pdb_27189` and then delete it.  

**Environment Used**  
- Oracle Database 19c  
- SQL*Plus command-line interface  
- Windows OS  

---

## Step 2: Database Creation 

**Commands Used:**

sql
CREATE PLUGGABLE DATABASE ba_pdb_27189
ADMIN USER bahati_plsqlauca_27189 IDENTIFIED BY "Bahati123"
FILE_NAME_CONVERT = (
  'C:/USERS/HP/DESKTOP/ORADATA/ORCL/PDBSEED/',
  'C:/USERS/HP/DESKTOP/ORADATA/ORCL/ba_pdb_27189/'
);
After successful creation, the database was opened using:

ALTER PLUGGABLE DATABASE ba_pdb_27189 OPEN;


Verification:

SHOW PDBS;

Step 3: Create and Delete Another PDB 

Creation

CREATE PLUGGABLE DATABASE ba_to_delete_pdb_27189
ADMIN USER bahati_plsqlauca_27189 IDENTIFIED BY "Bahati123"
FILE_NAME_CONVERT = (
  'C:/USERS/HP/DESKTOP/ORADATA/ORCL/PDBSEED/',
  'C:/USERS/HP/DESKTOP/ORADATA/ORCL/ba_to_delete_pdb_27189/'
);


Deletion

ALTER PLUGGABLE DATABASE ba_to_delete_pdb_27189 CLOSE IMMEDIATE;
DROP PLUGGABLE DATABASE ba_to_delete_pdb_27189 INCLUDING DATAFILES;

Step 4: Screenshots and Report 

Full Report:
View Report
Step 5: Results

Successfully created and opened ba_pdb_27189.

Successfully created and deleted ba_to_delete_pdb_27189.

All SQL commands executed without syntax or path errors.

Screenshots (Creation & Deletion):
View Screenshots
Step 6: References 

Oracle. Multitenant: Managing Pluggable Databases. https://docs.oracle.com

W3Schools. Oracle CREATE PLUGGABLE DATABASE Statement. https://www.w3schools.com/sql

GeeksforGeeks. Pluggable Database in Oracle 19c. https://www.geeksforgeeks.org

OracleBase. How to Create and Drop PDBs. https://oracle-base.com

Stack Overflow. ORA-65005 Error Solutions. https://stackoverflow.com
