# Terraform AWS VPC Infrastructure

This Terraform configuration sets up a Virtual Private Cloud (VPC) infrastructure on AWS, including public and private subnets, route tables, internet gateway, NAT gateway, and associated resources.

## Prerequisites

Before using this Terraform configuration, ensure you have the following prerequisites:

- [Terraform](https://www.terraform.io/downloads.html) installed on your local machine.
- AWS credentials configured either via environment variables or AWS CLI.
- Basic understanding of Terraform and AWS services.

## Diagram
![33](https://github.com/nessamutia/Deploying-AWS-Infrastructure-using-Terraform/assets/137209546/a92361f5-5b1e-459a-b5a9-8b004d925433)

- Private subnets are not exposed to the internet, while public subnets are.
- The public route table has a default route pointing to an internet gateway, allowing traffic to flow to and from the internet. The private route table has a default route pointing to a NAT gateway, allowing outbound
  internet access for resources in the private subnet.
- Internet gateway allows resources within the VPC to access the internet via the public subnets.

