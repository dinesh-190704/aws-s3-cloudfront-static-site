Static Website Hosting using Amazon S3 and CloudFront
📌 Project Overview

This project demonstrates how to host a static website using Amazon S3 as the origin and Amazon CloudFront as a global Content Delivery Network (CDN). The website content (HTML, CSS, JavaScript) is stored in an S3 bucket and delivered securely and efficiently via a CloudFront distribution.

This implementation follows AWS best practices and is suitable for AWS Free Tier users.

🛠️ AWS Services Used

Amazon S3 – Static website storage

Amazon CloudFront – CDN for global content delivery

AWS IAM – Secure access control

AWS Management Console

🧱 Architecture

User
⬇
CloudFront Distribution Domain
⬇
Amazon S3 Bucket (Origin)
⬇
Static Website Files (HTML, CSS, JS)

⚙️ Implementation Steps
1. Create S3 Bucket

Created an S3 bucket with a globally unique name

Disabled public access

Uploaded:

index.html

style.css

script.js

2. Configure Bucket Permissions

Applied a bucket policy allowing CloudFront access

Prevented direct public access to S3 objects

3. Create CloudFront Distribution

Created a CloudFront distribution

Configured:

Origin: S3 bucket

Origin Access: Secure access via CloudFront

Default Root Object: index.html

Enabled caching and HTTP delivery

4. Website Access

Used the CloudFront Distribution Domain Name:

https://<distribution-id>.cloudfront.net


Verified that accessing the distribution domain loads the static website hosted in S3

🔐 Security Best Practices

S3 bucket access restricted to CloudFront only

No public S3 object access

CloudFront acts as the secure entry point

💰 Cost Optimization

Used AWS Free Tier eligible services

Leveraged CloudFront caching to reduce S3 requests

No custom domain or paid features enabled

📈 Learning Outcomes

Hands-on experience with Amazon S3 static hosting

Understanding of CloudFront distributions and origins

Configuring default root objects

Securing S3 with CloudFront

Real-world CDN usage for web content delivery

🚀 Future Enhancements

Attach a custom domain using Route 53

Enable HTTPS using AWS Certificate Manager (ACM)

Configure CloudWatch monitoring

Add cache invalidation strategies

Implement versioning for static assets

📎 Author

Dinesh M
Engineer - Cloud & AWS 
GitHub: https://github.com/dinesh-190704
