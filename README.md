# Cloud Learning Journey

A full-stack serverless web application built on AWS to learn core cloud computing concepts.

## Live site
https://d3kq7n5mvwtw4k.cloudfront.net

## Architecture
- **Amazon S3** – hosts the static website files
- **Amazon CloudFront** – CDN providing HTTPS and global caching
- **AWS IAM** – secure access management (MFA-enabled user, least-privilege roles)
- **Amazon API Gateway** – public HTTP endpoint for the contact form
- **AWS Lambda** – serverless function processing form submissions
- **Amazon DynamoDB** – NoSQL database storing contact messages

## Flow
1. Visitor loads the site via CloudFront, served from S3.
2. Visitor submits the contact form.
3. The form sends a POST request to API Gateway.
4. API Gateway triggers a Lambda function.
5. Lambda writes the message to a DynamoDB table.

## What I learned
- Configuring S3 static website hosting and bucket policies
- Setting up CloudFront as a CDN in front of S3
- IAM users, roles, and least-privilege permissions
- Building a serverless backend with Lambda, API Gateway, and DynamoDB
- Debugging real issues: CORS, origin protocol mismatches, and public access blocks
