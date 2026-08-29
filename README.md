## Project Demonstration

### Azure Data Factory Pipeline

The `incre_ingest` pipeline uses a metadata-driven loop to ingest Spotify music data dynamically. It reads JSON source files from Azure Data Lake Storage and loads curated outputs into Parquet files and Azure SQL Database.

![ADF Pipeline Overview](assets/screenshots/01-adf-pipeline-overview.png)

### Dynamic File Processing

The pipeline uses parameterized datasets and a `ForEach` activity so that multiple input files can be ingested without duplicating pipeline logic.

![Dynamic ForEach Configuration](assets/screenshots/02-foreach-dynamic-loop.png)

![Dynamic Dataset Parameters](assets/screenshots/04-dynamic-dataset-parameters.png)

### Successful Pipeline Execution

A successful ADF run confirms that the ingestion workflow completed and the copy activities processed the configured input files.

![Pipeline Monitoring Success](assets/screenshots/05-pipeline-success-monitoring.png)

### Data Output

The ingested data is persisted as Parquet in Azure Data Lake Storage and can be loaded into Azure SQL Database for querying and reporting.

![ADLS Parquet Output](assets/screenshots/06-adls-parquet-output.png)

![Azure SQL Output](assets/screenshots/07-azure-sql-output.png)
