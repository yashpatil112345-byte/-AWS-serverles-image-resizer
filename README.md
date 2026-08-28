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

| AWS Service    | Purpose                                                |
| -------------- | ------------------------------------------------------ |
| **Amazon S3**  | Stores uploaded and resized images                     |
| **AWS Lambda** | Automatically processes and resizes uploaded images    |
| **AWS IAM**    | Manages permissions and secure access to AWS resources |

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
                  │      AWS Lambda         │
                  │    Image Processing     │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Pillow Image Resize   │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Output S3 Bucket      │
                  │    Resized Image        │
                  └────────────┬────────────┘
                               │
                               ▼
                         ┌──────────────┐
                         │   Download   │
                         │    Image     │
                         └──────────────┘
```

---

## ⚙️ How It Works

The application follows a serverless image-processing pipeline:

### 1. 🖼️ Upload Image

The user selects an image through the web interface.

### 2. ☁️ Store Image in Amazon S3

The uploaded image is stored in the **Amazon S3 Upload Bucket**.

### 3. 🔔 S3 Event Notification

When a new image is uploaded, Amazon S3 generates an event notification.

### 4. ⚡ Trigger AWS Lambda

The S3 event automatically triggers the **AWS Lambda function**.

### 5. 🐍 Process Image Using Pillow

The Lambda function uses **Python, Boto3, and Pillow** to retrieve the uploaded image and resize it.

### 6. 📦 Store Resized Image

The resized image is saved to the **Amazon S3 Output Bucket**.

### 7. ⬇️ Download Processed Image

The processed image can then be accessed and downloaded from the output location.

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

## 🔐 Security

The project follows basic AWS security practices:

* 🔑 Uses **IAM Roles** for AWS resource permissions
* 🚫 No AWS Access Keys are stored in the source code
* ☁️ Uses a serverless event-driven architecture
* ⚡ Lambda executes automatically through S3 events
* 📦 Images are stored using Amazon S3
* 🛡️ AWS resources are accessed through controlled IAM permissions

---

# 📸 Project Screenshots

## 🏠 Home Page

The web interface allows users to select and upload an image for processing.

<img width="1296" height="663" alt="Serverless Image Resizer Home Page" src="https://github.com/user-attachments/assets/557de051-d870-4733-bc8f-493243d38fc4" />

---

## 📤 Upload Image

The selected image is uploaded through the web interface and sent to the Amazon S3 upload bucket.

<img width="1336" height="702" alt="Image Upload Interface" src="https://github.com/user-attachments/assets/b71baf04-577e-4c51-beee-bd378f86c8f8" />

---

## 🖼️ Image Processing Output

The application displays the processed image after the resizing operation has been completed.

<img width="1552" height="791" alt="Resized Image Processing Output" src="https://github.com/user-attachments/assets/96c7c965-2166-4e3f-af18-fa7502722975" />

---

## ⚡ AWS Lambda Trigger & Execution

An Amazon S3 upload event automatically triggers the AWS Lambda function for image processing.

<img width="1575" height="767" alt="AWS Lambda Trigger and Execution" src="https://github.com/user-attachments/assets/fec2d143-95fc-4b82-87c6-e136d9ffe4b2" />

---

## ⚙️ AWS Lambda Function Configuration

The Lambda function is configured to process uploaded images using Python and the Pillow library.

<img width="1335" height="722" alt="AWS Lambda Function Configuration" src="https://github.com/user-attachments/assets/bfe1dda1-234d-4b76-8f8f-6521fe30a28c" />

---

## 📦 Resized Image in Output Bucket

The processed image is stored in the designated Amazon S3 output bucket after Lambda completes the resizing operation.

<img width="1817" height="862" alt="Resized Image in Amazon S3 Output Bucket" src="https://github.com/user-attachments/assets/03cefa45-1d95-4acc-9334-646123e0de99" />

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
* 📊 Image processing history and analytics

---

## 📚 Key Learning Outcomes

Through this project, I gained practical experience with:

* AWS Lambda
* Amazon S3
* Amazon S3 Event Notifications
* AWS IAM Roles and Permissions
* Python-based image processing
* Pillow
* Boto3
* Serverless architecture
* Event-driven architecture
* Frontend-to-cloud integration
* Git and GitHub

---

## 👨‍💻 Author

### Mohit Manilal Patel

**B.Tech – Artificial Intelligence & Machine Learning**
R. C. Patel Institute of Technology, Shirpur

**AWS with Python Course Trainee**
Symbiosis — Sponsored by Capgemini

---

## ⭐ Project Summary

**Serverless Image Resizer** is a practical demonstration of serverless image processing using AWS.

The application combines **Amazon S3, AWS Lambda, Python, Boto3, and Pillow** to automatically process images without requiring traditional server infrastructure.

### 🔗 Architecture

```text
User
  │
  ▼
Web Application
  │
  ▼
Amazon S3 Upload Bucket
  │
  │ S3 Event
  ▼
AWS Lambda
  │
  ▼
Pillow Image Processing
  │
  ▼
Amazon S3 Output Bucket
  │
  ▼
Resized Image
```

This project demonstrates practical concepts in **cloud computing, serverless architecture, event-driven processing, cloud storage, IAM security, and automated image processing**.

---

## ⭐ Support

If you found this project useful or interesting, consider giving the repository a ⭐ **Star** on GitHub.
