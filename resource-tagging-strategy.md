Please [refer here](https://github.com/e2eSolutionArchitect/terraform/blob/main/docs/tagging.md)

Recommended primary set of tags for Cost Management are 'CostCenter','WorkloadName','Environment'
```
locals {
  name = "${var.project}-${var.prefix}"
  tags = {
    project      = var.project
    orgunit      = var.org_unit
    businessunit = var.business_unit
    costcenter   = var.cost_center
    workloadname = var.workloadname
    desc         = var.desc
    tier         = var.tier
    createdby    = var.created_by
    createdon    = timestamp()
    environment  = var.env
    owner = var.owner
    supportcentre = var.email_support_centre
  }
}

```
