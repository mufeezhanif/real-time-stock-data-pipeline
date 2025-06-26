

🪣 S3 Bucket Setup Instructions

Follow these steps to set up your Amazon S3 bucket for the real-time stock data pipeline:

Log in to AWS Console

Go to https://console.aws.amazon.com/s3/

Create a Bucket

Click Create bucket

Bucket name: stock-data-bucket (or a name of your choice)

Region: Choose same region as Glue/Athena (e.g., us-east-1)

Uncheck Block All Public Access (optional)

For development/testing purposes only

Enable Versioning (optional)

Recommended for data tracking

Create the Bucket

Folder Structure (Optional)

Inside the bucket, create a folder such as /streamed/ where the consumer writes files

Permissions

Ensure the EC2 instance (or user uploading files) has PutObject permission
