# 📦 AWS S3 Metadata Extraction Tool

## 📌 Overview
Python-based tool to retrieve detailed AWS S3 object metadata as a cost-effective alternative to S3 Inventory.  
Developed during HMSA migration to efficiently analyze and track large-scale S3 data.

---

## 🚀 Features
- Extracts S3 object metadata (size, last modified, storage class, ETag)
- Retrieves security details (encryption, replication status, bucket key)
- Optional extraction of:
  - ACL details  
  - Object Lock (retention & legal hold)  
- Handles large buckets using pagination  
- Exports data to **CSV** or **Excel**  
- Cost-optimized alternative to AWS S3 Inventory  

---

## 🛠️ Tech Stack
- Python  
- boto3 (AWS SDK)  
- pandas  

---

## ⚙️ Prerequisites
- Python 3.x  
- AWS CLI configured (`aws configure`)  

### Required IAM Permissions:
- s3:ListBucket  
- s3:GetObject  
- s3:GetObjectAcl  
- s3:GetObjectRetention  
- s3:GetObjectLegalHold  

---

## ▶️ Installation

pip install boto3 pandas

## 📊 Output
The script generates a file containing:
- Object Key  
- Size  
- Last Modified  
- Storage Class  
- Encryption  
- Replication Status  
- ACL (optional)  
- Object Lock details (optional)

## 💡 Use Case
This tool was designed and implemented during a cloud migration to:

- Efficiently list and analyze S3 objects  
- Replace AWS S3 Inventory for cost optimization  
- Support auditing and compliance requirements  

---

## ⚠️ Notes
- Enabling `--include-acl` and `--include-lock` may increase execution time  
- Suitable for large-scale buckets using pagination  

---

## 🔗 Future Enhancements
- Multi-threading for faster processing  
- Config file support (YAML/JSON)  
- Docker containerization  
- CLI packaging

---
##👩‍💻 Author

Mounika Puppala
