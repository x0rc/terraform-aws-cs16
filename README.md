### Run CS 1.6 server on AWS

### Steps

- Install terraform, awscli are installed

#### AWS 

Create secret key and access key add that in secrets

#### Secrets

Keep the secrets in `secret.tfvars` as 

```terraform
access_key = "your access key"
secret_key = "your secret key"
region       = "eu-central-1"
instance_type       = "t2.micro"
availability_zone = "eu-central-1a"
```


#### Start (from aws folder)

```
terraform init
terraform plan  -var-file="secret.tfvars"
terraform apply  -var-file="secret.tfvars"
```

#### Stop

```
terraform destroy  -var-file="secret.tfvars"
```

