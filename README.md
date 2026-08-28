# 🖼️ Serverless Image Resizer – AWS Lambda Image Processing

Serverless Image Resizer is an event-driven cloud application that automatically resizes uploaded images using AWS Lambda and the Pillow library. When a user uploads an image to an Amazon S3 bucket, the upload event triggers a Lambda function that resizes the image and stores the processed version in a separate S3 bucket. The application demonstrates serverless image processing without managing any servers.

---

# 🚀 Features

* Upload images through a web interface
* Automatic image resizing using AWS Lambda
* Event-driven architecture with Amazon S3
* Process images using the Pillow library
* Store resized images in a separate S3 bucket
* Download processed images
* Serverless deployment
* Responsive frontend interface

---

# ☁️ AWS Services Used

* Amazon S3
* AWS Lambda
* AWS IAM

---

# 💻 Technologies

* Python
* HTML
* CSS
* JavaScript
* Boto3
* Pillow (Python Imaging Library)
* Git & GitHub

---

# 📂 Project Workflow

```text
          User
            │
            ▼
      Web Application
            │
            ▼
 Upload Image to Amazon S3
            │
            ▼
    S3 Event Notification
            │
            ▼
      AWS Lambda Trigger
            │
            ▼
 Resize Image using Pillow
            │
            ▼
 Store Resized Image
     in Output S3 Bucket
            │
            ▼
 Download Processed Image
```

---

# 📁 Project Structure

```text
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
```

---

# 🔐 Security

* IAM Roles used for secure AWS resource access
* No AWS Access Keys stored in source code
* Serverless event-driven architecture
* Automatic execution through Amazon S3 events
* Secure image storage using Amazon S3

---

# ⚙️ How It Works

1. User uploads an image through the web interface.
2. The image is stored in the Amazon S3 Upload Bucket.
3. Amazon S3 triggers the AWS Lambda function.
4. Lambda uses the Pillow library to resize the image.
5. The resized image is saved to the Amazon S3 Output Bucket.
6. User downloads the processed image.

---

# 🚀 Future Enhancements

* Multiple image size options
* Image compression
* Watermark support
* Image format conversion (PNG, JPG, WebP)
* Batch image processing
* User authentication
* CloudFront CDN integration
* Image metadata storage using DynamoDB

---

# 👨‍💻 Author

**Mohit Manilal Patel**

* B.Tech – Artificial Intelligence & Machine Learning
* R. C. Patel Institute of Technology, Shirpur
* AWS with Python Course Trainee (Symbiosis, Sponsored by Capgemini)

---

# ⭐ Summary

Serverless Image Resizer is an event-driven AWS application that automatically processes uploaded images using Amazon S3, AWS Lambda, and the Pillow library. The project demonstrates serverless computing, cloud storage, automated image processing, and scalable AWS architecture without managing servers.

---

# 📸 Project Screenshots

## Home Page

<img width="1296" height="663" alt="Home Page" src="https://github.com/user-attachments/assets/557de051-d870-4733-bc8f-493243d38fc4" />

---

## Upload Image

<img width="1336" height="702" alt="Upload Image" src="https://github.com/user-attachments/assets/b71baf04-577e-4c51-beee-bd378f86c8f8" />

---

## Output

<img width="1552" height="791" alt="Output Image" src="https://github.com/user-attachments/assets/96c7c965-2166-4e3f-af18-fa7502722975" />

---

## AWS Lambda Trigger

<img width="1575" height="767" alt="AWS Lambda Trigger" src="https://github.com/user-attachments/assets/fec2d143-95fc-4b82-87c6-e136d9ffe4b2" />

<img width="1335" height="722" alt="AWS Lambda Configuration" src="https://github.com/user-attachments/assets/bfe1dda1-234d-4b76-8f8f-6521fe30a28c" />

---

## Resized Image in Output Bucket

<img width="1817" height="862" alt="Resized Image in Output Bucket" src="https://github.com/user-attachments/assets/03cefa45-1d95-4acc-9334-646123e0de99" />

---
