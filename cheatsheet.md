# CloudFormation Cheatsheet

## Validate a template
aws cloudformation validate-template   --template-body file://infra/vpc.yaml   --profile cf

## Deploy a stack
aws cloudformation deploy   --template-file infra/vpc.yaml   --stack-name starter-vpc   --profile cf

## Delete a stack
aws cloudformation delete-stack   --stack-name starter-vpc   --profile cf
