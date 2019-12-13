# CICD-AWS
## Terraform Create ECS with CodePipeline

if you want change variables in `variables.tfvars` ,
Create the requirement.txt in the web folder
```paste  Flask==0.12.2```
For example: want to create a VPC with CIDR (e.g 10.0.0.0/16 ), two public subnet and two private subnet.

```
vpc_cidr = "10.0.0.0/16"
environment = "production"
public_subnet_cidrs = ["10.0.0.0/26", "10.0.1.0/26"]
private_subnet_cidrs = ["10.0.50.0/26", "10.0.51.0/26"]
availibility_zones = ["us-east-1a", "us-east-1b"]
region = "us-east-1"
ami_image = "ami-04763b3055de4860b"
ecs_key = "cicd"
instance_type = "t2.medium"
repo_owner = "naveenkumar199901"
repo_name = "cicd-aws"
github_oauth_token = "github_oauth_token"

```
Change the key name for your key name 
run

```
terraform init
terraform plan -var-file=variables.tfvars
terraform apply -var-file=variables.tfvars
