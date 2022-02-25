# AWS strongDM Relay on EC2

This Terraform module creates a strongDM relay and provisions an EC2 instance
with the configured sdm daemon on it.

Example Usage
```hcl
module "relay" {
  source  = "truemark/strongdm-relay-ec2/aws"
  name = "myrelay"
  ssh_allowed_cidr_blocks = local.ssh_allowed
  vpc_id = "<VPC ID>"
  subnet_id = "<SUBNET ID>"
  ssh_keys = [
      "ssh-rsa <SSH_KEY>",
      "ssh-rsa <SSH_KEY>",
  ]
}
```
