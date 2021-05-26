# terraform-plus-ansible

Here's our repo used to  manage DA Compute environment in SJC DMZ with code.

## Managing vSphere with Terraform

### Credentials

Credentials are intentionally not included in these files to avoid a security vulnerability. 

The variables containing the username, password, and IP (or FQDN) are flagged as `sensitive` so Terraform will prompt you for values to these variables when you run `tereraform apply`. 

Alternatively, you can create your own `secret.tfvars` file with the following contents:
```
# vSphere credentials and IP address or FQDN
vsphere_user = "<the vsphere admin username goes here>"
vsphere_password = "<the vsphere admin password goes here>"
vsphere_server = "<the vsphere IP address or FQDN goes here>"
```

Then, you can include the file by running `terraform apply -var-file="secret.tfvars"`

