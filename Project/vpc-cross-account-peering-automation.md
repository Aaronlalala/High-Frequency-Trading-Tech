# VPC Cross Account Peering Automation

[A good direction to start the project.](https://github.com/aws-samples/vpc-cross-account-peering-automation)

## Terms

- **Cloud development kit (CDK).** It's an open-source software development for defining cloud infrastructure in code and provisioning it through AWS Cloud Formation.
- **Custom Lambda Logic**. [AWS Lambda](https://aws.amazon.com/lambda/#:~:text=AWS%20Lambda%20is%20a%20serverless,pay%20for%20what%20you%20use.) is a serverless computing service that lets you run your code without provisioning or managing servers.
- **VPC Peering**. This is a network connection between two Virtual Private Clouds (VPCs) that enables routing using each VPC's private IP address as if they were in the same network.
- **Cross-account IAM Trust**. IAM stands for identity and access management. Cross-account IAM trust would allow one AWS account to assume roles in another AWS account.
- **CloudFormation Custom Resource Provider**. AWS CloudFormation allows you to define "custom resources", resources that are created by a custom piece of code. (like a lambda function)
- **CDK Contrust.** A contruct is a cloud component that encapsulates everything AWS CloudFormation needs to create the component.



## Sequence of events

### Initial Setup

1. Initially the provider deploys the Amazon DynamoDB table and custom resource handler.

   Amazon DynamoDb is a managed NoSQL database service provided by AWS. 

2. The provider fills out the table with connectivity information for their consumer.

   The provider populates the DynamoDB table with information required for a consumer to connect, such as IP, domain names and other config data.

3. Provider shares with the consumer

   - The provider account ID
   - The consumer registration code
   - The arn of the custom resource provider

   ARN stands for Amazon Rsource Name, and it's a unique identifier for AWS resources.