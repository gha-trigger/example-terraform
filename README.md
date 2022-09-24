# example-terraform

Example Terraform Configuration for gha-trigger

https://gha-trigger.github.io/getting-started

## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.2 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | 4.32.0 |
| <a name="requirement_local"></a> [local](#requirement\_local) | 2.2.3 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 4.32.0 |
| <a name="provider_local"></a> [local](#provider\_local) | 2.2.3 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_api_gateway_deployment.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_deployment) | resource |
| [aws_api_gateway_integration.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_integration) | resource |
| [aws_api_gateway_integration_response.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_integration_response) | resource |
| [aws_api_gateway_method.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_method) | resource |
| [aws_api_gateway_method_response.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_method_response) | resource |
| [aws_api_gateway_resource.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_resource) | resource |
| [aws_api_gateway_rest_api.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_rest_api) | resource |
| [aws_api_gateway_stage.default](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/api_gateway_stage) | resource |
| [aws_cloudwatch_log_group.lambda_log](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/cloudwatch_log_group) | resource |
| [aws_iam_role.lambda](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/iam_role) | resource |
| [aws_iam_role_policy.lambda_log](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/iam_role_policy) | resource |
| [aws_iam_role_policy.read_secret](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/iam_role_policy) | resource |
| [aws_lambda_function.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/lambda_function) | resource |
| [aws_lambda_permission.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/lambda_permission) | resource |
| [aws_secretsmanager_secret.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/secretsmanager_secret) | resource |
| [aws_secretsmanager_secret.trigger_workflow](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/secretsmanager_secret) | resource |
| [aws_secretsmanager_secret_version.main](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/secretsmanager_secret_version) | resource |
| [aws_secretsmanager_secret_version.trigger_workflow](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/resources/secretsmanager_secret_version) | resource |
| [aws_caller_identity.current](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/data-sources/caller_identity) | data source |
| [aws_iam_policy_document.lambda](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/data-sources/iam_policy_document) | data source |
| [aws_iam_policy_document.lambda_log](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/data-sources/iam_policy_document) | data source |
| [aws_iam_policy_document.read_secret](https://registry.terraform.io/providers/hashicorp/aws/4.32.0/docs/data-sources/iam_policy_document) | data source |
| [local_file.secret](https://registry.terraform.io/providers/hashicorp/local/2.2.3/docs/data-sources/file) | data source |
| [local_file.secret_trigger_workflow](https://registry.terraform.io/providers/hashicorp/local/2.2.3/docs/data-sources/file) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_api_gateway_name"></a> [api\_gateway\_name](#input\_api\_gateway\_name) | n/a | `string` | `"test-gha-trigger"` | no |
| <a name="input_function_name"></a> [function\_name](#input\_function\_name) | Lambda Function Name | `string` | `"test-gha-trigger"` | no |
| <a name="input_lambda_architecture"></a> [lambda\_architecture](#input\_lambda\_architecture) | n/a | `string` | `"arm64"` | no |
| <a name="input_lambda_role_name"></a> [lambda\_role\_name](#input\_lambda\_role\_name) | n/a | `string` | `"test-gha-trigger"` | no |
| <a name="input_region"></a> [region](#input\_region) | n/a | `string` | `"us-east-1"` | no |
| <a name="input_secretsmanager_secret_name_main"></a> [secretsmanager\_secret\_name\_main](#input\_secretsmanager\_secret\_name\_main) | n/a | `string` | `"test-gha-trigger-main"` | no |
| <a name="input_secretsmanager_secret_name_trigger_workflow"></a> [secretsmanager\_secret\_name\_trigger\_workflow](#input\_secretsmanager\_secret\_name\_trigger\_workflow) | n/a | `string` | `"test-gha-trigger-trigger-workflow"` | no |
| <a name="input_zip_path"></a> [zip\_path](#input\_zip\_path) | n/a | `string` | `"gha-trigger-lambda_linux_arm64.zip"` | no |

## Outputs

No outputs.

## LICENSE

[MIT](LICENSE)

---

This document is generated by [terraform-docs](https://terraform-docs.io/)

```console
$ terraform-docs . > README.md
```

Please see [.terraform-docs.yml](.terraform-docs.yml) and [docs](docs) too.
