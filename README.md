# 📈 Real-Time Stock Market Data Pipeline using Kafka & AWS ☁️

This project demonstrates an end-to-end real-time data engineering pipeline for streaming and analyzing stock market data using **Apache Kafka** and **AWS services** including EC2, S3, Glue, and Athena.

---

## 🧠 Project Overview

- Simulate stock market data from a CSV file using Python.
- Stream data in real time using **Kafka Producer** to a **Kafka server hosted on EC2**.
- Consume data from Kafka, convert to **Pandas DataFrame**, save as CSV, and upload to **Amazon S3**.
- Use **AWS Glue Crawlers** to catalog the data automatically.
- Query the real-time data using **Amazon Athena**.

---

## 📌 Architecture

![Architecture Diagram](./Architecture.jpg)  <!-- Replace with actual image path if hosted -->

---

## 🛠️ Tech Stack

- **Apache Kafka** – Real-time data streaming
- **Python** – Producer & Consumer scripting
- **Pandas** – DataFrame handling
- **Amazon EC2** – Kafka server hosting
- **Amazon S3** – Scalable storage for CSVs
- **AWS Glue** – Data cataloging
- **Amazon Athena** – Serverless querying
- **s3fs** / **boto3** – Python S3 interaction

---

## ⚙️ How It Works

1. 📊 **Kafka Producer** reads stock data from CSV and sends each record as a JSON message to Kafka.
2. 🛰️ **Kafka Consumer** receives messages, converts them into a DataFrame, and writes to CSV.
3. ☁️ The CSV is uploaded to an S3 bucket.
4. 🔄 **AWS Glue Crawler** scans the S3 data and creates/update the Data Catalog.
5. 🔍 **Amazon Athena** enables SQL-based querying on the structured data.

---

## 🚀 Setup Instructions

> ⚠️ Replace placeholders like `<your-ip>` or `<bucket-name>` with actual values in the code.

1. Set up a Kafka server on EC2 and allow inbound ports (e.g., 9092).
2. Configure `KafkaProducer.ipynb` to:
   - Load stock CSV
   - Set correct Kafka broker IP
   - Send data to a topic
3. Configure `KafkaConsumer.ipynb` to:
   - Connect to same topic
   - Convert messages to DataFrame
   - Upload to S3 using `s3fs`
4. Create AWS Glue Crawler and connect it to the S3 bucket.
5. Use Athena to query data in SQL.

---

## 📚 Key Learnings

- Real-time data ingestion using Apache Kafka
- Transforming streamed data before cloud storage
- Serverless data cataloging & querying using AWS Glue and Athena
- Orchestrating multiple cloud services in a real-world pipeline

---

## 📎 Related Files

- `KafkaProducer.ipynb` – Simulates and sends data to Kafka
- `KafkaConsumer.ipynb` – Consumes, transforms, and stores data in S3

---

## ✨ Author

**Muhammad Hamza**  
[LinkedIn](https://www.linkedin.com/in/-muhammad-hamza/)

---

## 🏁 License

MIT License – feel free to use and adapt!
