# Step By Step Prompt & Response

- Refer the image attached and provide ddl statement as per the diagram.
- make the dev & qa database transient and have the production database as 7 days time travel. Also suggest why 7 days time travel is good, is this a best practice?
- Execute the DDL statements to create DEV/QA/PROD databases with transient and time travel settings


2nd Prompt
I would like one modification in the database names, don't use the prefix APPLE and just have it sales_dev, sales_qa and sales_prod.

sate promopt
Now perform following set of operations only in sales_dev database.
Create an internal stage inside the bronze layer including the comment where I would upload the sales analytics csv files.

Now the stage location has got csv files, go under customer-master sub-folder, check all the 4 csv files and load them in the bronze layer. The 1st line of each csv file is a header and before loadaing these csv files, create the table that matches the csv header, remove any space or special character from the header for column name use, also pick the most appropriate data type whilc creating tables. Add 3 additional audit columns based on the stage location like __file_name, __row_number and __load_st using stage location metadata. Make sure give short and meaningful table descriptions and column descrition.
use the file formate created inside the common schema or feel free to use infer schema to solve the problem)

Now we are done with country master, lets do the same for initial-load/product-master csv file, it has total 5 csv files for product data, do the same what is done for country master.

Now we are done with product master, lets do the same for initial-load/store-master csv file, it has total 5 csv files for store data, do the same what is done for product master.

Now we are done with store master, lets do the same for initial-load/customer-master csv file, it has total 1 csv file for customer data, do the same what is done for store master.

Now we are done with customer master, lets do the same for initial-load/sales-master csv file, it has total 2 csv files for sales data, do the same what is done for customer master.

## Silver Layer + Dynamic Tables

Next, we have to move data from bronze layer to silver layer using dynamic table approach as referred in our architectural diagram instruction and we will start with one table at a time. So lets start with region master table. 
Bronze layer tables may have duplicate records as copy command does not validate it, hence understand the entity domain and check duplicate records, also add column/record level quality check if necessary. Dynamic table shoudl have downstream lag and incremental approach. Do we need stream object in bronze layer or not, please propose an optimal solution to save cost





