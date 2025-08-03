\# 🧾 Job Portal Web Application (AWS Based)



\## 📌 Overview



This project is a cloud-based \*\*Job Portal\*\* where users can submit their \*\*Name\*\*, \*\*Email\*\*, and \*\*Resume\*\*. The application is hosted on \*\*AWS EC2\*\* instances behind a \*\*Load Balancer\*\* with \*\*Auto Scaling\*\*, and it uses \*\*S3\*\*, \*\*DynamoDB\*\*, and \*\*SNS\*\* for backend services.



The project demonstrates how to integrate various AWS services to build a scalable, reliable, and serverless-like architecture using core cloud components.



---



\## 🗂️ Folder Structure



job-portal/

├── app/

│   ├── main.py

│   └── templates/

│       └── form.html

├── README.md 





---



\## 🚀 Features



\- Responsive job application form

\- File upload support (Resume)

\- Resume stored in \*\*Amazon S3\*\*

\- Applicant data stored in \*\*DynamoDB\*\*

\- Application ID generated using UUID

\- Real-time notification using \*\*SNS Topic\*\*

\- Scalable backend using \*\*Auto Scaling\*\* and \*\*Application Load Balancer\*\*



---



\## 🔧 Setup Instructions



\### 1. Create S3 Bucket

\- Name: `your-resume-bucket`

\- Enable public access or use pre-signed URLs



\### 2. Create DynamoDB Table

\- Table Name: `JobApplications`

\- Partition Key: `application\_id` (String)



\### 3. Create SNS Topic

\- Name: `JobApplicationTopic`

\- Add your email as a subscriber and confirm it



\### 4. Prepare EC2 Launch Template Script (`launch\_template.sh`)



```bash

\#!/bin/bash

sudo yum update -y

sudo yum install -y python3 git

git clone https://github.com/Shrimanraj-dev/JJob-portal.git

cd JJob-portal/app

pip3 install flask boto3

python3 main.py



5\. Create Launch Template

Add the above script in the User Data



6\. Create Load Balancer \& Auto Scaling Group

Attach the Launch Template



Set Min/Max EC2 count



7\. Assign IAM Role to EC2

With permissions:



AmazonS3FullAccess



AmazonDynamoDBFullAccess



AmazonSNSFullAccess



🛠️ Skills and Tools Demonstrated

AWS EC2, S3, SNS, DynamoDB



IAM Roles and Policies



Auto Scaling \& Load Balancer



Flask (Python)



HTML, CSS (Frontend)



Git \& GitHub



👤 Author

Shrimanraj L J

GitHub: @Shrimanraj-dev

\# 🧾 Job Portal Web Application (AWS Based)



\## 📌 Overview



This project is a cloud-based \*\*Job Portal\*\* where users can submit their \*\*Name\*\*, \*\*Email\*\*, and \*\*Resume\*\*. The application is hosted on \*\*AWS EC2\*\* instances behind a \*\*Load Balancer\*\* with \*\*Auto Scaling\*\*, and it uses \*\*S3\*\*, \*\*DynamoDB\*\*, and \*\*SNS\*\* for backend services.



The project demonstrates how to integrate various AWS services to build a scalable, reliable, and serverless-like architecture using core cloud components.



---



\## 🗂️ Folder Structure



job-portal/

├── app/

│   ├── main.py

│   └── templates/

│       └── form.html

├── README.md 





---



\## 🚀 Features



\- Responsive job application form

\- File upload support (Resume)

\- Resume stored in \*\*Amazon S3\*\*

\- Applicant data stored in \*\*DynamoDB\*\*

\- Application ID generated using UUID

\- Real-time notification using \*\*SNS Topic\*\*

\- Scalable backend using \*\*Auto Scaling\*\* and \*\*Application Load Balancer\*\*



---



\## 🔧 Setup Instructions



\### 1. Create S3 Bucket

\- Name: `your-resume-bucket`

\- Enable public access or use pre-signed URLs



\### 2. Create DynamoDB Table

\- Table Name: `JobApplications`

\- Partition Key: `application\_id` (String)



\### 3. Create SNS Topic

\- Name: `JobApplicationTopic`

\- Add your email as a subscriber and confirm it



\### 4. Prepare EC2 Launch Template Script (`launch\_template.sh`)



```bash

\#!/bin/bash

sudo yum update -y

sudo yum install -y python3 git

git clone https://github.com/Shrimanraj-dev/JJob-portal.git

cd JJob-portal/app

pip3 install flask boto3

python3 main.py



5\. Create Launch Template

Add the above script in the User Data



6\. Create Load Balancer \& Auto Scaling Group

Attach the Launch Template



Set Min/Max EC2 count



7\. Assign IAM Role to EC2

With permissions:



AmazonS3FullAccess



AmazonDynamoDBFullAccess



AmazonSNSFullAccess



🛠️ Skills and Tools Demonstrated

AWS EC2, S3, SNS, DynamoDB



IAM Roles and Policies



Auto Scaling \& Load Balancer



Flask (Python)



HTML, CSS (Frontend)



Git \& GitHub



👤 Author

Shrimanraj L J

GitHub: @Shrimanraj-dev



