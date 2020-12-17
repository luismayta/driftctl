# AWS Supported resources

## Least privileged policy

Driftctl needs access to your cloud provider account so that it can list resources on your behalf.

As AWS documentation recommends, the below policy is granting only the permissions required to perform driftctl's tasks.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Resource": "*",
            "Action": [
                "ec2:DescribeAddresses",
                "ec2:DescribeImages",
                "ec2:DescribeInstanceAttribute",
                "ec2:DescribeInstances",
                "ec2:DescribeInstanceCreditSpecifications",
                "ec2:DescribeKeyPairs",
                "ec2:DescribeSecurityGroups",
                "ec2:DescribeSnapshots",
                "ec2:DescribeTags",
                "ec2:DescribeVolumes",
                "ec2:DescribeVpcs",
                "iam:GetPolicy",
                "iam:GetPolicyVersion",
                "iam:GetRole",
                "iam:GetRolePolicy",
                "iam:GetUser",
                "iam:GetUserPolicy",
                "iam:ListAccessKeys",
                "iam:ListAttachedRolePolicies",
                "iam:ListAttachedUserPolicies",
                "iam:ListPolicies",
                "iam:ListRolePolicies",
                "iam:ListRoles",
                "iam:ListUserPolicies",
                "iam:ListUsers",
                "lambda:GetFunction",
                "lambda:GetFunctionCodeSigningConfig",
                "lambda:ListFunctions",
                "lambda:ListVersionsByFunction",
                "rds:DescribeDBInstances",
                "rds:DescribeDBSubnetGroups",
                "rds:ListTagsForResource",
                "route53:GetHostedZone",
                "route53:ListHostedZones",
                "route53:ListResourceRecordSets",
                "route53:ListTagsForResource",
                "s3:GetAccelerateConfiguration",
                "s3:GetAnalyticsConfiguration",
                "s3:GetBucketAcl",
                "s3:GetBucketCORS",
                "s3:GetBucketLocation",
                "s3:GetBucketLogging",
                "s3:GetBucketNotification",
                "s3:GetBucketObjectLockConfiguration",
                "s3:GetBucketPolicy",
                "s3:GetBucketRequestPayment",
                "s3:GetBucketTagging",
                "s3:GetBucketVersioning",
                "s3:GetBucketWebsite",
                "s3:GetEncryptionConfiguration",
                "s3:GetInventoryConfiguration",
                "s3:GetLifecycleConfiguration",
                "s3:GetMetricsConfiguration",
                "s3:GetReplicationConfiguration",
                "s3:ListAllMyBuckets",
                "s3:ListBucket"
            ]
        }
    ]
}
```

## S3

- [x]  aws_s3_bucket
- [x]  aws_s3_bucket_analytics_configuration
- [x]  aws_s3_bucket_inventory
- [x]  aws_s3_bucket_metric
- [x]  aws_s3_bucket_notification
- [x]  aws_s3_bucket_policy
- [ ]  aws_s3_access_point
- [ ]  aws_s3_account_public_access_block
- [ ]  aws_s3_bucket_object
- [ ]  aws_s3_bucket_public_access_block


## EC2

- [x]  aws_instance
- [x]  aws_key_pair
- [x]  aws_ami
- [x]  aws_ebs_snapshot
- [x]  aws_ebs_volume
- [x]  aws_eip
- [x]  aws_eip_association

## Lambda

- [x]  aws_lambda_function
- [ ]  aws_lambda_alias
- [ ]  aws_lambda_event_source_mapping
- [ ]  aws_lambda_function_event_invoke_config
- [ ]  aws_lambda_layer_version
- [ ]  aws_lambda_permission
- [ ]  aws_lambda_provisioned_concurrency_config

## RDS

- [x]  aws_db_instance
- [x]  aws_db_subnet_group
- [ ]  aws_rds_cluster
- [ ]  aws_rds_cluster_endpoint
- [ ]  aws_rds_cluster_instance
- [ ]  aws_db_cluster_snapshot
- [ ]  aws_db_event_subscription
- [ ]  aws_db_instance_role_association
- [ ]  aws_db_option_group
- [ ]  aws_db_parameter_group
- [ ]  aws_db_proxy
- [ ]  aws_db_proxy_default_target_group
- [ ]  aws_db_snapshot
- [ ]  aws_rds_cluster_endpoint
- [ ]  aws_rds_cluster_parameter_group
- [ ]  aws_rds_global_cluster
- [ ]  aws_db_security_group

## Route53

- [x]  aws_route53_record
- [x]  aws_route53_zone
- [ ]  aws_route53_delegation_set
- [ ]  aws_route53_health_check
- [ ]  aws_route53_query_log
- [ ]  aws_route53_vpc_association_authorization
- [ ]  aws_route53_zone_association

## IAM

- [x]  aws_iam_access_key
- [ ]  aws_iam_instance_profile
- [x]  aws_iam_policy
- [x]  aws_iam_policy_attachment
- [ ]  aws_iam_group
- [ ]  aws_iam_group_membership
- [ ]  aws_iam_group_policy
- [ ]  aws_iam_group_policy_attachment
- [x]  aws_iam_role
- [x]  aws_iam_role_policy
- [x]  aws_iam_role_policy_attachment
- [x]  aws_iam_user
- [ ]  aws_iam_user_group_membership
- [x]  aws_iam_user_policy
- [x]  aws_iam_user_policy_attachment
- [ ]  aws_iam_user_ssh_key
- [ ]  aws_iam_account_alias
- [ ]  aws_iam_account_password_policy
- [ ]  aws_iam_openid_connect_provider
- [ ]  aws_iam_saml_provider
- [ ]  aws_iam_server_certificate
- [ ]  aws_iam_service_linked_role
- [ ]  aws_iam_user_login_profile

## VPC

- [x]  aws_security_group
- [x]  aws_security_group_rule