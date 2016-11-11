# Cloud Computing Final Project - SQL with DashDB & Node.js

An implementation of cloud SQL querying using DashDB, Node.js and IBM DevOps Services

Conor Hanavan		
21303234

This code may be found at:
    https://github.com/Hanavcm/Cloud-SQL-Implementation


## Summary

The aim of this implementation was firstly to transfer an excel/csv file database onto the cloud, whilst not impeding the analytic and manipulative properties of the database. This was achieved by utilizing the IBM DashDB on Bluemix, where uploading a csv file from desktop is relatively self explanatory.

To retain the analytic properties that would accompany the likes of an excel spreadsheet, DashDB is integrated with 'R' based data analytic services, which allow for such things as graphs, charts, and summary tables to be created based on the values stored within the database.

Next, a Node.js webapp was implemented to output the entire stored table on a hosted webpage. This was done using a combination of Node.js, Jade, and Express, all hosted on IBMs Bluemix DevOps service.

The main sections of hard-code in this implementation are the app.js and the index.js files as they are responsible for the operation of the JavaScript webapp.

## Functional Requirements Fulfilled (Action)

1. Updating & querying the database using SQL in DashDB
2. Appending new rows to the tables in DashDB
3. Exporting a query result to a javascript webapp
4. Javascript hosted query result will automatically update and sync up with any changes in DashDB as the webapp is refreshed.
5. Data analytic tools using 'R' to a minor extent

## Non Functional Requirements (Static)

1. The Ability to bring a csv/xlsx database to the cloud 
2. Multiple people may access/view the hosted Javascript output if they so require
3. Any changes to database will not require re-deployment of the app for them to take effect, only for the Javascript webapp to be refreshed.
4. Convert new/updated databases into csv files for desktop storage and manipulation in excel


## Running the Javascript function & App

A simple guide to the usage of this implementation

1. Download sample data excel file from git repository
2. Upload from desktop to an IBM DashDB service using IBM Bluemix console
3. Connect and Link said DashDB service to an empty JS DevOps app in bluemix
4. Extract contents of project zip file to the empty JS DevOps application
5. Deploy the application using the GUI interface
6. Opening the deployed app will open the hosted webpage containing the output of the query. 


+++++++++++++++++++++++++++++++++++++++++++++++++++++++


NB: The user may then begin to edit the query in index.js if they wish to change the result of the query, for example: rather than selecting all elements as per:

	SELECT * from SAMPLEDATA

It could be changed to a :

	SELECT * FROM SAMPLEDATA WHERE "Rep" = 'Kivell'; 

This will result in the JS app only displaying the rows of the table where Kivell is the rep responsible for the orders of those products.
And so on and so forth should they wish to edit the operation.


