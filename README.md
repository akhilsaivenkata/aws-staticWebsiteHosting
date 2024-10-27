# Static Website Deployment on AWS

## Project Description
This project demonstrates the deployment of a static website on AWS using Amazon S3, CloudFront for content delivery, ACM for SSL management, and a custom domain configuration. The setup includes an automated deployment pipeline with AWS CodePipeline connected to a GitHub repository, allowing instant updates to the website as changes are pushed.

## Audience
This documentation is intended for developers and cloud engineers with a foundational understanding of AWS, GitHub, and basic website deployment.

## Pre-requisites
- An AWS account
- Domain registration with a DNS provider that supports CNAME records

## Architecture Overview
![Architecture Diagram Placeholder]

In this architecture:
- **Amazon S3** hosts the website content (`index.html`, `style.css`).
- **AWS CloudFront** is used as a content delivery network (CDN) for global reach and performance.
- **ACM (AWS Certificate Manager)** provides SSL certificates for secure HTTPS access.
- **Custom Domain** configured via CNAME records links CloudFront distribution with the user-friendly domain name.
- **AWS CodePipeline** automates deployment by connecting to a GitHub repository, instantly reflecting any code updates on the live website.

## Key Steps and Components

### 1. S3 Bucket Creation
- Created an S3 bucket configured for static website hosting.
- Uploaded `index.html` and `style.css` files.

### 2. CloudFront Configuration
- Configured CloudFront distribution with S3 as the origin.
- Enabled caching and HTTPS enforcement for enhanced security and performance.

### 3. Custom Domain with SSL
- Registered a custom domain and used ACM to issue SSL certificates.
- Set up CNAME records in the DNS provider to link the domain to the CloudFront distribution.

### 4. Continuous Deployment via CodePipeline
- Created an AWS CodePipeline to automate website deployment by connecting with the GitHub repository.
- Configured triggers to deploy changes automatically upon every new commit.

## Learnings
- Enhanced understanding of static website hosting and CDN integration.
- Gained experience in configuring SSL certificates and managing custom domains.
- Practical experience in setting up CI/CD pipelines for automated deployments.

## Usage
To modify and deploy updates:
1. Make changes to `index.html` or `style.css`.
2. Commit and push changes to the GitHub repository.
3. CodePipeline will automatically deploy the updated files, making changes live on the website.

## Screenshots
- Deployed Website Screenshot
- CloudFront Configuration Screenshot
- CodePipeline Workflow Screenshot

## Conclusion
Deploying this static website enhanced my understanding of AWS services like S3, CloudFront, ACM, and CodePipeline. This hands-on experience helped streamline cloud-based static site deployment with secure access and automated updates.
