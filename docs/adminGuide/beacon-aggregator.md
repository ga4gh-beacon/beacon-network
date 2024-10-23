---
title: "Aggregator"
date: 2024-10-22
layout: default
parent: "Installation"
nav_order: 3
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Beacon Aggregator

The Beacon Aggregator (BA) is the agent in charge of querying the Beacons of the network and gather the results. It also aggregates and parses their metadata.

## Meta-Beacon

The Beacon Aggregator is itself a standard Beacon v2. As it is created to query other Beacons, it is referred to as Meta-Beacon.

In order to differentiate the Meta-Beacon to a simple Beacon, besides having aggregation functionalities, we have listed the following additional properties:

- `isBeaconNetwork`: If `true`, it means that the beacon is a Meta-Beacon.
- `beaconId`: Unique identifier for each beacon. It is needed to differentitate where the data comes in a network.

All the beacons in a network also need to have the `beaconId` in their `info` page, as it is needed for the EBN to differentiate each instance.

## Query Policies

The Beacon aggregator sends the query to the multiple Beacons in the network. To reduce to the minimum the queries sent, thus reducing the payload of the server, it follows these policies:

 - First, if a Beacon requires authentication, the BA must provide a header with the authentication of the user to the given Beacon. If the authentication is not needed, it goes to the next step.

 - The BA parses the `/map` endpoint and looks if the Beacon has the model schema needed (individuals, biosamples, etc).

 - Check if the filtering terms of the query exists.

 - In the network, there can be Beacons with different schemas, such as Phenopackets or different versions of Beacon. If the network is not able to read these schemas, it must quit the query for the given Beacon.

