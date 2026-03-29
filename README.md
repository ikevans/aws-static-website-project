# AWS Static Website Project (S3 + CloudFront)

## Overview
This project demonstrates how to host a static website using AWS S3 and deliver it globally using CloudFront.

## Architecture
- Amazon S3 (Static Website Hosting)
- AWS CloudFront (Content Delivery Network)
- IAM Policies (Public Read Access)

## What I Built
- Created and configured an S3 bucket for static hosting
- Uploaded website files (HTML)
- Enabled static website hosting with index document
- Configured bucket policy for public access
- Set up CloudFront distribution for global delivery
- Linked CloudFront to S3 website endpoint

## Key Challenges & Fixes
- Fixed 404 NoSuchKey error by ensuring correct file structure
- Resolved AccessDenied by using S3 website endpoint instead of bucket endpoint
- Corrected Content-Type metadata to ensure HTML rendering

## Live Demo
[https://d366bsebu8ln7.cloudfront.net]

## Skills Demonstrated
- AWS S3 configuration
- CloudFront setup
- Troubleshooting cloud deployment issues
- Understanding of CDN and hosting concepts
