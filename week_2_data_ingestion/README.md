# Data Ingestion

## Data Lake

Un Data Lake est un endroit où on stocke de nombreuses données venant de plusieurs sources de données. On les utilise aussi bien pour du Machine Learning que des applications Analytics. Un Data Lake doit être sécurisé et on veut avoir accès à ces données le plus rapidement possible. 

![Datalake](images/data_lake.png)

### Data Lake vs Data Warehouse

Dans un data lake les données ne sont pas structurées. Les usagers sont des data scientists ou des data analysts. Le nombre de données présentés sont importants (de l'ordre du Pétaoctet). Dans un data warehouse, les données sont structurées. Les utilisateurs sont des data analysts et les données sont moins importantes à l'intérieur. 

![DatalakeVsDataWarehouse](images/dl_vs_dw.png)

### Data Lake et Cloud Providers

Selon le cloud provider, le Data Lake se fera avec différents services : 
- **S3** pour **AWS**
- **Azure Blob** pour **Azure**
- **Cloud Storage** pour **GCP**

## Orchestration d'un workflow d'ingestion

*Source :* [Repo GitHub](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/week_2_data_ingestion)

