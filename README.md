# **Crowdfunding_ETL** #
--------------

## **PROJECT GOAL** ##

This repository showcases an ETL (Extract-Transform-Load) pipeline built using Python, ultimately resulting in the upload of the transformed data to a database via pdAdmin4. The project demonstrates the practical application of data extraction and transformation techniques to prepare a dataset for further analysis.

---------------------------

## *EXTRACT:* ##
* Two Excel files, 'contacts.xlsx' and 'crowdfunding.xlsx', were used as source data. The data underwent extraction and transformation processes to ensure its cleanliness and suitability for loading into a database for future analytical use.

## **contacts.xlsx** ##
![Screenshot 2024-04-30 012459](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/495def13-a9f2-4b04-a3e4-f229a0407706)

## **crowdfunding.xlsx** ##
![Screenshot 2024-04-30 012537](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/e44a7ec9-8587-4bb8-b3ff-3c2ade9614cc)

-----------

## *TRANSFORM:* ##
This repository contains the code for an ETL (Extract, Tranform, and Load) pipeline. The pipeline is used to upload, clean, and reproduce crowdfunding data from excel files into csv dataframes and a crowdfunding database. The original excel crowdfunding information has data that is difficult to sift through. The categories and sub-categories decribing the crowdfunding projects are combined into a single column, making it difficult to filter through project categories. The project launch and funding deadline columns are named incorrectly and not set to date time data types. There are also extra columns that are not useful as well as column names that needed to be changed for clarity.
The excel file containing the contact information of crowdfunding campaigns is also poorly structured, with all the data existing in a single column, instead of being seperated by id, first name, and last name.

The code in this repository makes changes to these excel files, reorganizing and cleaning data as necessary as well as creating two new dataframes to reference the categories and subcategories of the projects.
The code also uses list comprehension methods to seperate the contact information into seperate columns. 
After making these transformations to the files, the new dataframes are saved as CSV files (Can be found in "Resources" folder). 

------------------------

## *LOAD:* ##
## **Crowdfunding DB ERD & Table Data** ##
* A database called "crowdfunding db" was created inside pgAdmin4 and a schema called "crowdfunding_db_schema.sql" was used to create the tables to allow for importing of the CSV files. SELECT * statements were ran on each table to ensure that each table's respective data was imported correctly from the CSV files

### **Crowdfunding DB Entity-Relationship Diagram (ERD)** ###
![Crowdfunding_ETL_ERD](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/078925d6-580c-4390-9702-43459c9e4bd5)

### **Campaign Table** ###
![Campaign_table_data_screenshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/7c9a37e2-1d78-46ad-a9d6-9025f2465a90)

### **Contacts Table** ###
![Contact_table_data_screnshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/648f6ba0-0e73-497c-aa43-e91193e9d43e)

### **Category Table** ###
![Category_table_data_screenshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/6e415dd1-9e39-4717-a842-2fa667fe5b00)

### **Subcategory Table** ###
![Subcategory_table_data_screenshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/155a5c44-d060-47c0-bd85-cf5fbc25e726)
