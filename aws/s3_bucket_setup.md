# 🪣 S3 Bucket Setup Instructions

Follow these steps to set up your Amazon S3 bucket for the real-time stock data pipeline:

---

## 🔗 Log in to AWS Console
- [Go to AWS S3 Console](https://console.aws.amazon.com/s3/)

---

## 🪣 Create a Bucket

1. Click **Create bucket**
2. **Bucket name**: `stock-data-bucket` *(or a name of your choice)*
3. **Region**: Choose the same region as Glue/Athena (e.g., `us-east-1`)

---

## 🔓 Public Access (Optional)

- Uncheck **Block All Public Access** *(only for development/testing)*

---

## 🗂️ Enable Versioning (Optional)

- Enable this to track object changes over time (recommended)

---

## ✅ Finalize Bucket

- Click **Create bucket** to finish setup

---

## 📁 Folder Structure (Optional)

- Inside the bucket, create a folder: `/streamed/`
  - This is where the Kafka consumer will write the data files

---

## 🔐 Permissions

- Ensure the EC2 instance or IAM user that writes to S3 has the `PutObject` permission
