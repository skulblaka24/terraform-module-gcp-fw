terraform-module-gcp-fw
=======================

Module to provision three firewall rules for VMs tagged "tfe" on GCP.

Note:

It does not hold a provider configuration inside.

This can be used:
```
provider "google" {
  region  = var.region
  project = var.project_name
}
```

# Exemple main.tf:
------------------

```
module "vm_firewall_rules" {
  source  = "github.com/skulblaka24/terraform-module-gcp-fw"
}
```

Modify variables to use it.
For example, add "GOOGLE_CREDENTIALS" to be able to connect to GCP on TFC.