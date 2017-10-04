# terraform-openstack-provider

Provide a basic configuration to use OpenStack with Terraform.

## Usage

```bash
export OS_USERNAME='foo'
export OS_TENANT_NAME='foo'
export OS_PASSWORD='foo'
export OS_AUTH_URL='foo'
export OS_REGION_NAME='foo'
```

```HCL
variable "os_username" {}
variable "os_tenant_name" {}
variable "os_password" {}
variable "os_auth_url" {}
variable "os_region" {}

module "openstack_provider" {
  source = "julienlevasseur/provider/openstack"
  username    = "${var.os_username}"
  tenant_name = "${var.os_tenant_name}"
  password    = "${var.os_password}"
  auth_url    = "${var.os_auth_url}"
  region      = "${var.os_region}"
}

```

## Authors

Julien Levasseur (https://github.com/julienlevasseur)
