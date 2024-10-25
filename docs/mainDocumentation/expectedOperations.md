---
title: "Expected Operations"
date: 2024-10-22
layout: default
parent: "Governance Model"
nav_order: 1
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Expected operations within the ELIXIR Beacon Network

The expected operations of the EBN revolve around ensuring smooth functioning, growth and ethical management of the service.

Information related to customer support is described in the [ELIXIR Beacon Network Customer Support Model](https://docs.google.com/document/d/1rarBVaBMq4V6TO7BKe0yd0cgu16hW6OpwK7i6F5tNGg/edit).


## Querying system

The ELIXIR Beacon Network (EBN) holds primary responsibility for querying all beacons within its network. The granularity of responses provided by each beacon is contingent upon the user's access level to that particular beacon. Moreover, the EBN has the authority to determine which terms are searchable and which are restricted, thereby empowering the Steering Committee to manage data privacy and facilitate access to genomic and phenotypic information.

User queries must conform to the schema of the beacons to generate potentially positive results. If a query deviates from the version of the Beacon protocol supported by the aggregator a specific beacon's schema, the beacon will respond negatively. This protocol ensures that users receive accurate and relevant information consistent with the capabilities of each beacon within the network.

## Add Beacons

To include a Beacon in the ELIXIR Beacon Network (EBN), it must first receive acceptance from the ELIXIR Beacon Network Maintainer.

The criteria for admission into the network will be outlined by the Steering Committee. If a Beacon aligns completely with the criteria, such as being associated with a designated ELIXIR project, it will be automatically integrated into the network by the EBN Maintainer. In case the EBN Maintainer has uncertainty regarding the Beacon's alignment with the criteria, the matter will be referred to the Steering Committee for discussion. Consequently, the Steering Committee bears responsibility for the beacons in their network.

In addition to meeting the Steering Committee's criteria, the following minimum requirements must be satisfied for a Beacon to be added:

1. Versioning: The Beacon must be version 2.0 or higher.

2. Availability: The Beacon must be operational and accessible for querying upon integration into the network. More information about what is a Beacon being operational in the section [What makes a Beacon operational in the ELIXIR Beacon Network](#what-makes-a-beacon-operational-in-the-elixir-beacon-network).

3. Specification: The properties within the Beacon must conform to the expected schema, including essential properties like BeaconId.

4. Endpoints: The Beacon must possess at least one endpoint for querying, along with endpoints necessary for metadata retrieval.

5. Data: While it is not obligatory for a Beacon to contain data upon integration into the network, it is recommended to utilise synthetic data if authentic data is unavailable.

## Remove Beacons

The individual responsible for removing beacons from the network is the EBN Maintainer. The removal process is initiated under the following circumstances:

1. A Beacon Maintainer expresses a desire to withdraw from the ELIXIR Beacon Network.

2. A decision is reached by the Steering Committee.

3. A beacon remains non-operational for a specified duration, as determined by the Steering Committee.

4. A beacon significantly compromises the network's performance or security.

## Validate a Beacon

Before integration into the ELIXIR Beacon Network (EBN), a beacon must undergo validation. If the validation process concludes without errors, the beacon is deemed suitable for inclusion in the network. However, if errors are detected during validation, and they do not pose significant risks to querying the beacon or to the EBN itself, the decision to integrate the beacon rests with the EBN Maintainer.

## Load-Balance

The Load-Balance server must be hosted at a minimum of two distinct institutions, as designated by the Steering Committee, each of which must possess adequate funding for EBN maintenance.

If an institution becomes unable to support the Load-Balance approach, a meeting with the Steering Committee is required to arrange for the allocation of a new server for subsequent deployment. If no institution is available for server allocation, an open project will be initiated for any institution to submit proposals.

All institutions implementing the Load-Balance approach within the ELIXIR Beacon Network must maintain consistent versions of the network. Any updates to the EBN must be synchronised across all deployments, ensuring uniformity in network versions.

The Load-Balance approach is not mandatory. It is up to the SC to decide if it is suitable to use it or use another approach, such as having the EBN in the cloud.

## Registration/Authorization

Users are required to include the appropriate token with each query, whether utilising the direct API or the FrontEnd interface. This token functions as both authentication and authorization, providing the necessary level of access to query the beacons within the ELIXIR Beacon Network with the desired granularity.

## Product updates and maintenance

Any modification to the ELIXIR Beacon Network requires validation by at least two members of the Steering Committee and two members of the Operations Team. Users of the EBN have the ability to create their own branches or forks. However, any additions, removals, or updates to the main or development code must be submitted as pull requests to the main/dev branch of the repository.

To initiate a new version of the ELIXIR Beacon Network, approval from all SC members is necessary. Subsequently, an email must be circulated to all participating EBNs in the Load-Balance approach to coordinate the timing of their deployment updates. Finally, an email must be sent to all participants via the EBN mailing list.

## Monitoring

It is up to the Steering Committee to decide which statistics and how to monitor the EBN. The EBN maintainer is the one responsible to be in contact with the Operations Team for deploying the monitorisation, and report it to the Steering Committee (it must be done at least once a year). Also, they are responsible to contact the Disaster Recovery Coordinator when an incident has been detected.

## Documentation and training

Documentation and training for the EBN are continuously evolving to meet the needs of its users. Any user of the EBN has the opportunity to contribute to the documentation. However, any proposed additions, removals, or updates to the documentation must receive approval from at least two members of the Steering Committee or the Operations Team.

Training programs may be conducted by any interested individual. Prior to conducting training, notification and relevant information must be provided to the Steering Committee for assistance and coordination. Additionally, the ELIXIR Training program, accessible via TeSS, can offer valuable resources and support for training initiatives.

# What makes a Beacon operational in the ELIXIR Beacon Network

This section outlines the standards and expectations for maintaining an Operational Beacons within the ELIXIR Beacon Network v2. It aims to ensure a consistent and high-quality user experience, facilitate interoperability, and uphold the network's overall reliability and integrity. This **section is aimed at Beacon owners** with a Beacon inside the network.

## Operational Requirements

- Compliance: Beacons must comply with the ELIXIR Beacon Network v2 specifications and standards.

- Interoperability: Beacons must support interoperability with other Beacons in the network, including standardised query formats and response protocols.

- Data Quality: Beacons must ensure the accuracy, completeness, and timeliness of the genomic data they host.

## Performance Metrics

- Response Time: Beacons must respond to queries within 30 seconds under normal operating conditions.

- Throughput: Beacons must handle a minimum of 100 concurrent queries without performance degradation.

## Service Availability

- Uptime: Beacons must maintain a minimum uptime of 99.5% on a monthly basis.

- Scheduled Maintenance: Beacon operators must notify the ELIXIR Beacon Network Management of any scheduled maintenance at least 72 hours in advance. Maintenance windows should be scheduled during off-peak hours to minimise user impact.

- Unscheduled Downtime: In the event of unscheduled downtime, Beacon operators must notify the ELIXIR Beacon Network Management within 30 minutes of the incident.

## Incident Management

- Incident Reporting: Beacon operators must report any incidents affecting service availability or performance to the ELIXIR Beacon Network Management immediately.

- Incident Resolution: Beacon operators must resolve incidents affecting service availability or performance within 4 hours. For major incidents, a root cause analysis must be provided within 24 hours of resolution.

- Escalation: If an incident cannot be resolved within the stipulated time, it must be escalated to the ELIXIR Beacon Network Management for further assistance.

## Support and Maintenance

- Support Availability: Beacon maintainers must provide support for their Beacons during regular business hours.

- Maintenance Practices: Beacon maintainers must perform regular maintenance to ensure optimal performance and compliance with security standards. This includes applying software updates, patching vulnerabilities, and monitoring system health.

## Responsibilities

- Beacon Maintainers: Ensure compliance with all operational requirements and performance metrics outlined in this section. Maintain the accuracy and quality of the data hosted by the Beacon. Provide timely support and incident resolution as specified.

- ELIXIR Beacon Network Maintainer: Monitor the performance and availability of Beacons within the network. Provide guidance and support to Beacon operators to help them meet the requirements. Coordinate network-wide maintenance and updates to ensure interoperability and performance. Review incident reports and facilitate root cause analysis and resolution.