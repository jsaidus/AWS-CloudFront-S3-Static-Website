# AWS CloudFront + S3 Static Website

## Project Overview

This project demonstrates how to deploy a static website using Amazon S3 and accelerate global content delivery with Amazon CloudFront.

CloudFront caches website content at edge locations worldwide, reducing latency while improving website performance, scalability, and availability.

---

## Architecture

```
             User
               │
               ▼
      Amazon CloudFront
               │
               ▼
      Amazon S3 Bucket
               │
               ▼
        Static Website
```

---

## AWS Services Used

- Amazon S3
- Amazon CloudFront
- IAM
- Static Website Hosting

---

## Features

- Static website hosting
- Global content delivery
- Low-latency access
- CloudFront distribution
- Edge caching
- Public website deployment

---

## Skills Demonstrated

- Amazon S3
- Amazon CloudFront
- CDN Configuration
- Cache Distribution
- IAM
- Static Website Deployment
- AWS Networking Fundamentals

---

## Screenshots

Screenshots of the deployment process are included in the **images/** folder.

---

## Lessons Learned

- Creating an S3 static website
- Configuring a CloudFront distribution
- Connecting CloudFront to an S3 origin
- Understanding edge locations and caching
- Deploying highly available static websites

---

## Future Improvements

- Configure HTTPS using AWS Certificate Manager (ACM)
- Add a custom domain with Amazon Route 53
- Enable CloudFront logging
- Implement AWS WAF for enhanced security

---

## Author

**Joseph Saidu Sesay**

Cloud Computing Student

Aspiring Cloud Engineer