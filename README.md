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
Web services - Many smartphone applications need a network connection, either cellular or Wi-Fi, to work correctly. The reason is that much of the data these applications need is not on the smartphone itself. Instead, data is found in private and public data sources and is accessible via a web service. A web service is an API you can call via Hypertext Transfer Protocol (HTTP), the language of the World Wide Web.While a web service is an API, an API does not have to be a web service
Web Scrapping -If data exists in a structured format, you can retrieve it programmatically. Programmatic retrieval of data from a website is known as web scraping.
Human in the loop -There are times when the data you seek exists only in people's minds. For example, you can extract the most popular and profitable motorcycling destination from your existing internal data. 
Survey -One way to collect data directly from your customers is by conducting a survey. Surveys can be much more complicated than a single question. For example, suppose you want a comprehensive understanding of customer satisfaction. In that case, you design a sophisticated survey that presents people with different questions depending on their answers. Complex survey logic lets you gather additional details as to why a person has a particular opinion.
Observation- Observation is the act of collecting primary source data, from either people or machines. Observational data can be qualitative or quantitative. Collecting qualitative observational data leads to unstructured data challenges.
sampling -Regardless of the data acquisition approach, you may end up with more data than is practical to manipulate. Imagine you are doing analytics in an Internet-of-Things environment, in which 800 billion events occur daily.
Data Manipulation
Create - Insert 
Read - Select 
Update -UpdaTE
Delete - delete
Select <what> from <source>.
SELECT  Animal_Name, Breed_Name

FROM   Animal

WHERE  Animal_Type = 'Dog'

AND   Weight> 60

ORDER BY Date_of_Birth DESC

Boolean

SELECT  Animal_Name, IFF(Sex = 'M', 'Male', 'Female')

FROM   Animal

SQL aggregate functions
Count,Min,Max,AVG,SUM,STDDEV

Querying optimization
Parametrization:
Whenever a SQL query executes, the database has to parse the query. Parsing translates the human-readable SQL into code the database understands. Parsing takes time and impacts how long it takes for a query to return data. Effective use of parameterization reduces the number of times the database has to parse individual queries.
Indexing :
A database index can point to a single column or multiple columns. When running queries on large tables, it is ideal if all of the columns you are retrieving exist in the index. If that is not feasible, you at least want the first column in your SELECT statement to be covered by an index.
Subsets and temporary tables
When dealing with large data volumes, you may want to work with a subset of records. For example, suppose an organization has 1,000,000 customers. Each of those customers places 200 orders per year, and there are 10 years of data in the data warehouse. In this situation, the Order table in the data warehouse would have 2 billion rows. If you want to explore trends for a specific customer's order history, it would not be efficient to query the main Order table.
Execution plan : An execution plan shows the details of how a database runs a specific query. Execution plans are extremely helpful in troubleshooting query performance issues. They provide additional information about how a query is spending its time. For example, an execution plan can tell you if a slow-running query uses a full table scan instead of an index scan. 
  
  Data Quality:
  
Duplicate data occurs when data representing the same transaction is accidentally duplicated within a system. Suppose you want to open a spreadsheet on your local computer. To open the spreadsheet, you locate the file and double-click it. This method of opening documents establishes muscle memory that associates double-clicking with the desired action.
REedundant Data:
While duplicate data typically comes from accidental data entry, redundant data happens when the same data elements exist in multiple places within a system. Frequently, data redundancy is a function of integrating multiple systems.
Having multiple data sources for the same data elements is also a source of duplicate data
Missing Data :
Another issue that impacts data quality is the concept of missing values. Missing values occur when you expect an attribute to contain data but nothing is there. Missing values are also known as null values. A null value is the absence of a value. A null is not a space, blank, or other character. There are situations when allowing nulls makes sense.
A data outlier is a value that differs significantly from other observations in a dataset. Consider the real estate sale price example in Figure 4.10. All of the properties are on the same street, city, and state. Most of the properties have a sale price between $128,000 and $153,000. However, the property at 130 Main Street has a sale price of $26,496,400. That is a dramatic difference from the rest of the sales prices.

A specification describes the target value for a component. A specification mismatch occurs when an individual component's characteristics are beyond the range of acceptable values. For example, suppose you want to add a room to a house and you buy 15 wooden studs. Looking at the blueprint for the addition, you need wooden studs with a rectangular cross-section measuring 2 inches by 4 inches (2×4). When purchasing the studs, you want to ensure that all 15 have a consistent cross-section.

Invalid data are values outside the valid range for a given attribute. An invalid value violates a business rule instead of having an incorrect data type. As such, you have to understand the context of a system to determine whether or not a value is invalid.

Nonparametric data is data collected from categorical variables, which you read about in Chapter 2: Understanding Data. Sometimes the categories indicate differentiation, and sometimes they have a rank order associated with them. In this latter case, the rank order of the values is of significance, not the individual values themselves.

Data type validation ensures that values in a dataset have a consistent data type.The primary keys for both the Manufacturer and Model expect integer values, while the Manufacturer_Name and Model_Name are characters. Recall from Chapter 3 that the foreign key on Manufacturer_ID enforces referential integrity between the two tables.
Data manipulation techniques
Recoding data is a technique you can use to map original values for a variable into new values to facilitate analysis. Recoding groups data into multiple categories, creating a categorical variable. A categorical variable is either nominal or ordinal.

Recoding data is a technique you can use to map original values for a variable into new values to facilitate analysis. Recoding groups data into multiple categories, creating a categorical variable. A categorical variable is either nominal or ordinal. Nominal variables are any variable with two or more categories where there is no natural order of the categories, like hair color or eye color. 

A derived variable is a new variable resulting from a calculation on an existing variable. In the case of the recoded data in Figure 4.14, the Pain_Category categorical variable is an example of a derived variable. 

A data merge uses a common variable to combine multiple datasets with different structures into a single dataset. Merging data improves data quality by adding new variables to your existing data. Additional variables make for a richer dataset, which positively impacts the quality of your analysis. ETL processes commonly append data while transforming data for use in analytical environments.

Data blending combines multiple sources of data into a single dataset at the reporting layer. While data blending is conceptually similar to the extract, transform, and load process in Chapter 3, there is a crucial 
A data append combines multiple data sources with the same structure, resulting in a new dataset containing all the rows from the original datasets. When appending data, you save the result as a new dataset for ongoing analysis.

Imputation is a technique for dealing with missing values by replacing them with substitutes. When merging multiple data sources, you may end up with a dataset with many nulls in a given column. If you are collecting sensor data, it is possible to have missing values due to collection or transmission issues.

Approahes analysts can use to impute data:
removing missinf values
replacing with zero
replace the average
replace with most frequent mode 
Closest value average
