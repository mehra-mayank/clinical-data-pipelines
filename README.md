

**SCD Type 1**

1. Source – scd\_upsert in 
1. Source schema – test/dbo. Server – w3.devsql.modak.com:1433
1. Destination – test\_dbo\_scd\_upsert
1. Destination schema – hive\_data, server – w3.cdhnode1.modak.com

**SCD Type 2**

1. Source – scd\_type2
1. Source schema – test/dbo. Server – w3.devsql.modak.com:1433
1. Destination – test\_dbo\_scd\_type2
1. Destination schema – hive\_data, server – w3.cdhnode1.modak.com

**Incremental Load**

1. Source – incremental\_load
1. Source schema – test/sales. Server – w3.devsql.modak.com:1433
1. Destination – test\_sales\_incremental\_load
1. Destination schema – hive\_data, server – w3.cdhnode1.modak.com

**File Ingestion**

1. Source bucket– nabuingestion
1. Source directory – Data\_Ingest
1. Destination – test\_sales\_incremental\_load
1. Destination schema – hive\_data, server – w3.cdhnode1.modak.com

Schedule crawling before ingestion (after uploading file)

**File Copy**

1. Source bucket– nabuingestion
1. Source directory – Data\_Ingest
1. Destination – nabuingestion
1. Destination directory – Ingested\_tables/Data\_Ingest/

Schedule crawling before ingestion (after uploading file)

Check monitoring dashboard for pipeline objects

**Swagger API**

1. Pipeline\_id: 4414
1. Pipeline\_name: Swagger\_ingestion


**DQ Active Rule**

1. Pipeline name: DQ Active 1
1. Source: dev postgres, source\_db/public, product\_patents

**DQ Passive Rule**

1. Pipeline name: DQ Passive test
1. Check for rule prod\_pat\_id
1. Run pipeline using schedule option
1. Source: dev postgres, source\_db/public, product\_patents


**For creating bug with REST API**

1. Create Bug on failure\_REST API
1. Source: dev postgres, source\_db/public, dq\_test

**For System Variables**

1. System Variables test
1. Source: Amazon S3, Buckets: gratis-bucket-test mt4010/system\_variables\_test.csv
1. Destination: [Amazon S3](https://s3.console.aws.amazon.com/s3/get-started?region=us-west-2), [Buckets](https://s3.console.aws.amazon.com/s3/buckets?region=us-west-2), [nabuingestion](https://s3.console.aws.amazon.com/s3/buckets/nabuingestion), [testing/](https://s3.console.aws.amazon.com/s3/buckets/nabuingestion?prefix=testing/), [system_variables_test/](https://s3.console.aws.amazon.com/s3/buckets/nabuingestion?prefix=testing/system_variables_test/)


**For ingestion using hash partitions**

1. Without hash partitions\_assay\_parameters
1. With hash partitions\_assay\_parameters
1. Without hash partitions\_compound\_structural\_alerts
1. With hash partitions\_compound\_structural\_alerts

