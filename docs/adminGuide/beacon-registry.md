---
title: "Registry"
date: 2024-10-22
layout: default
parent: "Installation"
nav_order: 4
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Beacon Registry

The role of the Beacon registry is to check the Beacons available in the network and gather their basic information. 

## Cache

The cache of the registry store the following information about the Beacons:

- Entry types available to search.

- Type of schemas for representing data and metadata.

- Filtering terms that the beacon support.

- Authentication/Authorization mechanism needed to ensure that only authorized users access the data.

- Basic metadata from the `info` endpoint.

As it can be seen, the data stored in the cache is directly related with the queries policy. So, it needs to be updated every time there is a change in any Beacon.

## Update Registry

Beacon Aggregator will check if the `updateDateTime` property has changed since the last time a Beacon has been updated. If true, I will reload again all the cache of such Beacon.

If a Beacon maintainer wants to force an update of the metadata, they should run the following in the terminal:

```
 curl -H "Accept: application/json" -H "Cache-Control: no-cache" {url_of_your_ebn}/info
```

## Status

Heartbeat mechanism that regularly checks the status of the Beacons in the network. This ensures the availability of the different Beacons when querying. (Still in development)
