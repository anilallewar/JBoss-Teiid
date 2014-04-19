JBoss-Teiid
===========

Demo project to show data virtualization and federation with JBoss Teiid
===========

The project is a JBoss Teiid example to show data virtualization and federation across mySql and MongoDB data stores.

Pre-requisites:
	1. mySQL server 5.5+ installed
	2. MongoDB 2.4.x+ installed
	
1. Start the mySQL service and MongoDB server and connect through the respective clients (mySql command line client/Mongo executable).
2. mySQL
	1. Create database called "sales" in the mySql instance.
	2. Execute the queries in "Documents/SQL Scripts-Loading mySQL and MongoDB.txt" file to create tables in mySQL instance in the "sales" database.
3. MondoDB
	1. Connect to the "sales" collection by using the command "use sales" in the mongo shell.
	2. Execute the insert mongo statements in the "Documents/SQL Scripts-Loading mySQL and MongoDB.txt" file to create the connections and insert data to them.
4. Install the JBoss EAP 6.1.0 Alpha application server and JBoss Teiid by following the instructions in the "Documents/JBoss Teiid Installation Instructions.txt".
5. Copy the "Documents/standalone-teiid.xml" file to the "${JBOSS_HOME}/standalone/configuration" folder and overwrite the existing file.
6. Copy the "sales-mongodb-vdb.xml" file to the "${JBOSS_HOME}/standalone/deployments" folder.
7. Start the JBoss server.
8. Import the database from Teiid (for the MongoDB VDB) and mySql and federate the sources to create a virtual model.
9. Create a VDB for the view model and deploy it on the JBoss server to access the data. More details on how to accomplish steps 8/9 will be demonstrated in the webinar. 


