# DataQ Accelerator
Easily Implemented Big Data Profiling And Data Quality Tool
![summary](https://github.com/ashu1979/dataq_accelerator/blob/main/images/DataQ%20%20summary.jpg?raw=true)


## Pre-requisites
1) Requires adding both deequ spark jar, and pydeequ librarys to Databricks cluster. You can find the library to install in lib folder of this repository
[how to add a library to a databricks cluster](https://docs.microsoft.com/en-us/azure/databricks/libraries/cluster-libraries)



2) Connection to Azure Data Lake Storage using security and/or connection to a SQL Database
[how to connect to ADLS Gen2 from databricks](https://docs.databricks.com/data/data-sources/azure/azure-datalake-gen2.html)
[Mounting & accessing ADLS Gen2 in Azure Databricks using Service Principal and Secret Scopes](https://towardsdatascience.com/mounting-accessing-adls-gen2-in-azure-databricks-using-service-principal-and-secret-scopes-96e5c3d6008b)


## Inputs
![Just add required input params at top of notebook](https://github.com/ashu1979/dataq_accelerator/blob/main/images/Inputs.jpg?raw=true)

Then run the notebook!

## Outputs
Detailed profiles of the data and suggested constraints in either file or database.
Profiles currently implemented:

 Markup : - Column (name)
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






