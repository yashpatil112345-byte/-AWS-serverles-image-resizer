🖼️ Serverless Image Resizer

Event-Driven Image Processing with AWS Lambda, Amazon S3 & Pillow

A serverless, event-driven image processing application that automatically resizes images uploaded to Amazon S3.

When a user uploads an image through the web interface, the image is stored in an Amazon S3 input bucket. An S3 event automatically triggers an AWS Lambda function, which uses Python, Boto3, and Pillow to resize the image and store the processed version in a separate S3 output bucket.

The project demonstrates how AWS serverless services can be combined to build an automated, scalable, and cost-efficient image processing workflow without managing servers.

✨ Features

📤 Upload images through a web interface

⚡ Automatically process images using AWS Lambda

☁️ Event-driven processing with Amazon S3

🐍 Image processing using Python and Pillow

🔄 Automatically resize uploaded images

📦 Store original and processed images separately

⬇️ Download processed images

🔐 Use IAM roles for AWS resource permissions

🌐 Responsive frontend interface

🖥️ Completely serverless backend architecture

🏗️ Architecture

                         ┌──────────────────┐
                         │       User       │
                         └────────┬─────────┘
                                  │
                                  ▼
                    ┌─────────────────────────┐
                    │    Web Application      │
                    │ HTML / CSS / JavaScript │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │     Amazon S3           │
                    │     Input Bucket        │
                    └────────────┬────────────┘
                                 │
                         S3 Object Event
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │      AWS Lambda         │
                    │     Python + Boto3      │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │       Pillow            │
                    │   Image Processing      │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │     Amazon S3            │
                    │     Output Bucket       │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Download Processed     │
                    │        Image            │
                    └─────────────────────────┘

☁️ AWS Services Used

AWS Service

Purpose

Amazon S3

Stores uploaded and resized images

AWS Lambda

Executes the image processing logic

AWS IAM

Provides secure permissions to AWS resources

🛠️ Technologies Used

Technology

Purpose

Python

Lambda image-processing logic

Boto3

Python SDK for AWS

Pillow

Image resizing and processing

HTML5

Frontend structure

CSS3

Frontend styling

JavaScript

Frontend functionality

Git & GitHub

Version control and project hosting

🔄 How the Project Works

1. Upload an Image

The user selects an image from the web application.

2. Store the Original Image

The image is uploaded to the Amazon S3 Input Bucket.

3. Trigger Lambda Automatically

Amazon S3 generates an event when a new image is uploaded. This event invokes the AWS Lambda function.

4. Process the Image

Lambda retrieves the uploaded image and uses Pillow to resize it.

5. Store the Processed Image

The resized image is saved in a separate Amazon S3 Output Bucket.

6. Download the Result

The processed image can then be accessed and downloaded by the user.

📁 Project Structure

serverless-image-resizer/
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── lambda/
│   ├── lambda_function.py
│   └── requirements.txt
│
└── README.md

Frontend

Contains the user interface used to upload images and access processed results.

Lambda

Contains the Python-based AWS Lambda function and its dependencies.

🔐 Security

Security is an important part of the architecture.

🔑 IAM roles are used to provide Lambda with required AWS permissions.

🚫 AWS Access Keys and Secret Keys are not stored in the source code.

☁️ AWS services communicate through configured IAM permissions.

⚡ Lambda is triggered automatically by S3 events.

📦 Input and output images are separated into different S3 buckets.

Important: Never commit AWS credentials, .env files, private keys, or other secrets to GitHub.

📸 Project Screenshots

🏠 Home Page

<img width="1296" height="663" alt="Home Page" src="https://github.com/user-attachments/assets/557de051-d870-4733-bc8f-493243d38fc4" />

📤 Upload Image

<img width="1336" height="702" alt="Upload Image" src="https://github.com/user-attachments/assets/b71baf04-577e-4c51-beee-bd378f86c8f8" />

🖼️ Processed Image Output

<img width="1552" height="791" alt="Processed Image Output" src="https://github.com/user-attachments/assets/96c7c965-2166-4e3f-af18-fa7502722975" />

⚡ AWS Lambda Trigger

<img width="1575" height="767" alt="AWS Lambda Trigger" src="https://github.com/user-attachments/assets/fec2d143-95fc-4b82-87c6-e136d9ffe4b2" />

🔧 Lambda Configuration

<img width="1335" height="722" alt="Lambda Configuration" src="https://github.com/user-attachments/assets/bfe1dda1-234d-4b76-8f8f-6521fe30a28c" />

☁️ Resized Image in Output Bucket

<img width="1817" height="862" alt="Resized Image in Output Bucket" src="https://github.com/user-attachments/assets/03cefa45-1d95-4acc-9334-646123e0de99" />

🚀 Deployment Overview

The application can be deployed using the following high-level process:

1. Create an Amazon S3 Input Bucket
              ↓
2. Create an Amazon S3 Output Bucket
              ↓
3. Create an AWS Lambda Function
              ↓
4. Configure Pillow and Boto3
              ↓
5. Configure the Lambda IAM Role
              ↓
6. Configure the S3 Event Notification
              ↓
7. Upload the Frontend
              ↓
8. Test Image Upload
              ↓
9. Verify Lambda Processing
              ↓
10. Check the Output Bucket

🧪 Example Workflow

User uploads image
        ↓
Input S3 Bucket
        ↓
S3 Event Notification
        ↓
AWS Lambda
        ↓
Pillow resizes image
        ↓
Output S3 Bucket
        ↓
Processed image available

📈 Future Enhancements

The project can be extended with:

🎚️ Multiple image size options

🗜️ Image compression

💧 Watermark support

🔄 PNG / JPG / WebP conversion

📚 Batch image processing

🔐 User authentication

🌍 CloudFront CDN integration

🗄️ DynamoDB metadata storage

📊 Processing history and analytics

🧠 AI-based image optimization

🎯 What This Project Demonstrates

This project provides practical experience with:

Serverless computing

Event-driven architecture

AWS Lambda

Amazon S3

IAM permissions

Python-based cloud functions

Image processing with Pillow

AWS SDK with Boto3

Cloud automation

Frontend-to-cloud integration

Git and GitHub

👨‍💻 Author

Yash Patil

B.Tech – Artificial Intelligence & Machine Learning
R. C. Patel Institute of Technology, Shirpur

Focus: AWS | Full Stack Development | AI & ML

⭐ Project Summary

Serverless Image Resizer is an event-driven AWS application that automatically processes uploaded images using Amazon S3, AWS Lambda, Python, Boto3, and Pillow.

The project demonstrates how serverless cloud services can be combined to create an automated image-processing pipeline without managing traditional servers.
