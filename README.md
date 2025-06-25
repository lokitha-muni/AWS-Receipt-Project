# 🧾 Serverless Receipt Scanner – Powered by AWS

This project showcases a serverless backend solution that automates receipt processing using several AWS services. It demonstrates how cloud-native tools can be used to build an event-driven, real-world workflow from scratch.

---

## 📌 What It Does

When a user uploads a receipt image to an S3 bucket:
- ✅ **AWS Lambda** is triggered
- 🧠 **Amazon Textract** extracts key information like:
  - Vendor name
  - Purchase date
  - Total amount
  - Line items
- 💾 The extracted data is saved to **Amazon DynamoDB**
- 📧 A clean, structured summary of the receipt is emailed to the user using **Amazon SES**

---

## 🧱 Architecture Diagram

![Screenshot 2025-06-25 114417](https://github.com/user-attachments/assets/b7c96a88-7fd1-43ad-8a8b-2cec804dfa9c)

*The user uploads the receipt to S3.*

*After a receipt is uploaded to S3, the trigger invokes the Lambda function.*

*Lambda invokes Amazon Textract for data extraction from the receipts.*

*Amazon Textract returns a structured data to Lambda.*

*Lambda stores the processed data from Amazon Textract to the DynamoDB table.*

*Lambda uses Amazon SES to send email notifications.*

---

**## 🖼️ Screenshots**

![Screenshot 2025-06-16 195611](https://github.com/user-attachments/assets/2404bc0e-edba-42ad-bacf-31eaa792e19e)

## 🎯 Key Learnings

- Gained hands-on experience with **serverless architecture** using AWS services.
- Learned how to build **event-driven workflows** triggered by S3 uploads.
- Understood how to use **Amazon Textract** to extract structured data from unstructured receipt images.
- Practiced integrating multiple AWS tools (Lambda, S3, Textract, DynamoDB, SES) into a **cohesive automation pipeline**.
- Improved skills in handling **real-world data processing scenarios** using cloud-native approaches.

---

## 🛠️ Tech Stack

- **AWS Lambda** – Executes backend logic and orchestration.
- **Amazon S3** – Stores user-uploaded receipt images.
- **Amazon Textract** – Extracts text and key data from receipts.
- **Amazon DynamoDB** – Stores extracted, structured data.
- **Amazon SES** – Sends the structured receipt summary to the user via email.
- **Python** – Programming language used for Lambda functions.

