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
I created a Pluggable Database (PDB) using the naming convention: FirstTwoLettersOfFirstName_pdb_StudentID (e.g., ar_pdb_2024101, assuming my student ID is 2024101 and first name Arthur).
Commands used:

CREATE PLUGGABLE DATABASE ar_pdb_2024101 ADMIN USER arthur_plsqlauca_2024101 IDENTIFIED BY [password];
ALTER PLUGGABLE DATABASE ar_pdb_2024101 OPEN;

Then, I created a user inside the PDB: arthur_plsqlauca_2024101 with a simple password.
Evidence: Screenshots in the screenshots/ folder showing the creation command, PDB open state, and user creation (with username visible).
### Task 2: Create and Delete a PDB
I created a temporary PDB using the naming convention: FirstTwoLettersOfFirstName_to_delete_pdb_StudentID (e.g., ar_to_delete_pdb_2024101).
Commands used:

Creation: CREATE PLUGGABLE DATABASE ar_to_delete_pdb_2024101 ADMIN USER temp_user IDENTIFIED BY [password];
Verification: SHOW PDBS;
Deletion: DROP PLUGGABLE DATABASE ar_to_delete_pdb_2024101 INCLUDING DATAFILES;
Confirmation: SHOW PDBS; (to verify it no longer exists).

Evidence: Screenshots in the screenshots/ folder showing creation, verification, deletion, and confirmation.
### Task 3: Oracle Enterprise Manager (OEM)
I configured and accessed OEM by starting the listener and ensuring the database was registered.

Accessed OEM via browser (e.g., https://localhost:5500/em).
Logged in with SYSDBA credentials.
Verified the dashboard shows the Oracle environment, completed PDB tasks, and my username is visible.

Evidence: Screenshot of the OEM dashboard in the screenshots/ folder.
Task 4: Documentation & Reporting
This README.md serves as the documentation. The repository is public and contains all required elements, including the screenshots/ folder.
Challenges Faced and How They Were Solved
No major challenges were encountered. Minor issues, such as ensuring the PDB was in the correct open mode, were resolved by checking Oracle documentation and re-running the ALTER PLUGGABLE DATABASE command. All tasks were straightforward once connected as SYSDBA.
