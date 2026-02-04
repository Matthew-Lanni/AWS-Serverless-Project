# AWS-Serverless-Project
I built a serverless web app that is highly scalable, available, and cost optimized. CloudFront is the front door that ensures low latency for the user and protects against DDoS attacks. API Gateway routes HTTP requests to one of two Lambdas depending on the request. My POST Lambda writes to DynamoDB. Everything is monitored with CloudWatch. 
