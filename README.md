# AWS Static Website Hosting (S3 + CloudFront)

## Overview
This project demonstrates how to build and deploy a static website using Amazon S3 and deliver it globally using AWS CloudFront. It covers core cloud concepts such as storage, permissions, content delivery, and troubleshooting real-world deployment issues.

---

## Architecture
- Amazon S3 (Static Website Hosting)
- AWS CloudFront (Content Delivery Network)
- IAM Policies (Public Read Access via Bucket Policy)

---

## What I Built
- Created an S3 bucket configured for static website hosting
- Uploaded website files (HTML)
- Configured bucket policies to allow public access
- Enabled static website hosting with index document
- Set up a CloudFront distribution for global content delivery
- Connected CloudFront to the S3 website endpoint

---

## Key Features
- Fully hosted static website on AWS
- Global content delivery using CloudFront CDN
- Secure and controlled access using bucket policies
- High availability and improved performance via CDN caching

---

## Deployment Steps

### 1. Create S3 Bucket
- Created a unique S3 bucket  
- Disabled "Block all public access"  
- Uploaded website files (index.html)  

### 2. Enable Static Website Hosting
- Enabled static hosting in bucket properties  
- Set index.html as the index document  
- Retrieved the S3 website endpoint  

### 3. Configure Bucket Policy
- Applied a public read policy to allow website access  

Bucket Policy Used:

Version: 2012-10-17  
Effect: Allow  
Principal: *  
Action: s3:GetObject  
Resource: arn:aws:s3:::kings-aws-website-ike/*  

### 4. Set Up CloudFront
- Created a CloudFront distribution  
- Used S3 website endpoint as origin  
- Configured default root object (index.html)  
- Waited for deployment to complete  

---

## Challenges & Troubleshooting

### 1. 404 Error (NoSuchKey)
- Cause: index.html not in root directory  
- Fix: Uploaded file directly to bucket root  

### 2. Access Denied Error
- Cause: Using S3 bucket endpoint instead of website endpoint  
- Fix: Switched CloudFront origin to S3 website endpoint  

### 3. HTML Showing as Code
- Cause: Incorrect Content-Type metadata  
- Fix: Set Content-Type to text/html  

### 4. CloudFront Not Updating
- Cause: Cached content  
- Fix: Performed hard refresh or waited for cache update  

---

## Live Demo
CloudFront URL:  
https://d366bsebu8ln7.cloudfront.net/

---

## Screenshots

### S3 Bucket
(Add screenshot here)

### Live Website
(Add screenshot here)

### CloudFront Distribution
(Add screenshot here)

---

## Skills Demonstrated
- AWS S3 configuration and static hosting  
- CloudFront CDN setup and optimisation  
- IAM and bucket policy configuration  
- Troubleshooting cloud deployment issues  
- Understanding of web hosting architecture  

---

## What I Learned
- How static websites are hosted in the cloud  
- The difference between S3 bucket endpoint and website endpoint  
- How CDN improves performance and availability  
- How to debug real-world AWS errors effectively  

---

## Future Improvements
- Add custom domain using Route 53  
- Enable HTTPS with SSL certificate (ACM)  
- Implement CI/CD for automated deployment  

---

## Author
Kingsley Evans
