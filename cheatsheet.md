# CloudFormation Cheatsheet

## Validate a template
aws cloudformation validate-template   --template-body file://infra/vpc.yaml   --profile cf

## Deploy a stack
aws cloudformation deploy   --template-file infra/vpc.yaml   --stack-name starter-vpc   --profile cf

## Delete a stack
aws cloudformation delete-stack   --stack-name starter-vpc   --profile cf

## Verify a stack i gone
aws ec2 describe-vpcs --query "Vpcs[].{Id:VpcId,CIDR:CidrBlock,IsDefault:IsDefault}" --profile cf

## Describe Route Tables
aws ec2 describe-route-tables --filters Name=vpc-id,Values=$VPC_ID --profile cf
# Why: verify public/private route tables in a VPC
