## 📂 Project Structure
```bash
aaws-lambda-rekognition-imagetotext/
 ├── README.md              # Project documentation
 ├── diagram.png            # Architecture diagram
 ├── screenshots/           # AWS Console screenshots
 │    ├── s3-upload.png     # Uploaded image in S3 bucket
 │    ├── cloudwatch-log.png # Lambda execution log in CloudWatch
 │    ├── json-output.png   # Extracted text in JSON format
 └── lambda_function.py     # AWS Lambda function code

```
# 🚀 Serverless Image-to-Text with AWS Lambda and Rekognition

## 🎯 Goal
Automatically extract text from images uploaded to an S3 bucket using Amazon Rekognition, with a serverless architecture powered by AWS Lambda.

## 🛠 AWS Services Used
- Amazon S3 (for image storage)
- AWS Lambda (event-driven function)
- Amazon Rekognition (text detection in images)
- Amazon CloudWatch (logs and monitoring)
- AWS IAM (roles and permissions)

## 📷 Screenshots

### 1. Uploading Image to S3
![S3 Upload](screenshots/s3-upload.jpeg)

### 2. Lambda Execution Log (CloudWatch)
![CloudWatch Log](screenshots/cloudwatch-log.jpeg)

### 3. Extracted JSON Output
![JSON Output](screenshots/json-output.jpeg)


## 📌 Architecture
1. A user uploads an image (`.jpg` or `.png`) to the **rekognition-image-input** S3 bucket.
2. The S3 event triggers the **rekognition-image-to-text** Lambda function.
3. Lambda calls **Rekognition DetectText API** to extract text from the image.
4. The detected text is saved back into the same bucket as a `.json` file.
5. CloudWatch logs show the detected text for validation.

## 🎨 Architecture Diagram
![Architecture](diagram.jpeg)

