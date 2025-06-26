🕷️ AWS Glue Crawler Configuration

Follow these steps to crawl your S3 stock data and make it queryable in Athena:

Go to AWS Glue Console

https://console.aws.amazon.com/glue/

Create Database

Go to Databases → Add Database

Name: stock_data_db

Create a Crawler

Go to Crawlers → Add Crawler

Name: stock_data_crawler

Data Store: S3

Path: s3://stock-data-bucket/streamed/

Add another data store: No

IAM Role

Use existing role with AWSGlueServiceRole permissions, or create a new one

Output

Choose the database stock_data_db

Table name will be auto-generated from data

Run the Crawler

After setup, run the crawler

It will scan the S3 path and add the table to Glue Catalog

Verify

Go to Tables → check if table appears with correct schema

You can now query this using Athena
