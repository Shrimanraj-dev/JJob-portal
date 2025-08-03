Project Title: Job Portal Web Application (AWS Based)



Overview:

This project is a cloud-based Job Portal where users can submit their Name, Email, and Resume. The application is hosted on AWS EC2 instances behind a Load Balancer with Auto Scaling, and it uses S3, DynamoDB, and SNS for backend services.



The project demonstrates how to integrate various AWS services to build a scalable, reliable, and serverless-like architecture using core cloud components.



---



Folder Structure:



jjob-portal/

├── app/

│   ├── main.py

│   └── templates/

│       └── form.html

├── README.md



---



Features :



\- Responsive job application form

\- File upload support (Resume PDF/doc)

\- Resume stored in Amazon S3

\- Applicant data stored in DynamoDB

\- Application ID generated using UUID

\- Real-time notification using SNS Topic

\- Scalable backend using Auto Scaling and Application Load Balancer



---



Setup Instructions:

1\. Prepare Your Code

Create a GitHub repository with the folder structure above



Add Flask app, HTML form, and bash script



2\. Create an S3 Bucket

Name: your-resume-bucket



Enable public access or use pre-signed URLs if needed



3\. Create a DynamoDB Table

Table Name: JobApplications



Partition Key: application\_id (String)



4\. Create SNS Topic

Name: JobApplicationTopic



Add your email as a subscriber and confirm it



5\. Prepare Launch Template Script (launch\_template.sh)

Install Python, Flask



Pull code from GitHub



Run the Flask server



```bash

\#!/bin/bash

sudo yum update -y

sudo yum install -y python3 git

git clone https://github.com/Shrimanraj-dev/JJob-portal.git

cd JJob-portal/app

pip3 install flask boto3

python3 main.py

```





6\. Launch Template

Use the above bash script in the User Data section



7\. Create Load Balancer + Auto Scaling Group

Attach the launch template



Set minimum/maximum instance count



8\. Security Groups

Allow HTTP (port 80) and SSH (port 22)



Ensure proper IAM role with permissions:



&nbsp; AmazonS3FullAccess



&nbsp; AmazonDynamoDBFullAccess



&nbsp; AmazonSNSFullAccess



Skills and Tools Demonstrated :



AWS EC2



AWS Launch Template



Auto Scaling and Load Balancer



Amazon S3 (Object Storage)



Amazon DynamoDB (NoSQL Database)



Amazon SNS (Notification Service)



IAM Role and Policy Management



Flask (Python Web Framework)



HTML/CSS (Frontend Form)



Git \& GitHub



📞 Contact / Author

Shrimanraj L J

Email: shrimanraj.lj@gmail.com

LinkedIn: https://www.linkedin.com/in/shrimanraj-lj-523a84141

GitHub: https://github.com/Shrimanraj-dev/JJob-portal

