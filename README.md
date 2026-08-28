🖼️ Serverless Image Resizer – AWS Lambda Image Processing

A serverless Image Resizer web application that automatically processes and resizes uploaded images using AWS Lambda, Amazon S3, Python, Boto3, and Pillow.

When a user uploads an image through the web interface, the image is stored in an Amazon S3 input bucket. An S3 event notification automatically triggers an AWS Lambda function, which processes the image using the Pillow library and stores the resized image in a separate Amazon S3 output bucket.

This project demonstrates serverless computing, event-driven architecture, cloud storage, automated image processing, and secure AWS resource access without managing traditional servers.

🚀 Features

📤 Upload images through a web interface

⚡ Automatic image resizing using AWS Lambda

☁️ Event-driven architecture using Amazon S3

🐍 Python-based image processing

🖼️ Image manipulation using Pillow

🔗 AWS integration using Boto3

📦 Store original images in an S3 input bucket

📁 Store resized images in a separate S3 output bucket

⬇️ Download processed images

🔐 Secure AWS resource access using IAM roles

🌐 Serverless backend architecture

📱 Responsive frontend interface

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
                Amazon S3 Input Bucket
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
                Amazon S3 Output Bucket
                           │
                           ▼
                  Resized Image
                           │
                           ▼
                  Download Image

⚙️ AWS Services Used

Service

Purpose

Amazon S3

Stores uploaded and processed images

AWS Lambda

Automatically processes images when triggered by S3

AWS IAM

Provides secure permissions for AWS resource access

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

🔄 Project Workflow

Step 1 – Upload Image

The user selects an image through the web interface.

↓

Step 2 – Store Image

The selected image is uploaded to the Amazon S3 Input Bucket.

↓

Step 3 – S3 Event Notification

Amazon S3 detects the newly uploaded object and generates an event notification.

↓

Step 4 – Trigger Lambda

The S3 event automatically invokes the AWS Lambda function.

↓

Step 5 – Retrieve Image

Lambda retrieves the uploaded image from the input S3 bucket using Boto3.

↓

Step 6 – Resize Image

The Lambda function uses Pillow to process and resize the image.

↓

Step 7 – Store Processed Image

The resized image is uploaded to the Amazon S3 Output Bucket.

↓

Step 8 – Download Result

The processed image becomes available for the user to access or download.

🧩 Image Processing Flow

S3 Upload Event
       │
       ▼
   AWS Lambda
       │
       ▼
 Retrieve Image
       │
       ▼
 Pillow Processing
       │
       ▼
  Resize Image
       │
       ▼
Save Processed Image
       │
       ▼
Output S3 Bucket

🛠️ Technologies Used

Python

Boto3

Pillow (Python Imaging Library)

HTML5

CSS3

JavaScript

Amazon S3

AWS Lambda

AWS IAM

Git & GitHub

🔐 Security

IAM roles are used to provide Lambda with the required AWS permissions.

No AWS Access Keys or Secret Keys are stored in the source code.

AWS resources are accessed through IAM-based permissions.

S3 events automatically trigger the image-processing function.

Input and processed images are stored separately.

⚠️ Security Note: Never upload AWS Access Keys, Secret Keys, .env files, private keys, passwords, or other sensitive credentials to GitHub.

📦 Python Dependencies

The Lambda function uses the following Python libraries:

boto3
Pillow

These dependencies are listed in:

lambda/requirements.txt

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
7. Deploy the Frontend
              ↓
8. Upload a Test Image
              ↓
9. Verify Lambda Execution
              ↓
10. Check the Output S3 Bucket

🧪 Example Workflow

User uploads image
        ↓
Input S3 Bucket
        ↓
S3 Event Notification
        ↓
AWS Lambda
        ↓
Pillow processes image
        ↓
Image is resized
        ↓
Output S3 Bucket
        ↓
Processed image available

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

🔮 Future Enhancements

🎚️ Multiple image size options

🗜️ Image compression

💧 Watermark support

🔄 PNG, JPG, and WebP format conversion

📚 Batch image processing

🔐 User authentication

🌍 CloudFront CDN integration

🗄️ Image metadata storage using DynamoDB

📊 Image processing history

🖱️ Drag-and-drop image upload

👁️ Image preview before processing

⭐ Summary

Serverless Image Resizer is an event-driven AWS application that automatically processes uploaded images using Amazon S3, AWS Lambda, Python, Boto3, and Pillow.

The project demonstrates how AWS serverless services can be combined to build an automated, scalable, and efficient image-processing pipeline without managing traditional servers.

👨‍💻 Author

Mohit Manilal Patel

🎓 B.Tech – Artificial Intelligence & Machine Learning

🏫 R. C. Patel Institute of Technology, Shirpur

☁️ AWS with Python Course Trainee – Symbiosis, Sponsored by Capgemini

Focus: AWS | Full Stack Development | AI & ML
