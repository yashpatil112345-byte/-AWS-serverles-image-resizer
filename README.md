# 🖼️ Serverless Image Resizer

### AWS Lambda + Amazon S3 + Pillow

An event-driven serverless application that automatically resizes images uploaded to Amazon S3 using AWS Lambda and the Pillow library.

When a user uploads an image through the web interface, the image is stored in an Amazon S3 bucket. The upload event triggers an AWS Lambda function, which processes and resizes the image using Pillow and stores the resized image in a separate S3 bucket.

---

## ✨ Features

* 🖼️ Upload images through a web interface
* ⚡ Automatic image resizing using AWS Lambda
* ☁️ Event-driven architecture with Amazon S3
* 🐍 Image processing using Python and Pillow
* 📦 Store processed images in a separate S3 bucket
* ⬇️ Download processed images
* 🚀 Fully serverless architecture
* 📱 Responsive frontend interface

---

## ☁️ AWS Services Used

| Service        | Purpose                                        |
| -------------- | ---------------------------------------------- |
| **Amazon S3**  | Stores uploaded and processed images           |
| **AWS Lambda** | Processes and resizes images                   |
| **AWS IAM**    | Manages permissions and secure resource access |

---

## 💻 Technologies Used

* **Python**
* **HTML**
* **CSS**
* **JavaScript**
* **Boto3**
* **Pillow (Python Imaging Library)**
* **Git & GitHub**

---

## 🔄 Project Workflow

```text
                         ┌──────────────┐
                         │     User     │
                         └──────┬───────┘
                                │
                                ▼
                     ┌────────────────────┐
                     │  Web Application   │
                     └─────────┬──────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │  Upload Image to S3     │
                  │     Upload Bucket       │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   S3 Event Notification │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │     AWS Lambda          │
                  │   Image Processing      │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Pillow Image Resize   │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │  Output S3 Bucket       │
                  │  Resized Image          │
                  └────────────┬────────────┘
                               │
                               ▼
                         ┌──────────────┐
                         │    Download  │
                         │    Image     │
                         └──────────────┘
```

---

## 📁 Project Structure

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

## ⚙️ How It Works

The application follows a simple serverless image-processing pipeline:

### 1. Upload Image

The user selects an image through the web interface.

### 2. Store Image in S3

The uploaded image is stored in the **Amazon S3 Upload Bucket**.

### 3. Trigger Lambda

Amazon S3 generates an event notification when a new image is uploaded. This event triggers the **AWS Lambda function**.

### 4. Process Image

The Lambda function uses **Pillow** to open and resize the uploaded image.

### 5. Store Resized Image

The processed image is saved to a separate **Amazon S3 Output Bucket**.

### 6. Download Result

The user can download the resized image from the output location.

---

## 🔐 Security

The project follows basic AWS security practices:

* 🔑 Uses **IAM Roles** for AWS resource permissions
* 🚫 No AWS Access Keys are stored in the source code
* ☁️ Uses a serverless event-driven architecture
* ⚡ Lambda executes automatically through S3 events
* 📦 Images are stored using Amazon S3

---

## 📸 Project Screenshots

### 🏠 Home Page

<img width="1296" height="663" alt="Home Page" src="https://github.com/user-attachments/assets/557de051-d870-4733-bc8f-493243d38fc4" />

---

### 📤 Upload Image

<img width="1336" height="702" alt="Upload Image" src="https://github.com/user-attachments/assets/b71baf04-577e-4c51-beee-bd378f86c8f8" />

---

### 🖼️ Image Processing Output

<img width="1552" height="791" alt="Image Processing Output" src="https://github.com/user-attachments/assets/96c7c965-2166-4e3f-af18-fa7502722975" />

---

### ⚡ AWS Lambda Trigger

<img width="1575" height="767" alt="AWS Lambda Trigger" src="https://github.com/user-attachments/assets/fec2d143-95fc-4b82-87c6-e136d9ffe4b2" />

<img width="1335" height="722" alt="AWS Lambda Configuration" src="https://github.com/user-attachments/assets/bfe1dda1-234d-4b76-8f8f-6521fe30a28c" />

---

### 📦 Resized Image in Output Bucket

<img width="1817" height="862" alt="Resized Image in Output Bucket" src="https://github.com/user-attachments/assets/03cefa45-1d95-4acc-9334-646123e0de99" />

---

## 🚀 Future Enhancements

* 📐 Multiple image size options
* 🗜️ Image compression
* 🖋️ Watermark support
* 🔄 Image format conversion — PNG, JPG, WebP
* 📚 Batch image processing
* 🔐 User authentication
* 🌐 CloudFront CDN integration
* 🗄️ Image metadata storage using DynamoDB

---

## 👨‍💻 Author

### Mohit Manilal Patel

**B.Tech – Artificial Intelligence & Machine Learning**
R. C. Patel Institute of Technology, Shirpur

**AWS with Python Course Trainee**
Symbiosis — Sponsored by Capgemini

---

## ⭐ Project Summary

**Serverless Image Resizer** demonstrates how AWS serverless technologies can be combined to build an automated image-processing application.

The project integrates:

**Amazon S3 → S3 Event → AWS Lambda → Pillow → Output S3 Bucket**

It demonstrates practical concepts including **serverless computing, cloud storage, event-driven architecture, automated image processing, IAM security, and scalable AWS application design**.

---

## 📌 Key Learning Outcomes

Through this project, I gained practical experience with:

* AWS Lambda functions
* Amazon S3 buckets and events
* IAM roles and permissions
* Python-based image processing
* Pillow library
* Boto3
* Event-driven serverless architecture
* Frontend-to-cloud integration
* Git and GitHub project management

---

⭐ **If you found this project useful, consider giving it a star!**
