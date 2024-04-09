# Basic Terraform Commands and Configuration

## 1. Initialize Terraform:
```
terraform init
```

## 2. Create Execution Plan:
```
terraform plan
```

## 3. Apply Changes:
```
terraform apply
```

## 4. Destroy Resources:
```
terraform destroy
```

## 5. Validate Configuration:
```
terraform validate
```

# Configuration

## 6. Define Provider:
```
provider "aws" {
  region = "us-east-1"
}
```

## 7. Define Resource (e.g., EC2 Instance):
```
resource "aws_instance" "example" {
  ami           = "ami-12345678"
  instance_type = "t2.micro"
}
```

## 8. Define Variable:
```
variable "instance_count" {
  type    = number
  default = 1
}
```

## 9. Define Output:
```
output "instance_public_ip" {
  value = aws_instance.example.public_ip
}
```

## 10. Define Module:
```
module "vpc" {
  source = "./modules/vpc"
}
```








