---
title: "Governance Model"
date: 2024-10-22
layout: default
parent: "Documentation"
has_children: true
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

# Governance Model

# 1. Vision statement

The ELIXIR Beacon Network (EBN) aims to act as a resource to facilitate biomedical data discoverability across multiple sites and data types, given stable and community-driven specifications governing the interactions of the different associated resources. The Global Alliance for Genomics and Health (GA4GH) and ELIXIR constitute the two main EBN reference organisations for community-driven standards and their implementation into software products that can be uptaken by the whole Life Sciences community.

# 2. Overview and scope.

## Overview

The ELIXIR Beacon Network (EBN) is a service to support a collaborative initiative to advance data discoverability across the biomedical community. Developed under ELIXIR, the network creates an interconnected ecosystem of beacons, fostering responsible sharing of genomic, phenotypic and other data types.

The main objectives of the ELIXIR Beacon Network are:

- Facilitating data accessibility: Promoting easy discoverability, use, and access to diverse biomedical data types for researchers and other interested stakeholders.

- Interoperability: Ensuring compatibility among different data sources by adopting  standardised Beacon protocol and data models.

- Knowledge exchange: Bringing different data providers together serves to identify commonalities and differences across sites, facilitating expert knowledge exchange and the promotion and adoption of standardised protocols across the community.


## Structure

The governance structure is designed to facilitate transparent decision-making, both strategic and operational, and community involvement. The key parts are:

- Roles, Bodies and Responsibilities in the EBN

- Governance rules for the different Roles and Bodies

- Appendixes that describe details on particular aspects.

The considerations for expected operations, such as relevant and contextual considerations for the governance in the different operations inside the EBN and what makes a Beacon operational in the network are in the [ELIXIR Beacon Network Operations document](https://docs.google.com/document/d/1GfCztXyPIN3m0dY-1RGZQac0EUqzFCACnAdnq4XrgDQ/edit).


# 3. Roles, Bodies and Responsibilities

This section lists roles, bodies and responsibilities in the ELIXIR Beacon Network:


## Users

User is anyone querying EBN. As an example, a user can be a researcher searching for individuals with a certain disease across multiple beacons. Users could be anonymous or registered.


### Anonymous Users

Anonymous users refer to individuals who are not registered or do not pass any authentication in the ELIXIR Beacon Network. Such users are limited to accessing only the public beacons, with access restricted to the default level of granularity of each beacon.


### Registered Users

Registered users are those who have logged into EBN. Whenever these users initiate a query, EBN will transmit their identity to the beacons within the network.


## Beacon Maintainer

Beacon maintainers are the people in charge of the beacons that have been included in the network, or want to be in the network. They are responsible for overseeing the operations and functionalities of their respective beacons.

They are the primary point of contact with the EBN Maintainer, facilitating the addition or update of their beacons within the network. Additionally, they are tasked with notifying the EBN Maintainer of any errors in their beacon that could impact the network's performance.

Before asking permission to enter the ELIXIR Beacon Network, they must pass their beacon to the [validator](https://github.com/elixir-europe/neat-beacon-v2-validator) to ensure their beacon is complying with the specification.


## ELIXIR Beacon Network Maintainer

Responsible for the operations of the ELIXIR Beacon Network instance or instances. They control the actual addition or updating of beacons within the network. Also, they serve as the primary operational point of contact for beacon owners and are responsible for notifying them of any issues, such as beacon downtime or errors.

Additionally, these individuals are tasked with ensuring the continuous operation of the ELIXIR Beacon Network and keeping it up to date, according to the service level agreement (SLA). 

This role could be split into several individuals or subroles, e.g.: customer support and EBN System Administration.

The EBN Maintainer is selected by the Steering Committee. It must be a person with access to the system where the EBN backend is located.


## Contributors

Contributors are community members who help maintain and develop the ELIXIR Beacon Network. Any person can contribute. Participation is open to anyone, with no expectation of long-term commitment, specific skill requirements, or selection process.

Contributions can take multiple forms such as reporting bugs, writing documentation, contributing code (e.g. new model schemas). Any form of contribution is welcome, and it will be recognized.


## Steering CommitteeBeacon Maintainer at least one member from the contributing communities.

The members are typically nominated and elected by the existing committee (Derived from the Service Founding Committee at M1.1) or through a vote by the contributing community members. The selection criteria prioritise diversity in expertise and community representation, with a balance between technical and project perspectives.

The Steering Committee holds regular mandatory meetings, typically on a quarterly basis, to discuss the progress, challenges, and strategic direction of the EBN. Additional meetings can be convened as needed. Agendas for these meetings are set in advance and typically include:

1. Review of Project Goals and Progress: Assessing current milestones and setting future objectives.

2. Technical Developments: Evaluating new technical proposals, updates, and innovations.

3. Governance and Administrative Matters: Addressing any issues related to governance, member roles, and administrative duties.

4. Policy Development and Updates: Discussing and approving new policies or modifications to existing ones.


## Operations Team

Specialists responsible for the technical infrastructure and development of the network. Their primary focus is on developing the network, implementing extensions and ensuring interoperability to enhance its functionality and efficiency.

This committee is composed by contributors of the ELIXIR Beacon Network. It is also encouraged that the members of contributing communities help the development together with the Steering Committee.

Disaster Recovery team


## Training and outreach

Anyone related to the EBN can do training or participate in outreach activities. Before doing so, they must send a mail to <bn-contact@elixir-europe.org> to inform them of the activity, and get any possible help from the community or any other valuable assistance.


## SC Chair

The SC Chair is a single individual, a member of the Steering Committee, and elected for a 2-year non-renewable term by the SC, with the expectation that this role should rotate between its members. The Chair has no additional authority over other members of the Steering Committee: the role is one of coordinator. The Chair is also expected to ensure that all governance processes are adhered to, and has the casting vote when the project fails to reach consensus.

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