Terraform module which creates a name for infrastructure resources that follows

## Usage

### Example

```hcl
# Create a name for the EKS cluster
module "eks_name" {
  source = "git::https://github.com/agiwalpooja20/Hello?ref=v1.0.0"

  providers {
    random = "random"
  }

  environment = "${var.environment}"
  resource    = "eks"

  # Domain is only required to further specify what AWS account/team/owner/category it belongs to.
  # Otherwise, we can just omit it entirely.
  domain      = "${var.domain}"
}
```

