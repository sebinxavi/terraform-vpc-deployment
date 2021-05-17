# Terraform script for AWS VPC deployment

This Terraform module will helps to create an Amazon Web Services (AWS) Virtual Private Cloud (VPC).

## _Features of Terraform_

- Improved multi-cloud infrastructure deployment
- Automated infrastructure management
- Infrastructure as code
- Reduced development costs
- Reduced time to provision

## Prerequisites
- Terraform version - 0.15.3
- Linux operating System
-  Access keys to sign programmatic requests to the AWS CLI and the required permissions for VPC creation

# _Terraform Installation_

```sh
$ wget https://releases.hashicorp.com/terraform/0.15.3/terraform_0.15.3_linux_amd64.zip
$ unzip terraform_0.15.3_linux_amd64.zip 
$ mv terraform /usr/bin/
$ which terraform
```

### _Usage_

This module creates a VPC alongside a variety of related resources, including:

- Public and private subnets
- Public and private route tables
- Elastic IPs
- Network Interfaces
- NAT Gateways
- An Internet Gateway

## How to configure

- Open the file terraform.tfvars and edit the variables as per your requirements

```sh
region = "ap-south-1"
access_key = "Add your access key here"
secret_key = "Add your secret key here"
project = "myvpcproject.com"
vpc_cidr = "172.16.0.0/16"
```

- region = Please provide your desired AWS region in which VPC should be deployed. Example, "ap-south-1"
- access_key = This is your AWS access key.
- secret_key = This is your AWS secret key. 
- project = Please put your Project name here, Example, "myvpcproject.com"
- vpc_cidr = The CIDR block for the VPC.

For more information, read the [Terraform Documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)



## _Steps to be done_

With Terraform installed, you are ready to create your VPC infrastructure by following the below steps.

```sh
$ git clone https://github.com/sebinxavi/terraform-vpc-deployment.git
$ cd terraform-vpc-deployment
$ terraform init
$ terraform plan
$ terraform apply
```

- terraform init – this is where you initialize your code to download the requirements mentioned in your code.
- terraform plan – this is where you review changes and choose whether to simply accept them.
- terraform apply – this is where you accept changes and apply them against real infrastructure.

