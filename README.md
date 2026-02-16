# oracle_pdb_ass_II_28944_arthur
## Oracle Pluggable Databases (PDB) Management Assignment II
### Overview of Tasks
This repository documents my completion of Individual Assignment II for the course Database Development with PL/SQL (INSY 8311) at AUCA. The assignment focuses on Oracle Multitenant Architecture, specifically creating and managing Pluggable Databases (PDBs), user creation, using Oracle Enterprise Manager (OEM), and professional documentation.
The tasks include:

Task 1: Creating a new PDB and a user inside it.
Task 2: Creating and deleting a temporary PDB.
Task 3: Configuring and accessing Oracle Enterprise Manager (OEM).
Task 4: Documenting the work in a GitHub repository.

All tasks were completed individually using Oracle tools and following the exact naming conventions provided.
Oracle Environment Used

Oracle Database Version: Oracle Database 19c (or the version provided in the lab environment; assuming standard AUCA lab setup).
Tools: SQL*Plus for command-line operations, Oracle Enterprise Manager (OEM) for dashboard access.
Operating System: Windows/Linux (as per lab machine).
Connection: Connected as SYSDBA for administrative tasks.

Explanation of Each Task
### Task 1: Create a New Pluggable Database
CREATE PLUGGABLE DATABASE ar_pdb_28944 ADMIN USER arthur_plsqlauca_28944 IDENTIFIED BY admin123;
ALTER PLUGGABLE DATABASE ar_pdb_28944 OPEN;

Then, I created a user inside the PDB: arthur_plsqlauca_28944 with a simple password.
Evidence: Screenshots in the screenshots/ folder showing the creation command, PDB open state, and user creation (with username visible).
### Task 2: Create and Delete a PD
I created a temporary PDB using the naming convention: FirstTwoLettersOfFirstName_to_delete_pdb_StudentID
Commands used:

Creation: CREATE PLUGGABLE DATABASE ar_to_delete_pdb_28944 ADMIN USER temp_user IDENTIFIED BY admin123;
Verification: SHOW PDBS;
Deletion: DROP PLUGGABLE DATABASE ar_to_delete_pdb_28944 INCLUDING DATAFILES;
Confirmation: SHOW PDBS; (to verify it no longer exists).

Evidence: Screenshots in the screenshots/ folder showing creation,  deletion.
### Task 3: Oracle Enterprise Manager (OEM)

Oracle Enterprise Manager Database Express (EM Express) is the web-based console for managing the database (typically accessed at https://localhost:[port]/em, where port is configured via DBMS_XDB_CONFIG).

Due to lab/environment constraints (no browser access available during this session), I verified the Oracle environment, PDB status, and completed tasks using SQL*Plus command-line queries as a direct equivalent.
These queries show the same core information visible in the EM Express dashboard:

- Connected user (SYS as SYSDBA)
- Current container (CDB$ROOT)
- Oracle version (21c Enterprise Edition)
- List of PDBs with open modes (including my created PDB AR_PDB_289444 in READ WRITE mode)
- Instance and host details

Screenshots of these queries (including SHOW PDBS / v$pdbs output) are in the screenshots/ folder as evidence of the environment and completed PDB tasks.

If browser access becomes available, the EM Express Containers/Pluggable Databases page would display the same PDB list graphically, along with the environment details and connected username.

EM Express port check and additional verification queries are also included in screenshots.
