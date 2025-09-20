# Project-Tittle-1-ETL-Data-Engineering-Pipeline-USGS-Earthquake-Data
 Ingested earthquake event data from the US Geological Survey (USGS) API for daily intervals and stored raw JSON files in the
 Bronze layer (Azure Data Lake Storage– ADLS).
 
 Developed and executed transformations in Azure Databricks (PySpark) for Silver layer:
 o Flattenednested JSON fields (geometry.coordinates, properties.*).
 o Enforcedschemawithdata type casting for accuracy.
 o Handlednullvalues (defaulted numeric fields to 0).
 o Removedinvalid/mismatched values (lat/lon, mag, sig, elevation).
 o Deduplicated records, keeping the latest per id using the updated timestamp.
 
 Curated Gold layer datasets in Azure Databricks with advanced transformations:
 o Geo-enrichment: Derived country_code from latitude & longitude using reverse geocoding.
 o Businessclassification: Categorized earthquake significance (Low, Moderate, High) based on sig value.
 o Datapersistence: Stored curated outputs in Parquet (analytics-ready) and CSV (reporting/consumption) formats in
 ADLS.
 
 Skills used: Azure Data Lake Storage (ADLS), Azure Databricks, PySpark, Delta Lake, APIs, Parquet/CSV
