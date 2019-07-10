# SA Lauch Demo

## Terraform Create ECS with CodePipeline

You can change variables in `variables.tfvars` , 

For example: I want to create a VPC with CIDR ( 10.0.0.0/16 ), two public subnet and two private subnet.

```
vpc_cidr = "10.0.0.0/16"
environment = "production"
public_subnet_cidrs = ["10.0.0.0/24", "10.0.1.0/24"]
private_subnet_cidrs = ["10.0.50.0/24", "10.0.51.0/24"]
availibility_zones = ["eu-west-2a", "eu-west-2b"]
region = "eu-west-2"
ami_image = "ami-09568291a9d6c804c"
ecs_key = "demo"
instance_type = "t2.medium"
repo_owner = "ibuchh"
repo_name = "salaunch-ecs-cicd"
github_oauth_token = "********************"

```

Then run

```
terraform init
terraform plan -var-file=variables.tfvars
terraform apply -var-file=variables.tfvars
```
