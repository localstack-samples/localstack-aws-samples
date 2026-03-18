# LocalStack AWS Samples

A collection of AWS sample applications that can be deployed and tested with [LocalStack](https://localstack.cloud).

Each sample includes up to four Infrastructure-as-Code deployment methods:
- **Scripts** — AWS CLI shell scripts
- **Terraform** — HashiCorp Terraform configurations
- **CloudFormation** — AWS CloudFormation templates
- **CDK** — AWS Cloud Development Kit apps

## Samples

| Sample | Language | Scripts | Terraform | CloudFormation | CDK |
|--------|----------|---------|-----------|----------------|-----|
| [apigw-custom-domain](apigw-custom-domain/) | python | ✓ | ✓ | ✓ | ✓ |
| [apigw-websockets](apigw-websockets/) | javascript | ✓ | ✓ | ✓ | ✓ |
| [appsync-graphql-api](appsync-graphql-api/) | python | ✓ | ✓ | ✓ | ✓ |
| [athena-s3-queries](athena-s3-queries/) | python | ✓ | ✓ | ✓ | ✓ |
| [cdk-for-terraform](cdk-for-terraform/) | — |  |  |  |  |
| [cdk-resources](cdk-resources/) | javascript |  |  |  |  |
| [chalice-rest-api](chalice-rest-api/) | python | ✓ | ✓ | ✓ | ✓ |
| [cloudwatch-metrics-aws](cloudwatch-metrics-aws/) | python | ✓ | ✓ | ✓ | ✓ |
| [codecommit-git-repo](codecommit-git-repo/) | python | ✓ | ✓ |  |  |
| [cognito-jwt](cognito-jwt/) | python | ✓ | ✓ | ✓ | ✓ |
| [ec2-docker-instances](ec2-docker-instances/) | python | ✓ | ✓ | ✓ | ✓ |
| [ecs-ecr-app](ecs-ecr-app/) | python | ✓ | ✓ | ✓ | ✓ |
| [elb-load-balancing](elb-load-balancing/) | javascript | ✓ | ✓ | ✓ | ✓ |
| [emr-serverless-python-dependencies](emr-serverless-python-dependencies/) | python |  |  |  |  |
| [emr-serverless-spark](emr-serverless-spark/) | java | ✓ | ✓ | ✓ | ✓ |
| [glacier-s3-select](glacier-s3-select/) | python | ✓ | ✓ | ✓ | ✓ |
| [glue-etl-jobs](glue-etl-jobs/) | python | ✓ | ✓ | ✓ | ✓ |
| [glue-msk-schema-registry](glue-msk-schema-registry/) | python | ✓ | ✓ | ✓ | ✓ |
| [glue-redshift-crawler](glue-redshift-crawler/) | python | ✓ | ✓ | ✓ | ✓ |
| [iam-policy-enforcement](iam-policy-enforcement/) | python | ✓ | ✓ | ✓ | ✓ |
| [iot-basics](iot-basics/) | python | ✓ | ✓ | ✓ | ✓ |
| [lambda-cloudfront](lambda-cloudfront/) | python | ✓ | ✓ | ✓ | ✓ |
| [lambda-container-image](lambda-container-image/) | python | ✓ | ✓ | ✓ | ✓ |
| [lambda-debugging-sam-java](lambda-debugging-sam-java/) | — |  |  |  |  |
| [lambda-debugging-sam-javascript](lambda-debugging-sam-javascript/) | — |  |  |  |  |
| [lambda-debugging-sam-python](lambda-debugging-sam-python/) | python |  |  |  |  |
| [lambda-debugging-sam-typescript](lambda-debugging-sam-typescript/) | — |  |  |  |  |
| [lambda-event-filtering](lambda-event-filtering/) | javascript, python | ✓ | ✓ | ✓ | ✓ |
| [lambda-function-urls](lambda-function-urls/) | javascript, python | ✓ | ✓ | ✓ | ✓ |
| [lambda-layers](lambda-layers/) | javascript | ✓ | ✓ | ✓ | ✓ |
| [lambda-php-bref-cdk-app](lambda-php-bref-cdk-app/) | javascript |  |  |  |  |
| [lambda-s3-http](lambda-s3-http/) | python | ✓ | ✓ | ✓ | ✓ |
| [lambda-xray](lambda-xray/) | python | ✓ | ✓ | ✓ | ✓ |
| [mq-broker](mq-broker/) | python | ✓ | ✓ | ✓ | ✓ |
| [multi-account-multi-region-s3-access](multi-account-multi-region-s3-access/) | — |  |  |  |  |
| [neptune-graph-db](neptune-graph-db/) | python | ✓ | ✓ | ✓ | ✓ |
| [rds-db-queries](rds-db-queries/) | python | ✓ | ✓ | ✓ | ✓ |
| [rds-failover-test](rds-failover-test/) | python | ✓ | ✓ | ✓ | ✓ |
| [reproducible-ml](reproducible-ml/) | python | ✓ | ✓ | ✓ | ✓ |
| [route53-dns-failover](route53-dns-failover/) | python | ✓ | ✓ | ✓ | ✓ |
| [sagemaker-inference](sagemaker-inference/) | python | ✓ | ✓ | ✓ | ✓ |
| [stepfunctions-lambda](stepfunctions-lambda/) | python | ✓ | ✓ | ✓ | ✓ |
| [terraform-resources](terraform-resources/) | — |  |  |  |  |
| [testcontainers-java-sample](testcontainers-java-sample/) | — |  |  |  |  |
| [transfer-ftp-s3](transfer-ftp-s3/) | python | ✓ | ✓ | ✓ | ✓ |
| [web-app-dynamodb](web-app-dynamodb/) | python | ✓ | ✓ | ✓ | ✓ |
| [web-app-rds](web-app-rds/) | python | ✓ | ✓ | ✓ | ✓ |

## Quick Start

```bash
# Set AWS credentials for LocalStack
export AWS_ACCESS_KEY_ID=test
export AWS_SECRET_ACCESS_KEY=test
export AWS_DEFAULT_REGION=us-east-1

# Deploy a sample
bash lambda-function-urls/python/scripts/deploy.sh

# Teardown
bash lambda-function-urls/python/scripts/teardown.sh
```

## Prerequisites

- Docker
- [LocalStack](https://localstack.cloud) (running on localhost.localstack.cloud:4566)
- AWS CLI
- Terraform (for Terraform deployments)
- AWS CDK + Node.js (for CDK deployments)
