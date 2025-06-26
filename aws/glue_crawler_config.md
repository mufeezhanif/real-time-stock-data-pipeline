# 🕷️ AWS Glue Crawler Configuration

Follow these steps to crawl your S3 stock data and make it queryable in Athena:

---

## 🔗 Access AWS Glue Console
- [Go to AWS Glue Console](https://console.aws.amazon.com/glue/)

---

## 🗃️ Create Database
1. Go to **Databases** → **Add Database**
2. **Name**: `stock_data_db`

---

## 🛠️ Create a Crawler
1. Go to **Crawlers** → **Add Crawler**
2. **Name**: `stock_data_crawler`
3. **Data Store**: `S3`
4. **Path**: `s3://stock-data-bucket/streamed/`
5. **Add another data store**: `No`

---

## 🔐 IAM Role
- Use existing role with `AWSGlueServiceRole` permissions
- Or create a new one during the setup

---

## 📥 Output
- Choose the database: `stock_data_db`
- Table name will be auto-generated from the dataset

---

## ▶️ Run the Crawler
- After completing the setup, **run the crawler**
- It will scan the provided S3 path and add the table to the Glue Catalog

---

## ✅ Verify Table
- Go to **Tables** in AWS Glue
- Check if the table appears with correct schema
- You can now query the data using **Amazon Athena**
