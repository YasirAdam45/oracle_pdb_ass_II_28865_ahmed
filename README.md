# Oracle Pluggable Databases (PDB) Management - Assignment II

**Name:** [ahmed adam yasir ibrahim]
**Student ID:** [28865]
**Group:** [B]


## TASK 1
### creating pluggable database
```spl
CREATE PLUGGABLE DATABASE ah_pdb_28865 
ADMIN USER ahmed_plsqlauca_28865 IDENTIFIED BY "1234567"
FILE_NAME_CONVERT = ('/pdbseed_path/', '/ah_pdb_28865_path/');
```
<img width="2527" height="1172" alt="create plgdatabase" src="https://github.com/user-attachments/assets/67a01ccd-9ddf-4b94-aab9-d25a3186d91f" />


### open pluggable database
```spl
ALTER PLUGGABLE DATABASE ah_pdb_28865 OPEN;
SHOW PDBS;
```
<img width="2372" height="1277" alt="open plg database" src="https://github.com/user-attachments/assets/0448136f-6f67-403b-b5ed-60c4b88f7638" />


### create user
```spl
ALTER SESSION SET CONTAINER = ah_pdb_28865;

SELECT username, account_status 
FROM dba_users 
WHERE UPPER(username) LIKE '%AHMED%' OR UPPER(username) LIKE '%28865%';
```
<img width="2507" height="1142" alt="check the user" src="https://github.com/user-attachments/assets/6e6cd066-8755-45f4-a297-2381bb378868" />


## TASK 2
#### Create the temporary PDB
```spl
CREATE PLUGGABLE DATABASE ah_to_delete_pdb_28865 
ADMIN USER admin_temp IDENTIFIED BY "12345";

SHOW PDBS;
```
<img width="2534" height="1158" alt="create temp plgdatabase" src="https://github.com/user-attachments/assets/a8afb241-f454-4a0b-8f09-fc67c4b0176f" />


### Delete the temp pluggable database
```spl
DROP PLUGGABLE DATABASE ah_to_delete_pdb_28865 INCLUDING DATAFILES;

SHOW PDBS;
```
<img width="2500" height="1176" alt="delete temp plgdatabase" src="https://github.com/user-attachments/assets/5f6614a5-e9e0-44c6-b708-86edb4bf0ab1" />

## TASK 3
### OEM page
<img width="2468" height="1124" alt="oem" src="https://github.com/user-attachments/assets/9138b88a-6ced-46e8-b1f1-d08173e62fd8" />







