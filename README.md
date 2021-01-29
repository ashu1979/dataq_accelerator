# DataQ Accelerator
Easily Implemented Big Data Profiling And Data Quality Tool

## Pre-requisites
1) Requires adding both deequ spark jar, and pydeequ librarys to Databricks cluster. You can find the library to install in lib folder of this repository
[how to add a library to a databricks cluster](https://docs.microsoft.com/en-us/azure/databricks/libraries/cluster-libraries)



2) Connection to Azure Data Lake Storage using security and/or connection to a SQL Database
[how to connect to ADLS Gen2 from databricks](https://docs.databricks.com/data/data-sources/azure/azure-datalake-gen2.html)
[Mounting & accessing ADLS Gen2 in Azure Databricks using Service Principal and Secret Scopes](https://towardsdatascience.com/mounting-accessing-adls-gen2-in-azure-databricks-using-service-principal-and-secret-scopes-96e5c3d6008b)


## Inputs
Input file or folder and Output file or folder, format csv or parquet


## Outputs
Detailed profiles of the data and suggested constraints in either file or database.

## 
![summary](https://github.com/ashu1979/dataq_accelerator/blob/main/images/DataQ%20%20summary.jpg?raw=true)
![notebook](https://github.com/ashu1979/dataq_accelerator/blob/main/images/solution%20implementation.jpg?raw=true)



