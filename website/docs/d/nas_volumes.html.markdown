---
layout: "ncloud"
page_title: "NCLOUD: ncloud_nas_volumes"
sidebar_current: "docs-ncloud-datasource-nas-volumes"
description: |-
  Get NAS volume instance list
---

# Data Source: ncloud_nas_volumes

Gets a list of NAS volume instances.

## Example Usage

```hcl
data "ncloud_nas_volumes" "nas_volumes" {}
```

## Argument Reference

The following arguments are supported:

* `volume_allotment_protocol_type_code` - (Optional) Volume allotment protocol type code. All volume instances will be selected if the filter is not specified. (`NFS` | `CIFS`)
* `is_event_configuration` - (Optional) Indicates whether the event is set. All volume instances will be selected if the filter is not specified. (`true` | `false`)
* `is_snapshot_configuration` - (Optional) Indicates whether a snapshot volume is set. All volume instances will be selected if the filter is not specified. (`true` | `false`)
* `no_list` - (Optional) List of nas volume instance numbers.
* `region` - (Optional) Region code. Get available values using the data source `ncloud_regions`.
    Default: KR region.
* `zone` - (Optional) Zone code. Get available values using the data source `ncloud_zones`.
* `output_file` - (Optional) The name of file that can save data source after running `terraform plan`.

## Attributes Reference

* `nas_volumes` - A list of NAS Volume Instance no
