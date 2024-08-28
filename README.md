# ETL_of_Cricket_Statistics

This project focuses on making a Data Engineering pipeline on **GCP** using its tools and services. The pipeline automates the extraction, transformation, and loading (ETL) of cricket match data into a structured format suitable for analysis.

## Key Features:

Data Extraction: Utilizes web scraping techniques using **Python** and **Cricbuzz API** to gather cricket match statistics from various online sources.
Data Transformation: When the API gives response, that data is then transformed using **Python** and only the relevant data is stored to a local csv file. 
Data Loading: This csv file is then uploaded to a **Cloud Storage bucket**. As soon as the file is loaded in bucket it triggers a **Cloud Function** operations which the starts a **DataFlow** job. The output of this job is stored in **BigQuery**.
This whole process is automated using **Cloud Composer** were a dag python file is used to execute the python file which will collect the data.
