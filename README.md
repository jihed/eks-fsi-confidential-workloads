# EKS FSI Confidential Workloads Reference Architecture

## Overview

This repository contains a reference architecture for deploying confidential workloads in Financial Services Industry (FSI) environments using Amazon Elastic Kubernetes Service (EKS). It provides a secure, scalable, and compliant foundation for running sensitive applications on Kubernetes.

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Deployment](#deployment)
- [Security Considerations](#security-considerations)
- [Compliance](#compliance)
- [Contributing](#contributing)
- [License](#license)

## Features

- Secure EKS cluster configuration optimized for FSI workloads
- Network isolation and segmentation
- Secrets management integration
- Automated compliance checks
- Continuous monitoring and logging
- GitOps-based deployment workflows

## Architecture

![Architecture Diagram](./docs/architecture.png)

Our reference architecture includes:

- Amazon EKS for orchestration
- AWS VPC for network isolation
- AWS Key Management Service (KMS) for encryption
- AWS Secrets Manager for secrets management
- Amazon CloudWatch for logging and monitoring
- AWS Identity and Access Management (IAM) for access control

## Prerequisites

- AWS Account with appropriate permissions
- AWS CLI configured with your credentials
- kubectl installed and configured
- Helm 3.x installed
- Terraform 1.x 

## Deployment

1. Clone this repository:
```bash
git clone https://github.com/your-username/eks-fsi-confidential-workloads.git
cd eks-fsi-confidential-workloads
```
3. Review and customize the configuration files in the `config` directory.

4. Deploy the infrastructure:
   
```bash
terraform init
terraform apply
```

4. Apply Kubernetes manifests:

```bash
kubectl create -f manifest/
```

For detailed deployment instructions, refer to our [Deployment Guide](./docs/deployment-guide.md).

## Security Considerations

- **Network Security**: VPC configuration with private subnets, NACLs, and Security Groups
- **Pod Security**: Implemented Pod Security Policies and OPA Gatekeeper
- **Data Encryption**: Encryption at rest and in transit using AWS KMS
- **Access Control**: Least privilege IAM roles and RBAC policies
- **Secrets Management**: Integration with AWS Secrets Manager and External Secrets Operator

## Compliance

This reference architecture is designed to help meet common FSI compliance requirements, including:

- PCI DSS
- SOC 2
- GDPR
- CCPA

Always consult with your compliance and legal teams to ensure all specific requirements are met.

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for more details.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.
