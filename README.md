# db2r
A Db2 demo using R functions that analyze taxi bookings

## Description
The demo links to a Db2 TAXIDB Columnar Store Database.  It then selects trip data that demonstrates taxi times between mid down Manhatten and NYC Airports.  It then uses Weather information to perform predicitions on increased trip time based on weather events.

The demo has been tested on Windows 10 environments although other environments also should work. 

The demo comes with the following components: 
1.  TAXIDB sample database (created with DB2 Backup)
2.  A sample R Notebook with program called TaxiDemo.RDB

In order to execute the program the following must be installed.

1.  DB2 Developer-C Docker Image
2.  R and R Notebooks
3.  R Studio  (or R Studio with dashDB or DSX)

After installing the DB2 Docker Image - configured for columnar store SAMPLE database, move the backup image to the Database "shared" Directory indicated in Database Connection Details.  Then run Restore command to restore the TAXIDB sample database.  Command can be created in Run SQL.  

Sample Restore:

RESTORE DATABASE TAXIDB FROM "/db2fs/backups" TAKEN AT 20170620131623 TO "/db2fs" INTO TAXIDB WITHOUT PROMPTING; 

Connectivity must be set up by installing Data Server Driver and configuring an ODBC Data Source in the ODBC Data Source Administrator (64-bit).  
