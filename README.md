# AWS-Serverless-Project
## Purpose
To build a serverless web application that solves traditional web hosting problems like
- Security vulnerabilities from managing servers
- Wasting money on infrastructure during low traffic periods
- Scaling issues during traffic spikes

## Architecture Overview
- Completely serverless with no infrastructure to manage
- Cloudfront integration for improved performance and security
- API Gateway routes HTTP requests to Lambdas
- Lambda 1 handles GET requests and Lambda 2 handles POST requests
- IAM roles following the principle of least privilege 
- Highly available, scalable, secure, optimized for cost
- Lambda only runs when an event is triggered. You don't pay for downtime
- Cloudwatch metrics, logs, and alarms for monitoring and 

## Architecture Diagram
![Architecture Diagram](Screenshots/Architecture Diagram.png)

## Security Considerations
- AWS manages the underlying network of all services
- No customer managed network
- No servers to compromise 
- No open ports
- CloudFront protects against DDoS through Shield Standard
- IAM roles following principle of least privilege
- Throttling on API Gateway protects it from being overwhelmed, reducing risk of DoS attacks

## Cost Optimization
- Lambda has a generous permanent free tier and you only pay for what you use beyond that. No paying for idle servers
- HTTP API Gateway is cheaer than REST API and still provides all necessary functions for this use case
- CloudFront caching reduces requests to the API Gateway and Lambda, lowering costs
- CloudWatch log retention enabled to save costs 

## Monitoring and Observation
- CloudWatch logs from API Gateway show all traffic and can be filtered to monitor GET or POST requests
- Set up CloudWatch alarms to notify me via SNS whenever an error occurs 
- Set up a custom CloudWatch dashboard that monitors Lambda, API Gateway, DynamoDB, and CloudFront metrics all in one place


## Technologies Used
- CloudFront
- Lambda
- API Gateway 
- DynamoDB
- IAM
- CloudWatch (Metrics, logs, alarms)
- 
## What I Learned
- How to set up a serverless website
- How to use a HTTP API Gateway to route HTTP traffic 
- How to assign IAM roles in accordance with the principle of least privilege 
- How to set up custom dashboards in CloudWatch and monitor effectively
- How CloudFront can be used to improve sercurity and performance

## Future Enhancements
- Route 53 for a custom DNS name
- WAF for extra security 
- reCAPTCHA to prevent bots from abusing DynamoDB



