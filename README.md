# Oracle Database PDB Management Assignment
______________________________________________________________
Name: Honette Igiraneza
Student ID: 27707
Instructor: Maniraguha Eric

Task 1: Creating a Pluggable Database
In this task, I created a new pluggable database (PDB) named ho_pdb_27707. which will help to store all class work
The creation was done from the root container using the CREATE PLUGGABLE DATABASE command, and I verified the new PDB with the SHOW PDBS command.

-Commands executed:
CREATE PLUGGABLE DATABASE ho_pdb_27707 
ADMIN USER honette-plsqlauca-27707 IDENTIFIED BY Welcome123
FILE_NAME_CONVERT=('C:\app\juliette\product\21c\oradata\XE\PDBSEED',
                   'C:\app\juliette\product\21c\oradata\XE\ho_pdb_27707');

ALTER PLUGGABLE DATABASE ho_pdb_27707 OPEN;
SHOW PDBS;
<img width="650" height="316" alt="PDB creation" src="https://github.com/user-attachments/assets/d9b9b05f-6973-4313-a2c4-e199aa44ac26" />

Task 2:Creation and Deletion of a Pluggable Database
In this task, I created and then deleted a temporary PDB named ho_to_delete_pdb_27707.
Before dropping a PDB, Oracle requires that it is closed. After closing it, I dropped the PDB including its datafiles and verified that it was removed.

-Commands executed:
CREATE PLUGGABLE DATABASE ho_to_delete_pdb_27707
ADMIN USER admin IDENTIFIED BY Welcome123
FILE_NAME_CONVERT=('C:\app\juliette\product\21c\oradata\XE\PDBSEED',
                    'C:\app\juliette\product\21c\oradata\XE\ho_to_delete_pdb_27707');
<img width="801" height="309" alt="new PDB" src="https://github.com/user-attachments/assets/4c303145-4cc4-42db-8bd3-c3ee7134d9f5" />

After creating it i deleted it using these commands:
ALTER PLUGGABLE DATABASE ho_to_delete_pdb_27707 CLOSE IMMEDIATE;
DROP PLUGGABLE DATABASE ho_to_delete_pdb_27707 INCLUDING DATAFILES;
<img width="623" height="263" alt="Delete PDB" src="https://github.com/user-attachments/assets/8881e2f0-0b3e-460e-9ace-2fd3481ad770" />

Task 3: Oracle Enterprise Manager (OEM) Express
In this task, I accessed Oracle Enterprise Manager (EM Express) using my browser at:
https://localhost:5500/em
I logged in with my created user HONETTE_PLSQLAUCA_27707 under the pluggable database ho_pdb_27707.
The OEM dashboard provided insights into database performance, sessions, and storage usage.
<img width="1337" height="644" alt="OEM" src="https://github.com/user-attachments/assets/ed7c6c3e-3afc-4650-92ed-dc1c17d679b4" />

Conclusion

Through this assignment, I gained practical skills in Oracle Database 21c pluggable database management. I successfully:

-Created a new pluggable database
-Dropped a pluggable database safely
-Accessed and explored Oracle Enterprise Manager Express

This hands-on exercise helped me understand Oracle Multitenant architecture and database administration concepts more clearly.

References

-Oracle Database 21c Documentation: https://docs.oracle.com/en/database/oracle/oracle-database/21/
-Class Lecture Notes





