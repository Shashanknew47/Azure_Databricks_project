# 🚀 Formula 1 Race Project 
Data Source: www.ergast.com/mrd 


#### Entity Relationship Model of Data Source
![Data model](https://github.com/Shashanknew47/Azure_Databricks_project/blob/master/Screentshots/Data_model.png)


# Project Requirement:
 1) **Ingestion**: ingest all the data into `raw` container from source.
 2) **Transformation** :
    - Apply appropriate schemas
    - Do appropriate cleaning and Transformation
    - Optimize by appropriate file formats and partition pruning.  
    - Covert all the files into Parquet format and loaded into `tran` container.
  3) **Presentation**:
      - Make its data ready for the presentation layer So, that  BI team can  :
         1) produce driver standing as well as constructor standing for the current race from 1950 to the current year.
         2) Find out the most dominant driver and dominant teams over the last decade.
         3) Rank drivers and teams in order of dominance.
         4) Create dashboards on these performance parameters.
         5) Able to see the history of the data and the ability to query the data based on time. 
      

      -  Apply appropriate transformations like Join, and Aggregate functions etc.
      -  Us `Delta` format to load in the `Presentation` container. :
         1)  Make it an appropriate transformation to handle `incremental data`.
         2)  Make a  test to check if different versions are available.
       
  4) **Automation**
     - Create an automated pipeline in `Azure Datafacroty` which will run every Sunday at 10a.m. to automate the whole pipeline. 
       
  5) **Apply best practices**; 
      - Make sure all the  secrets must be stored in `Azure Key Vault` and no key should be visible 
      - Use `Azrue service principal` for access control and make sure to provide granular  required accesses only. 
  
            
# Project Architecture:
   1) Created Storage account `formularacedata`.
   2) Created 3 containers in `formularacedata` account.
       - Raw
       - Processed
       - Presentation
   3) Created Service principal and provide 'read and list' permission
   4) Store service principal credentials in `Azure Key Vault`.
   5) Mount all these containers in `Azure Databricks workspace`.
   6) Collected all the raw data in `raw` container.
   7) Process the data 'raw data' and optimize it with 'partition pruning' and 'run lenght length encoding'
   8) Prepare the data in  `Delta Lake` format and created tables in 2 databases. So, that BI team can access this data for further analysis.
         - f1_processes
         - f1_presentation
    
   

  
      


