---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "domain-management_domain_annotations Resource - terraform-provider-domain-management"
subcategory: ""
description: |-
  Manage a domain's annotations using Terraform
---

# domain-management_domain_annotations (Resource)

Manage a domain's annotations using Terraform

## Example Usage

```terraform
resource "domain-management_domain_annotations" "example" {
  domain = "example.xyz"
  annotations = {
    "top-level/module-specific/annotations" = {
      numberExample = 69
      floatExample  = 69.69
      stringExample = "hello"
      boolExample   = false
      objectExample = {
        this = {
          is = {
            an = "object"
          }
        }
      }
      listStringExample = tolist(["a", "b", "c"])
      listNumberExample = tolist([1, 2, 3])
      listBoolExample   = tolist([true, false, true])
      listObjectExample = tolist([
        {
          type   = "weekday"
          status = "active"
        },
        {
          type   = "weekend"
          status = "dormant"
        },
      ])
    }
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `annotations` (Dynamic)
- `domain` (String) The domain name to add annotations
