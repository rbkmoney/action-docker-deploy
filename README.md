# `action-deploy-docker` - **Github Action**

This action deploy docker image

## Input

| Name                 | Description                                                                                    |
| ------------------   | ---------------------------------------------------------------------------------------------- |
| `registry-username`  | Username for image registry                                                                    |
| `registry-password`  | Password for image registry                                                                    |
| `docker-registry`    | Docker image registry                                                                          |
| `aws-ecr-access-key` | Amazon ECR access key                                                                          |
| `aws-ecr-secret-key` | Amazon ECR secret key                                                                          |
| `aws-region`         | AWS region                                                                                     |
| `dokerfile-path`     | Path to dockerfile directory                                                                   |

## Example Workflow File

```yaml
name: Deploy docker image

on: [pull_request]

jobs:
  deploy:
    runs-on: ubuntu-latest
      steps:
        uses: alfaind/action-docker-deploy@v1.0.0
```
