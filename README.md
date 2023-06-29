# 🚀 Azure_Databricks_project
Data Source: www.ergast.com/mrd 


#### Entity Relationship Model of Data Source
![Data model](http://ergast.com/images/ergast_db.png)


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

  
      


