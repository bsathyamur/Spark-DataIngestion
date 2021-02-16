# Guided capstone project for data ingestion via spark

# Project details:
Spring Capital data sources come from stock exchange daily submissions files in a semi-structured text format. This means the records follow a certain formatting convention like JSON, but don’t obey a tabular structure formatted for a relational database. The data ingestion process parses the semi-structured data out so it can be loaded into Spark.

# Environment setup:
1. Used azcopy (10.8.0) to copy the local files from local system to the azure blob container
2. spark-3.0.01
3. Java JDK 15.0.2
4. azure-storage-3.0.0.jar and hadoop-azure-2.7.4.jar

The JAR files are copied into the JAR folder into spark-3.0.1-bin-hadoop2.7\jars

# Description
The pyspark program will get the list of files from the blob container and parse the csv and json files according to the custom schema defined and write the data from the data frame into the partitions (T- Trade, Q-Quote and B-Bad records) in the output_dir folder in the blob container
