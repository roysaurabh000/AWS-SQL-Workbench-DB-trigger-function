# AWS-SQL-Workbench-DB-trigger-function

Step 1: Create an account on amazon AWS at https://aws.amazon.com/free/Links to an external site.

 

Step 2: Follow the instructions  to create the database on AWS and change the settings.

 



 

You also need to change the inbound rule related to the security group to 0.0.0.0/0 to allow connections from any IP address. 

You also need to create a custom DB parameter group and set the parameter log_bin_trust_function_creators=1.

 

Step 3: use SalesCo2.sql to create this database with all the tables and records



SalesCo2.sqlDownload SalesCo2.sql

Step 4: Create a trigger named trg_line_prod that automatically updates the quantity on hand (P_QOH) for each product sold after a new LINE row is added.

Provide a picture of created trigger (right-click on the LINE table and select table inspector and go to trigger tab )

 

Step 5: Run commands below to test the trigger.

SET SQL_SAFE_UPDATES = 0;

INSERT INTO LINE VALUES('1008','2','54778-2T','3','4.99','14.97');
