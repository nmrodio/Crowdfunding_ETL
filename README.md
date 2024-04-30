# **Crowdfunding_ETL** #

This repository contains the code for an ETL (Extract, Tranform, and Load) pipeline. The pipeline is used to upload, clean, and reproduce crowdfunding data from excel files into csv dataframes and a crowdfunding database. The original excel crowdfunding information has data that is difficult to sift through. The categories and sub-categories decribing the crowdfunding projects are combined into a single column, making it difficult to filter through project categories. The project launch and funding deadline columns are named incorrectly and not set to date time data types. There are also extra columns that are not useful as well as column names that needed to be changed for clarity.
The excel file containing the contact information of crowdfunding campaigns is also poorly structured, with all the data existing in a single column, instead of being seperated by id, first name, and last name.

The code in this repository makes changes to these excel files, reorganizing and cleaning data as necessary as well as creating two new dataframes to reference the categories and subcategories of the projects.
The code also uses list comprehension methods to seperate the contact information into seperate columns. 
After making thesetransformations to the files, the new dataframes are uploaded as csvs. 

Also included in the Resources folder of this repository is an Entity-Relationship Diagram (ERD) visualizing the relationship between each table (each CSV file).
Finally, all of the data is loaded into an SQL Schema for future analysis.

## **Crowdfunding DB Table Data** ##
* A select * was ran on each table to ensure that each table's respective data was imported correctly from the CSV files

### *Campaign Table* ###
![Campaign_table_data_screenshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/7c9a37e2-1d78-46ad-a9d6-9025f2465a90)

### *Contacts Table* ###
![Contact_table_data_screnshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/648f6ba0-0e73-497c-aa43-e91193e9d43e)

### *Category Table* ###
![Category_table_data_screenshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/6e415dd1-9e39-4717-a842-2fa667fe5b00)

### *Subcategory Table* ###
![Subcategory_table_data_screenshot](https://github.com/nmrodio/Crowdfunding_ETL/assets/157527614/155a5c44-d060-47c0-bd85-cf5fbc25e726)
