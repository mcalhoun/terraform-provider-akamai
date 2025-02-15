---
layout: "akamai"
page_title: "Shared Resources"
description: |-
  Shared Resources
---

# Shared Resources

Find information that applies to multiple Akamai Provider modules.

## Domain Suffixes for Different Edge Hostname Types

Each type of edge hostname has its own domain suffix. Knowing which one to use is important when creating edge hostnames:

| Edge Hostname Type | Domain Suffix |
|--------------------|---------------|
| Enhanced TLS       | `edgekey.net` |
| Standard TLS       | `edgesuite.net` |
| Shared Cert        | `akamaized.net` |
| Non-TLS            | `edgesuite.net` |

## Secure Hostnames

For secure hostnames you must include the certificate enrollment ID in your [`akamai_edge_hostname` resource](../resources/edge_hostname.md).

1. Retrieve the `enrollment-id` from the [Certificate Provisioning Service CLI](https://github.com/akamai/cli-cps).
2. Enter the ID as the certificate attribute.

## Common Product IDs

For some data sources and resources, you need to retrieve the ID for the specific Akamai product you are using. The following is a list of commonly used IDs for different products:

| Product | Code |
|---|---|
| **Web Performance Solutions**                   |
| Dynamic Site Accelerator | `prd_Site_Accel` |
| Ion Standard             | `prd_Fresca`     |
| Ion Premier          | `prd_SPM`        |
| Dynamic Site Delivery | `prd_Site_Del` |
| Rich Media Accelerator   | `prd_Rich_Media_Accel` |
| IoT Edge Connect | `prd_IoT` |
| **Security Solutions**          |         |
| Kona Site Defender | `prd_Site_Defender` |
| **Media Delivery Solutions**          |         |
| Download Delivery | `prd_Download_Delivery` |
| Object Delivery | `prd_Object_Delivery` |
| Adaptive Media Delivery | `prd_Adaptive_Media_Delivery` |

Note that if you have previously used the Property Manager API or CLI `set-prefixes` toggle option, you might have to remove the `prd_` prefix
