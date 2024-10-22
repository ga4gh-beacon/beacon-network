---
title: Governance Model
date: 2024-10-22
layout: default
nav_order: 2
---

# Governance Model

1. # Vision statement

**The ELIXIR Beacon Network (EBN) aims to act as a resource to facilitate biomedical data discoverability across multiple sites and data types, given stable and community-driven specifications governing the interactions of the different associated resources.** The Global Alliance for Genomics and Health (GA4GH) and ELIXIR constitute the two main EBN reference organisations for community-driven standards and their implementation into software products that can be uptaken by the whole Life Sciences community.

2. # Overview and scope.


### Overview

The ELIXIR Beacon Network (EBN) is a service to support a collaborative initiative to advance data discoverability across the biomedical community. Developed under ELIXIR, the network creates an interconnected ecosystem of beacons, fostering responsible sharing of genomic, phenotypic and other data types.

The main objectives of the ELIXIR Beacon Network are:

- Facilitating data accessibility: Promoting easy discoverability, use, and access to diverse biomedical data types for researchers and other interested stakeholders.

- Interoperability: Ensuring compatibility among different data sources by adopting  standardised Beacon protocol and data models.

- Knowledge exchange: Bringing different data providers together serves to identify commonalities and differences across sites, facilitating expert knowledge exchange and the promotion and adoption of standardised protocols across the community.


### Structure

The governance structure is designed to facilitate transparent decision-making, both strategic and operational, and community involvement. The key parts are:

- Roles, Bodies and Responsibilities in the EBN

- Governance rules for the different Roles and Bodies

- Appendixes that describe details on particular aspects.

