# Big Data

## Background
Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. However, they are quite large and can exceed the capacity of local machines to handle. One dataset alone contains over 1.5 million rows; with over 40 datasets, this can be quite taxing on the average local computer. The goal was to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. 

DataFrames were created to match production-ready tables from two big Amazon customer review datasets:
- Automotive Reviews
- Kitchen Reviews

## Summary
The furnished schema (see resources) was used to create tables in the RDS database.
Two separate Google Colab notebooks were created to extract the two chosen datasets from the list; one into each notebook.
Note: It is possible to ETL both data sources in a single notebook, but due to the large data sizes, it was easier to work with these S3 data sources in two separate Colab notebooks.

For each notebook (one dataset per notebook), the following was completed:
- Counted the number of records (rows) in the dataset.
- Transformed the dataset to fit the tables in the schema file. Also ensuring the DataFrames match in data type and in column name.
- Loaded the DataFrames that correspond to tables into an RDS instance; whilest noting that this process can take up to some time, thus ensuring that everything was correct before uploading.
