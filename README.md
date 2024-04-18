# DataAnalysis-week2
OLTPs(Online Transactional Process) A system that handles all online transactions.
Normalization - a process in which stuctures a database in way that minimises duplicates
First Normal form - contains unique values in each column.
Second Normal form -all non primary key values must depend on the primary key.
Third Normal form - all data in columns must depend on the primary key
Online Analytical Processing - Focus on the ability of an organisation to analyze data
OLAPs- Data warehouse wider data with more complex queries and rigid schema.
OLTPs- data stored in rows and columns , data is highly detailed, flexible schema , database is very fast at querying.
Star schema - is a schema diagram with a star shaped connection with the fact diagram at the centre
Intergration: Data from transactional systems flow into data warehouses and data marts for analysis
You need to retrieve, reshape, and insert data to move data between operational and analytical environments
One approach is known as extract, transform, and load (ETL)
Extract - you extract data from the source system and place it in a staging area. The goal of the extract phase is to move data from a relational database into a flat file as quickly as possible.
Transform -The second phase transforms the data. The goal is to reformat the data from its transactional structure to the data warehouse's analytical design.
Load -The purpose of the load phase is to ensure data gets into the analytical system as quickly as possible.
API is a structured method for computer systems to exchange information. APIs provide a consistent interface to calling applications, regardless of the internal database structure.