The considerations for expected operations, such as relevant and contextual considerations for the governance in the different operations inside the EBN and what makes a Beacon operational in the network are in the [ELIXIR Beacon Network Operations document](https://docs.google.com/document/d/1GfCztXyPIN3m0dY-1RGZQac0EUqzFCACnAdnq4XrgDQ/edit).


# 3. Roles, Bodies and Responsibilities

This section lists roles, bodies and responsibilities in the ELIXIR Beacon Network:


### Users

User is anyone querying EBN. As an example, a user can be a researcher searching for individuals with a certain disease across multiple beacons. Users could be anonymous or registered.


#### Anonymous Users

Anonymous users refer to individuals who are not registered or do not pass any authentication in the ELIXIR Beacon Network. Such users are limited to accessing only the public beacons, with access restricted to the default level of granularity of each beacon.


#### Registered Users

Registered users are those who have logged into EBN. Whenever these users initiate a query, EBN will transmit their identity to the beacons within the network.


### Beacon Maintainer

Beacon maintainers are the people in charge of the beacons that have been included in the network, or want to be in the network. They are responsible for overseeing the operations and functionalities of their respective beacons.

They are the primary point of contact with the EBN Maintainer, facilitating the addition or update of their beacons within the network. Additionally, they are tasked with notifying the EBN Maintainer of any errors in their beacon that could impact the network's performance.

Before asking permission to enter the ELIXIR Beacon Network, they must pass their beacon to the [validator](https://github.com/elixir-europe/neat-beacon-v2-validator) to ensure their beacon is complying with the specification.


### ELIXIR Beacon Network Maintainer

Responsible for the operations of the ELIXIR Beacon Network instance or instances. They control the actual addition or updating of beacons within the network. Also, they serve as the primary operational point of contact for beacon owners and are responsible for notifying them of any issues, such as beacon downtime or errors.

Additionally, these individuals are tasked with ensuring the continuous operation of the ELIXIR Beacon Network and keeping it up to date, according to the service level agreement (SLA). 

This role could be split into several individuals or subroles, e.g.: customer support and EBN System Administration.

The EBN Maintainer is selected by the Steering Committee. It must be a person with access to the system where the EBN backend is located.


### Contributors

Contributors are community members who help maintain and develop the ELIXIR Beacon Network. Any person can contribute. Participation is open to anyone, with no expectation of long-term commitment, specific skill requirements, or selection process.

Contributions can take multiple forms such as reporting bugs, writing documentation, contributing code (e.g. new model schemas). Any form of contribution is welcome, and it will be recognized.


### Steering CommitteeBeacon Maintainer at least one member from the contributing communities.

The members are typically nominated and elected by the existing committee (Derived from the Service Founding Committee at M1.1) or through a vote by the contributing community members. The selection criteria prioritise diversity in expertise and community representation, with a balance between technical and project perspectives.

The Steering Committee holds regular mandatory meetings, typically on a quarterly basis, to discuss the progress, challenges, and strategic direction of the EBN. Additional meetings can be convened as needed. Agendas for these meetings are set in advance and typically include:

1. Review of Project Goals and Progress: Assessing current milestones and setting future objectives.

2. Technical Developments: Evaluating new technical proposals, updates, and innovations.

3. Governance and Administrative Matters: Addressing any issues related to governance, member roles, and administrative duties.

4. Policy Development and Updates: Discussing and approving new policies or modifications to existing ones.


### Operations Team

Specialists responsible for the technical infrastructure and development of the network. Their primary focus is on developing the network, implementing extensions and ensuring interoperability to enhance its functionality and efficiency.

This committee is composed by contributors of the ELIXIR Beacon Network. It is also encouraged that the members of contributing communities help the development together with the Steering Committee.

Disaster Recovery team


### Training and outreach

Anyone related to the EBN can do training or participate in outreach activities. Before doing so, they must send a mail to <bn-contact@elixir-europe.org> to inform them of the activity, and get any possible help from the community or any other valuable assistance.


### SC Chair

The SC Chair is a single individual, a member of the Steering Committee, and elected for a 2-year non-renewable term by the SC, with the expectation that this role should rotate between its members. The Chair has no additional authority over other members of the Steering Committee: the role is one of coordinator. The Chair is also expected to ensure that all governance processes are adhered to, and has the casting vote when the project fails to reach consensus.


# 3. Expected operations within the ELIXIR Beacon Network

The expected operations of the EBN revolve around ensuring smooth functioning, growth and ethical management of the service.

Information related to customer support is described in the [ELIXIR Beacon Network Customer Support Model](https://docs.google.com/document/d/1rarBVaBMq4V6TO7BKe0yd0cgu16hW6OpwK7i6F5tNGg/edit).


### Querying system

The ELIXIR Beacon Network (EBN) holds primary responsibility for querying all beacons within its network. The granularity of responses provided by each beacon is contingent upon the user's access level to that particular beacon. Moreover, the EBN has the authority to determine which terms are searchable and which are restricted, thereby empowering the Steering Committee to manage data privacy and facilitate access to genomic and phenotypic information.

User queries must conform to the schema of the beacons to generate potentially positive results. If a query deviates from the version of the Beacon protocol supported by the aggregator a specific beacon's schema, the beacon will respond negatively. This protocol ensures that users receive accurate and relevant information consistent with the capabilities of each beacon within the network.


### Add Beacons

To include a Beacon in the ELIXIR Beacon Network (EBN), it must first receive acceptance from the ELIXIR Beacon Network Maintainer.

The criteria for admission into the network will be outlined by the Steering Committee. If a Beacon aligns completely with the criteria, such as being associated with a designated ELIXIR project, it will be automatically integrated into the network by the EBN Maintainer. In case the EBN Maintainer has uncertainty regarding the Beacon's alignment with the criteria, the matter will be referred to the Steering Committee for discussion. Consequently, the Steering Committee bears responsibility for the beacons in their network.

In addition to meeting the Steering Committee's criteria, the following minimum requirements must be satisfied for a Beacon to be added:

1. Versioning: The Beacon must be version 2.0 or higher.

2. Availability: The Beacon must be operational and accessible for querying upon integration into the network. More information about what is a Beacon being operational in the section [Service Level Agreement (SLA) for Operational Beacons in the ELIXIR Beacon Network](#service-level-agreement-sla-for-operational-beacons-in-the-elixir-beacon-network-1).

3. Specification: The properties within the Beacon must conform to the expected schema, including essential properties like BeaconId.

4. Endpoints: The Beacon must possess at least one endpoint for querying, along with endpoints necessary for metadata retrieval.

5. Data: While it is not obligatory for a Beacon to contain data upon integration into the network, it is recommended to utilise synthetic data if authentic data is unavailable.


### Remove Beacons

The individual responsible for removing beacons from the network is the EBN Maintainer. The removal process is initiated under the following circumstances:

1. A Beacon Maintainer expresses a desire to withdraw from the ELIXIR Beacon Network.

2. A decision is reached by the Steering Committee.

3. A beacon remains non-operational for a specified duration, as determined by the Steering Committee.

4. A beacon significantly compromises the network's performance or security.


### Validate a Beacon

Before integration into the ELIXIR Beacon Network (EBN), a beacon must undergo validation. If the validation process concludes without errors, the beacon is deemed suitable for inclusion in the network. However, if errors are detected during validation, and they do not pose significant risks to querying the beacon or to the EBN itself, the decision to integrate the beacon rests with the EBN Maintainer.


### Load-Balance

The Load-Balance server must be hosted at a minimum of two distinct institutions, as designated by the Steering Committee, each of which must possess adequate funding for EBN maintenance.

If an institution becomes unable to support the Load-Balance approach, a meeting with the Steering Committee is required to arrange for the allocation of a new server for subsequent deployment. If no institution is available for server allocation, an open project will be initiated for any institution to submit proposals.

All institutions implementing the Load-Balance approach within the ELIXIR Beacon Network must maintain consistent versions of the network. Any updates to the EBN must be synchronised across all deployments, ensuring uniformity in network versions.

The Load-Balance approach is not mandatory. It is up to the SC to decide if it is suitable to use it or use another approach, such as having the EBN in the cloud.


### Registration/Authorization

Users are required to include the appropriate token with each query, whether utilising the direct API or the FrontEnd interface. This token functions as both authentication and authorization, providing the necessary level of access to query the beacons within the ELIXIR Beacon Network with the desired granularity.


### Product updates and maintenance

Any modification to the ELIXIR Beacon Network requires validation by at least two members of the Steering Committee and two members of the Operations Team. Users of the EBN have the ability to create their own branches or forks. However, any additions, removals, or updates to the main or development code must be submitted as pull requests to the main/dev branch of the repository.

To initiate a new version of the ELIXIR Beacon Network, approval from all SC members is necessary. Subsequently, an email must be circulated to all participating EBNs in the Load-Balance approach to coordinate the timing of their deployment updates. Finally, an email must be sent to all participants via the EBN mailing list.


### Monitoring

It is up to the Steering Committee to decide which statistics and how to monitor the EBN. The EBN maintainer is the one responsible to be in contact with the Operations Team for deploying the monitorisation, and report it to the Steering Committee (it must be done at least once a year). Also, they are responsible to contact the Disaster Recovery Coordinator when an incident has been detected.


### Documentation and training

Documentation and training for the EBN are continuously evolving to meet the needs of its users. Any user of the EBN has the opportunity to contribute to the documentation. However, any proposed additions, removals, or updates to the documentation must receive approval from at least two members of the Steering Committee or the Operations Team.

Training programs may be conducted by any interested individual. Prior to conducting training, notification and relevant information must be provided to the Steering Committee for assistance and coordination. Additionally, the ELIXIR Training program, accessible via TeSS, can offer valuable resources and support for training initiatives.


# Service Level Agreement (SLA) for Operational Beacons in the ELIXIR Beacon Network

This Service Level Agreement (SLA) outlines the standards and expectations for maintaining an Operational Beacons within the ELIXIR Beacon Network v2. It aims to ensure a consistent and high-quality user experience, facilitate interoperability, and uphold the network's overall reliability and integrity.


### Operational Requirements

- Compliance: Beacons must comply with the ELIXIR Beacon Network v2 specifications and standards.

- Interoperability: Beacons must support interoperability with other Beacons in the network, including standardised query formats and response protocols.

- Data Quality: Beacons must ensure the accuracy, completeness, and timeliness of the genomic data they host.


### Performance Metrics

- Response Time: Beacons must respond to queries within 30 seconds under normal operating conditions.

- Throughput: Beacons must handle a minimum of 100 concurrent queries without performance degradation.


### Service Availability

- Uptime: Beacons must maintain a minimum uptime of 99.5% on a monthly basis.

- Scheduled Maintenance: Beacon operators must notify the ELIXIR Beacon Network Management of any scheduled maintenance at least 72 hours in advance. Maintenance windows should be scheduled during off-peak hours to minimise user impact.

- Unscheduled Downtime: In the event of unscheduled downtime, Beacon operators must notify the ELIXIR Beacon Network Management within 30 minutes of the incident.


### Incident Management

- Incident Reporting: Beacon operators must report any incidents affecting service availability or performance to the ELIXIR Beacon Network Management immediately.

- Incident Resolution: Beacon operators must resolve incidents affecting service availability or performance within 4 hours. For major incidents, a root cause analysis must be provided within 24 hours of resolution.

- Escalation: If an incident cannot be resolved within the stipulated time, it must be escalated to the ELIXIR Beacon Network Management for further assistance.


### Support and Maintenance

- Support Availability: Beacon maintainers must provide support for their Beacons during regular business hours.

- Maintenance Practices: Beacon maintainers must perform regular maintenance to ensure optimal performance and compliance with security standards. This includes applying software updates, patching vulnerabilities, and monitoring system health.


### Responsibilities

- Beacon Maintainers: Ensure compliance with all operational requirements and performance metrics outlined in this SLA. Maintain the accuracy and quality of the data hosted by the Beacon. Provide timely support and incident resolution as specified.

- ELIXIR Beacon Network Maintainer: Monitor the performance and availability of Beacons within the network. Provide guidance and support to Beacon operators to help them meet SLA commitments. Coordinate network-wide maintenance and updates to ensure interoperability and performance. Review incident reports and facilitate root cause analysis and resolution.


# 5. Communication channels

The official communication channels for user support and project discussions in general are:

- The official contact email, <bn-contact@elixir-europe.org> , which goes to all members of the project.

- The Gitter messaging system channel for the ecosystem.

- Via issues in any of the [Beacon Network repositories](https://github.com/elixir-europe/beacon-network).


# 6. Support

All participants in the community are encouraged to provide support for new users and contributors. This support is part of the ELIXIR Beacon Network, and is provided as a way to encourage reuse and contributions to the service. Support is provided on the communication channels listed in the previous section.

The types of support given can be the following:

- Frequently Asked Questions (FAQs): Used for common queries about beacon registration, data submission and more. You can use the mail, the Gitter messaging system or the documentation for these questions.

- Documentation: Detailed documentation for in-depth information on how to create an instance of a EBN.

- Contact support: For any specific queries or required personalised assistance, you can send a mail to <bn-contact@elixir-europe.org>.

- Training programs: Participating in different training programs to enhance your basic understanding of beacon operations and best practices.

- Feedback submission: You can support with your thoughts, suggestions and bug reports to help continuously improve the EBN.


# 7. Contribution Process and credit

Anyone can contribute to the project, regardless of their skills, as there are many ways to contribute. The Gitter channel is the most appropriate place for a contributor to ask for help when making their first contribution.

Contributions can take multiple forms, such as:

- Issues in the GitHub repositories ([Backend](https://github.com/elixir-europe/beacon-network-backend) and [FrontEnd](https://github.com/elixir-europe/beacon-network-ui)).

- Providing or improving code that adds or improves the product or more generally, maintains the infrastructure.

- Contributing to the documentation of the project.

The various ways of contributing are described in more detail in the [Administration document](https://docs.google.com/document/d/1_NjSqGtoAVlgpWOLvcOCYdDJMsBY8lCrcqk4Fu43wmM/edit?usp=sharing).


# 8. Decision Making Process

A robust and transparent decision-making process is fundamental to the success of the ELIXIR Beacon Network. These are the parts of the governance:

- Simple decisions: such as the updating of libraries and minimal changes in the project, will be subject to positive votes in any of GitHub's repositories.

* Steering Committee Authority: They hold the ultimate decision-making authority, guiding the strategic direction and policies of the ELIXIR Beacon Network. Their decisions are related to the network governance, policy changes and overall project goals.

* Community engagement: Decision-making involves active engagement with the community, including beacon operators, data providers and other stakeholders. Soliciting feedback from the community, working groups and diverse projects is key to ensuring diverse perspectives to improve the product.

* Decision criteria: Technical feasibility, ethical considerations, impact assessments and alignment with ELIXIR’s mission.

* Decision records: Comprehensive documentation of the decision to maintain transparency and accountability as a reference for future discussions.

* Timeliness and accountability: Ensure timely decision-making while avoiding unnecessary delays and addressing urgent matters promptly.

* Continuous improvement: Regular evaluation and refinement of the decision-making process. Iterative improvements based on feedback, changing project dynamics and community needs.