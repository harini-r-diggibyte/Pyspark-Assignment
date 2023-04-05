# Pyspark-Assignment
This repository contains Pyspark assignment.


Product Name	   Issue Date	    Price	  Brand	    Country	Product number
Washing Machine	 1648770933000	20000	  Samsung	  India	  0001
Refrigerator	   1648770999000	35000	  LG	      null	  0002
Air Cooler	     1648770948000	45000	  Voltas	  null	  0003

Create a table in the above structure.
It is referred as table 1.

This is done by the function create_table()

After completing the creation, we work on it to satisfy the below scenarios.

  - Convert the Issue Date with the timestamp format.

Example: 
Input: 1648770933000 -> Output: 2022-03-31T23:55:33.000+0000

This is done by the function timestamp_to_unixTime()

  - Convert timestamp to date type	  

Example: 
Input: 2022-03-31T23:55:33.000+0000 -> Output: 2022-03-31

This is done by the function convert_date()

  - Remove the starting extra space in Brand column for LG and Voltas fields

This is done by the function trim_spaces()

  - Replace null values with empty values in Country column 

This is done by the function replace_null_with_empty_values()


Create another table with the below data and referred as table 2.

SourceId	TransactionNumber	Language	ModelNumber	StartTime	                      Product Number
150711	  123456	          EN	      456789	    2021-12-27T08:20:29.842+0000    0001
150439	  234567	          UK	      345678	    2021-12-27T08:21:14.645+0000    0002
150647	  345678	          ES	      234567	    2021-12-27T08:22:42.445+0000    0003

This is done by the function creating_table_2()

After creating table, we work on it to satisfy the below scenarios.

  - Change the camel case columns to snake case 
  
Example: 
SourceId: source_id
TransactionNumber: transaction_number

This is done by the function column_case_conversion()

  - Add another column as start_time_ms and convert the values of StartTime to milliseconds.

Example: 
Input: 2021-12-27T08:20:29.842+0000 -> Output: 1640593229842
Input: 2021-12-27T08:21:14.645+0000 -> Output: 1640593274645

This is done by the function timestamp_to_unix_timestamp()

  - Combine both the tables based on the Product Number 
        - and get all the fields in return.
        - And get the country as EN
joining of tables is done by the function join_table()

Filtering the records based on the language column value "EN" is done by the function filter_records()
