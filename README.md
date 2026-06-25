# AWS CloudFront + Amazon S3 Static Website Hosting

## Project Overview

This project demonstrates how to host a static website using Amazon S3 and improve its performance, availability, and security by distributing the website through Amazon CloudFront.

The website is stored in an Amazon S3 bucket configured for Static Website Hosting, while CloudFront provides global content delivery using AWS edge locations.

---

## Project Objectives

- Create an Amazon S3 bucket
- Enable Static Website Hosting
- Upload website files
- Configure Bucket Policy for public access
- Create an Amazon CloudFront distribution
- Configure the S3 Website Endpoint as the CloudFront Origin
- Set the Default Root Object
- Invalidate cached objects
- Successfully access the website through CloudFront

---

## AWS Services Used

- Amazon S3
- Amazon CloudFront
- AWS IAM
- Amazon Route 53 (optional)
- CloudFront Cache Invalidation

---

## Architecture

User
│
▼
Amazon CloudFront
│
▼
Amazon S3 Static Website
│
▼
index.html

---

## Step 1 — Create an S3 Bucket

Created a new S3 bucket.

Example:

Bucket Name:
joseph-devry-bucket-376707314

Region:
US East (N. Virginia)

Screenshot:

images/01-create-bucket.png

---

## Step 2 — Enable Static Website Hosting

Enabled:

Properties
→ Static Website Hosting

Configuration

- Enable
- Host a static website

Index document

index.html

Screenshot:

images/02-static-hosting.png

---

## Step 3 — Upload Website Files

Uploaded:

- index.html

Verified the website loads successfully from the S3 Website Endpoint.

Screenshot:

images/03-upload-files.png

---

## Step 4 — Configure Bucket Policy

Allowed public read access to website objects.

Example policy:

{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Effect":"Allow",
      "Principal":"*",
      "Action":"s3:GetObject",
      "Resource":"arn:aws:s3:::YOUR_BUCKET/*"
    }
  ]
}

Screenshot:

images/04-bucket-policy.png

---

## Step 5 — Create CloudFront Distribution

Created a new CloudFront Distribution.

Configuration

Origin Type

Amazon S3

Origin

S3 Website Endpoint

Price Class

Use all Edge Locations

Screenshot:

images/05-cloudfront-create.png

---

## Step 6 — Configure CloudFront

Configured:

- S3 Website Endpoint
- Recommended Cache Settings
- Recommended Origin Settings

Default Root Object

index.html

Screenshot:

images/06-cloudfront-settings.png

---

## Step 7 — Cache Invalidation

Created an invalidation after modifying CloudFront.

Invalidation Path

/*

Screenshot:

images/07-invalidation.png

---

## Step 8 — Verify Deployment

Waited for CloudFront deployment.

Verified website successfully loads using the CloudFront URL.

Example:

https://d2pjtu6m2mo9tk.cloudfront.net

Screenshot:

images/08-cloudfront-success.png

---

## Skills Demonstrated

- Amazon S3
- Static Website Hosting
- Amazon CloudFront
- CDN Configuration
- Bucket Policies
- AWS IAM
- Cache Invalidation
- DNS Concepts
- Website Deployment
- Troubleshooting

---

## Challenges Encountered

Initially, the CloudFront distribution returned a DNS resolution error because an incorrect distribution domain name was used.

Additionally, the Default Root Object was configured after deployment, requiring cache invalidation before the updated configuration became available.

After correcting the CloudFront domain name and invalidating the cache, the website was successfully delivered through CloudFront.

---

## Key Learning Outcomes

- Learned how CloudFront distributes static website content globally.
- Understood the difference between an S3 Website Endpoint and an S3 REST Endpoint.
- Configured CloudFront to use a static website as its origin.
- Performed cache invalidation to refresh cached objects.
- Successfully deployed and verified a production-style static website using AWS services.

---

## Author

Joseph Saidu Sesay

Bachelor of Science in Computer Science

Aspiring Cloud Engineer

GitHub:
https://github.com/jsaidus
