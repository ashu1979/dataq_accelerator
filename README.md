# DataQ Accelerator
Easily Implemented Big Data Profiling And Data Quality Tool
DataQ accelerator is a Notebook solution which helps to perform data profiling, constraints suggestions and constraints validations on data stored in Azure Data Lake Store Gen2. DataQ accelerator works well with CSV and Parquet file format to perform data quality operations and validations. 
DataQ notebook implements and automates an open source Deequ library. It is spark library under Apache 2.0 license developed by Amazon AWS.

![summary](https://github.com/ashu1979/dataq_accelerator/blob/main/images/DataQ%20%20summary.jpg?raw=true)

There are mainly 2 notebooks created to perform profiling and constraint validation separately:
<b>Data Quality Accelerator,<\b> notebook gets the profile information, it runs the profile in one pass on your specified dataset and does not repeat. This notebook also get additional information for numeric data e.g. min, max, mean, stdDev etc. as part of the output. Along with profile information, it also helps to identify the constraints which can be applied to your dataset to improve the quality of data and ensure consistency and reliability. 
<b>Data Quality Validator,<\b> notebook helps to perform validation on your dataset columns to validate against constraints. It reports the constraint status along with message which shows unsupported value found in a particular column.

## Pre-requisites
1) Requires adding both deequ spark jar, and pydeequ librarys to Databricks cluster. You can find the library to install in lib folder of this repository
[how to add a library to a databricks cluster](https://docs.microsoft.com/en-us/azure/databricks/libraries/cluster-libraries)


2) Connection to Azure Data Lake Storage using security and/or connection to a SQL Database
[how to connect to ADLS Gen2 from databricks](https://docs.databricks.com/data/data-sources/azure/azure-datalake-gen2.html)
It is recommended to use Azure Key Vault to store the ADLS identity and secrets and use Azure Databricks service principle to securely access the ADLS account without specifying the secret as part of the notebook:
[Mounting & accessing ADLS Gen2 in Azure Databricks using Service Principal and Secret Scopes](https://towardsdatascience.com/mounting-accessing-adls-gen2-in-azure-databricks-using-service-principal-and-secret-scopes-96e5c3d6008b)


## Inputs
Just add required input params at top of notebook:

![Just add required input params at top of notebook](https://github.com/ashu1979/dataq_accelerator/blob/main/images/Inputs.jpg?raw=true)

Please note, it does accept CSV and Parquet file formats only. You can either specify single file path or a folder containing the various files with same format and structure.

Then run the notebook!

## Outputs
Detailed profiles of the data and suggested constraints in either file or database.
Profiles currently implemented:

 - Column (name)
 - completeness
 - approx distinct
 - datatype
 - minimum
 - maximum
 - mean
 - stdDev
 - instance
 - ApproxQuantile-0.5
 - Distinctness
 - Entropy
 - Histogram.abs.Boolean
 - Histogram.abs.Fractional
 - Histogram.abs.Integral
 - Histogram.abs.String
 - Histogram.abs.Unknown
 - Histogram.bins
 - Histogram.ratio.Boolean
 - Histogram.ratio.Fractional
 - Histogram.ratio.Integral
 - Histogram.ratio.String
 - Histogram.ratio.Unknown
 - MaxLength
 - MinLength
 - Size
 - filename_path
 - timestamp
 - profile_date

