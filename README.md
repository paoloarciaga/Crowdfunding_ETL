# Crowdfunding ETL Pipeline Project

This project was completed by Jessica Padilla, Sharon Romero, Maritza Ahumada, Marco Nigro, and Paolo Arciaga. We collaborated amongst each other in order to debug certain parts of our code. 

Within this repo, you will be able to see how we completed the following: 

## Creating the Category and Subcategory DataFrames
- Extracted and transformed the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  - A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
  - A "category" column that contains only the category titles
- Exported the category DataFrame as category.csv and save it to your GitHub repository.
- Extracted and transformed the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
  - A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
  - A "subcategory" column that contains only the subcategory titles
- Exported the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.
  
## Creating the Campaign DataFrame
- Extracted and transformed the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
  - The "cf_id" column
  - The "contact_id" column
  - The "company_name" column
  - The "blurb" column, renamed to "description"
  - The "goal" column, converted to the float data type
  - The "pledged" column, converted to the float data type
  - The "outcome" column
  - The "backers_count" column
  - The "country" column
  - The "currency" column
  - The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
  - The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
  - The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
  - The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
- Exported the campaign DataFrame as campaign.csv and save it to your GitHub repository.
  
## Creating the Contacts DataFrame
Option 1: Used Python dictionary methods.
Option 2: Used regular expressions.

Option 1: 

- Imported the contacts.xlsx file into a DataFrame.
- Iterated through the DataFrame, converting each row to a dictionary.
- Iterated through each dictionary, doing the following:
- Extracted the dictionary values from the keys by using a Python list comprehension.
- Added the values for each row to a new list.
- Created a new DataFrame that contains the extracted data.
- Split each "name" column value into a first and last name, and placed each in a new column.
- Cleaned and export the DataFrame as contacts.csv and save it to your GitHub repository.

Option 2:

- Imported the contacts.xlsx file into a DataFrame.
- Extracted the "contact_id", "name", and "email" columns by using regular expressions.
- Created a new DataFrame with the extracted data.
- Converted the "contact_id" column to the integer type.
- Split each "name" column value into a first and a last name, and placed each in a new column.
- Cleaned and then exported the DataFrame as contacts.csv and save it to your GitHub repository.

## Creating the Crowdfunding Database
- Inspected the four CSV files, and then sketched an ERD of the tables by using QuickDBDLinks 
- Used the information from the ERD to create a table schema for each CSV file.
- Specified the data types, primary keys, foreign keys, and other constraints.
- Saved the database schema as a Postgres file named crowdfunding_db_schema.sql, and saved it to our repository.
- Created a new Postgres database, named crowdfunding_db.
- Using the database schema, we created the tables in the correct order to handle the foreign keys.
- Verified the table creation by running a SELECT statement for each table.
- Imported each CSV file into its corresponding SQL table.
- Verified that each table has the correct data by running a SELECT statement for each.
