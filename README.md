🖼️ Serverless Image Resizer - AWS Lambda Image Processing

A serverless Image Resizer web application built using AWS Lambda, Amazon S3, AWS IAM, Python, Pillow, Boto3, HTML, CSS, and JavaScript.

Users can upload images through a web interface. When an image is uploaded to an Amazon S3 bucket, an S3 event automatically triggers an AWS Lambda function. Lambda uses the Pillow library to resize the image and stores the processed image in a separate S3 output bucket.

This project demonstrates serverless computing, event-driven architecture, automated image processing, cloud storage, and secure AWS resource access without managing traditional servers.

🚀 Features

Upload images through a web interface

Automatically resize uploaded images

Event-driven image processing using Amazon S3

Process images using AWS Lambda

Use Pillow for image manipulation

Store original images in an input S3 bucket

Store resized images in a separate output S3 bucket

Download processed images

Secure AWS resource access using IAM roles

Serverless backend architecture

Responsive web interface

🏗️ Architecture

                    User
                      │
                      ▼
            HTML / CSS / JavaScript
                      │
                      ▼
              Upload Image
                      │
                      ▼
            Amazon S3 - Input Bucket
                      │
                      │ S3 Event Notification
                      ▼
               AWS Lambda
                      │
                      ▼
          Python + Boto3 + Pillow
                      │
                      │ Resize Image
                      ▼
            Amazon S3 - Output Bucket
                      │
                      ▼
             Processed Image
                      │
                      ▼
              Download Image

⚙️ AWS Services Used

Service

Purpose

Amazon S3

Store uploaded and processed images

AWS Lambda

Automatically process uploaded images

AWS IAM

Manage secure permissions for AWS resources

📂 Project Structure

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

🔄 Workflow

Step 1

User opens the web application and selects an image.

↓

Step 2

The selected image is uploaded to the Amazon S3 Input Bucket.

↓

Step 3

Amazon S3 generates an event notification when the new image is uploaded.

↓

Step 4

The S3 event automatically triggers the AWS Lambda function.

↓

Step 5

Lambda retrieves the uploaded image from the input bucket using Boto3.

↓

Step 6

The Lambda function uses Pillow to resize the image.

↓

Step 7

The resized image is uploaded to the Amazon S3 Output Bucket.

↓

Step 8

The processed image becomes available for the user to access or download.

📸 Screenshots

Home Page

<img width="1296" height="663" alt="Home Page" src="https://github.com/user-attachments/assets/557de051-d870-4733-bc8f-493243d38fc4" />

Upload Image

<img width="1336" height="702" alt="Upload Image" src="https://github.com/user-attachments/assets/b71baf04-577e-4c51-beee-bd378f86c8f8" />

Processed Image Output

<img width="1552" height="791" alt="Processed Image Output" src="https://github.com/user-attachments/assets/96c7c965-2166-4e3f-af18-fa7502722975" />

AWS Lambda Trigger

<img width="1575" height="767" alt="AWS Lambda Trigger" src="https://github.com/user-attachments/assets/fec2d143-95fc-4b82-87c6-e136d9ffe4b2" />

Lambda Configuration

<img width="1335" height="722" alt="Lambda Configuration" src="https://github.com/user-attachments/assets/bfe1dda1-234d-4b76-8f8f-6521fe30a28c" />

Resized Image in Output Bucket

<img width="1817" height="862" alt="Resized Image in Output Bucket" src="https://github.com/user-attachments/assets/03cefa45-1d95-4acc-9334-646123e0de99" />

🛠️ Technologies Used

Python

Boto3

Pillow

HTML5

CSS3

JavaScript

AWS Lambda

Amazon S3

AWS IAM

Git & GitHub

🔐 Security

IAM roles are used to provide Lambda with the required AWS permissions.

No AWS Access Keys or Secret Keys are stored in the source code.

AWS resources are accessed through configured IAM permissions.

S3 events automatically trigger the Lambda function.

Input and processed images are separated between S3 buckets.

⚠️ Security Note: Never upload AWS Access Keys, Secret Keys, .env files, private keys, or other credentials to GitHub.

🧩 Lambda Image Processing

The Lambda function performs the core image-processing operation.

Amazon S3 Event
       │
       ▼
AWS Lambda
       │
       ▼
Download Image
       │
       ▼
Open with Pillow
       │
       ▼
Resize Image
       │
       ▼
Save Processed Image
       │
       ▼
Upload to Output S3 Bucket

📦 Python Dependencies

The Lambda function uses the following Python libraries:

boto3
Pillow

These dependencies are specified in:

lambda/requirements.txt

🚀 Future Improvements

Multiple image size options

Image compression

Watermark support

PNG, JPG, and WebP conversion

Batch image processing

User authentication

CloudFront CDN integration

Image metadata storage using DynamoDB

Image processing history

Drag-and-drop image upload

Image preview before processing

🎯 What This Project Demonstrates

This project provides practical experience with:

Serverless computing

Event-driven architecture

AWS Lambda

Amazon S3

AWS IAM

Python cloud development

Boto3 AWS SDK

Image processing with Pillow

Automated cloud workflows

Frontend and cloud integration

Git and GitHub

⭐ Summary

Serverless Image Resizer is an event-driven AWS application that automatically processes uploaded images using Amazon S3, AWS Lambda, Python, Boto3, and Pillow.

The project demonstrates how AWS serverless services can be combined to build an automated, scalable, and efficient image-processing pipeline without managing traditional servers.

👨‍💻 Author

Yash Patil

B.Tech - Artificial Intelligence & Machine Learning

R. C. Patel Institute of Technology, Shirpur

Focus: AWS | Full Stack Development | AI & ML
