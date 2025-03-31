# Serverless Web App with AWS Lambda & API Gateway

## Overview
This project demonstrates a serverless web application using AWS services. The backend is powered by AWS Lambda, API Gateway, and DynamoDB, while the frontend is hosted on S3 and served via CloudFront.

## Architecture
- **AWS Lambda**: Handles backend logic
- **API Gateway**: Exposes RESTful APIs
- **DynamoDB**: NoSQL database for storage
- **S3**: Hosts static frontend files
- **CloudFront**: CDN for faster delivery
- **Cognito**: User authentication

## Setup Instructions
### Prerequisites
- AWS CLI installed and configured
- Terraform installed
- Node.js and npm installed

### Deployment
1. **Clone the repository**
```sh
git clone https://github.com/yourgithub/serverless-web-app.git
cd serverless-web-app
```
2. **Deploy Backend**
```sh
cd backend
terraform init
terraform apply
```
3. **Deploy Frontend**
```sh
cd frontend
npm install
npm run build
aws s3 sync build/ s3://your-s3-bucket
```

## Repository Structure
```
serverless-web-app/
│── backend/           # Lambda functions and Terraform configs
│   │── main.tf        # Terraform configuration file
│   │── lambda_function.py # AWS Lambda function
│── frontend/          # React frontend app
│── README.md         # Project documentation
```

## Next Steps
- Implement authentication with Cognito
- Add monitoring with AWS CloudWatch
