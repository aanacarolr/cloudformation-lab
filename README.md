# CloudFormation Lab – Lambda RESTful API

This project automates the deployment of a RESTful API using AWS Lambda and API Gateway, managed via AWS CloudFormation.

## Steps to Launch
1. Deploy the stack:
   aws cloudformation create-stack --stack-name LambdaRestApiStack \
   --template-body file://template.yaml \
   --capabilities CAPABILITY_IAM

2. Wait for the stack to complete deployment:
   aws cloudformation describe-stacks --stack-name LambdaRestApiStack

3. Test your endpoint using curl:
   curl https://y96aqwb2pk.execute-api.eu-west-1.amazonaws.com/dev/ip

4. Update the code to add security features.
   
5. Apply the changes
   aws cloudformation deploy \
  --template template.yaml \
  --stack-name restapi-cloudformation --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM

## Project Structure
- template.yaml → CloudFormation template defining all AWS resources.
- lambda/index.py → Lambda handler code for API responses.

## Tutorial Reference
Based on the "Build and Deploy REST API on AWS" tutorial by Rino Dev, extended with:
- Cleaner infrastructure tagging
- JSON response structure
- IAM principle of least privilege
