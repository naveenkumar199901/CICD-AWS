# Terraform Create ECS with CodePipeline

You can change variables in `variables.tfvars` 

I want to create a VPC with CIDR(Classless inter-domain routing) ( 10.0.0.0/16 ), 2 public subnet and 2 private subnet.
```
vpc_cidr = "10.0.0.0/16"
environment = "production"
public_subnet_cidrs = ["10.0.0.0/24", "10.0.1.0/24"]
private_subnet_cidrs = ["10.0.50.0/24", "10.0.51.0/24"]
availibility_zones = ["us-east-1a", "us-east-1f"]
region = "us-east-1"
```

Then run the command

```
terraform init
terraform plan -var-file=vpc.tfvars
terraform apply -var-file=vpc.tfvars
```
