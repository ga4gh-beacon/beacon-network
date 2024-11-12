---
date: 2024-10-22
---

# What is a disaster recovery plan?

The purpose of this Disaster Recovery Plan (DRP) for the ELIXIR Beacon Network v2 is to provide a comprehensive, structured approach to prepare for, respond to, and recover from disruptive events that may impact the network's operations. This plan aims to ensure the continuity of critical functions, minimize downtime, and protect data integrity, thereby maintaining the trust and reliability essential to users and maintainers of the ELIXIR Beacon Network v2.

This DRP covers all aspects of disaster recovery for the ELIXIR Beacon Network v2, including hardware, software, data, and communication infrastructures. It applies to all potential disruptions including: cyber attacks, hardware failures, and other emergencies. The plan encompasses:

1. All critical systems and services associated with the ELIXIR Beacon Network v2.

2. Data backup and restoration processes.

3. Communication protocols for internal and external stakeholders during a disaster.

4. Roles and responsibilities of the disaster recovery team.

5. Procedures for testing, maintaining, and updating the DRP.

By achieving these objectives, the ELIXIR Beacon Network v2 will be better prepared to handle unexpected disruptions, ensuring that critical services remain available and secure for its users.


# Risk Assessment

These are the identified risks that can damage the ELIXIR Beacon Network (EBN). In the following list there are the possible risks prioritised based on their impact and likelihood:

1. Cyber attacks: Potential data breaches, loss of sensitive information, and extended downtime.

2. Software failures: May lead to application crashes, data corruption, and service disruptions. It can be caused by bugs when new deployments are in production.

3. Hardware failures: May cause partial or complete loss of services, data loss, and system unavailability.

4. Human errors: Could result in accidental deletion or modification of critical data, system misconfigurations.

5. Power outages: Temporary loss of access to the network.


# Recovery Objectives

The Recovery Objectives are crucial for guiding the disaster recovery efforts for the ELIXIR Beacon Network v2. These objectives define the acceptable downtime and data loss for different components of the network, ensuring that critical services are restored promptly and data integrity is maintained.


## Recovery Time Objectives (RTO)

Recovery Time Objectives (RTO) specify the maximum acceptable duration that a system, application, or function can be offline after a disaster before causing significant harm to the organization.

1. Critical Services: These are the services that must be restored as quickly as possible to maintain the core functionalities of the ELIXIR Beacon Network v2. This includes the main data processing servers and core network infrastructure.

   - RTO: 4 hours.

   - Reasoning: Any extended downtime of these services would severely impact the operations and availability of the network, affecting users' access to critical data.

2. Essential Services: These services support important, but not mission-critical, functions. This includes auxiliary servers and secondary databases (in case of load-balance), and important but non-critical applications such as the different log in applications (if any).

   - RTO: 12 hours.

   - Reasoning: While important, these services can tolerate a slightly longer downtime without significantly disrupting operations.

3. Non-essential Services: These are the services that, while useful, are not critical to the immediate functioning of the network. They include internal services such as the logging system.

   - RTO: 48 hours.

   - Reasoning: These services have the least impact on the immediate operations and can be restored last without causing major disruption.


## Recovery Point Objectives (RPO)

Recovery Point Objectives (RPO) define the maximum acceptable amount of data loss measured in time. It specifies how current the restored data should be after a disaster. As the only data the EBN stores is the one at the logging system and the metadata of each beacon there are no Critical Data losses.

1. Essential Data: It includes periodic logs and user data.

   - RPO: Up to 1 hour of data loss.

   - Reasoning: Logs must be current to prevent data inconsistencies. Also, information about the users making the queries or accessing the EBN.

2. Non-Essential Data: Archived logs and metadata of the beacons in the network.

   - RPO: Up to 24 hours of data loss.

   - Reasoning: Non-essential data that doesn't change much, such as the metadata of the beacons in the network. Daily backups are enough.

By defining clear RTO and RPO for each type of service and data, the ELIXIR Beacon Network v2 ensures a structured and prioritized approach to disaster recovery. This enables efficient resource allocation and focused recovery efforts, minimizing downtime and data loss while ensuring critical functions are restored quickly.


# Recovery Strategies

Recovery strategies outline the approaches and methods that will be employed to restore the ELIXIR Beacon Network v2 to full operational status after a disaster. These strategies are designed to address various types of disruptions and ensure that recovery objectives are met efficiently. The key areas covered include data recovery, system restoration, and infrastructure rebuilding.


## Data Recovery

Data recovery strategies focus on ensuring that data can be restored to meet the Recovery Point Objectives (RPO) defined for different data categories. These strategies involve regular backups, real-time replication, and secure storage solutions.

1. Regular Backups: Backups of all critical, essential and non-essential data, specially the logging system, in the load-balance approach or in the system of the EBN.

   - Frequency: Backup of new data every hour. For non-essential data make daily backups.

   - Storage Location: Multiple locations (in case of Load-Balance approach), on server or in a cloud-based storage. 

2. Cloud Storage Solutions: If you are using cloud storage solutions, they can store backup copies of critical and essential data. Moreover, the cloud storage offers high availability, easy scalability, and additional security features, ensuring data remains accessible and secure.


## System Restoration

System restoration strategies focus on quickly restoring hardware, software, and network infrastructure to operational status. These strategies ensure that critical systems are prioritized and restored to meet the Recovery Time Objectives (RTO).

1. Redundant Systems and Load Balancers: It is recommended to use redundant systems and Load-Balance approaches to distribute the load and provide failover capabilities.

2. Updated System Images: Maintain updated container images of the system for rapid deployment. Regularly update and test with CI/CD the images to ensure they include the latest patches, configuration and pass all the tests.


## Infrastructure Rebuilding

Infrastructure rebuilding strategies focus on restoring the physical and virtual infrastructure needed to support the ELIXIR Beacon Network v2. These strategies ensure that all necessary components are available and can be quickly deployed to restore services.

1. Virtualised Environments: It is recommended the usage of virtualised environments for flexibility and quick recovery. They allow easy replication and migration across different physical hosts.

2. Documentation of hardware: Specify and document the minimum memory and hardware the machines need to run the EBN. 


# Incident Response Plan

The Incident Response Plan outlines the procedures for detecting, responding to, and mitigating incidents that could disrupt the ELIXIR Beacon Network v2. This plan ensures a quick and effective response to minimize impact, protect data, and restore normal operations as quickly as possible.


## Incident Detection

1. Monitoring Tools: Use monitoring tools to detect anomalies in the network and generate alerts. The monitoring can be of network services, intrusion detection and application performance.

2. Incident Response Team: Establish an incident response team available for any issue that can be encountered.

3. Automated Alerts: Set up alerts to notify the incident to the response team of potential issues.


## Incident Response

1. Initial Assessment: Use predefined criteria to categorise the incident (Critical, high, medium or low) based on the impact of the operations. Prioritise the response based on the severity of the incident.

2. Containment: Contain the incident to prevent further damage. It can be done by: Isolating any affected system, blocking malicious IP addresses or disconnecting compromised Beacon from the network.

3. Notification: Notify the disaster recovery team about the incident and the users with any problem that might affect them.


## Incident Mitigation

1. Eradication: Remove the cause of the incident from the affected systems, ensuring the incident will not recur from the same cause.

2. Recovery: Restore affected systems and services to normal operation.

3. Documentation: Document the actions taken during the incident response. It will be used as a lessons learned for future improvements.


## Review

1. Post-Incident Analysis: Review the incident and the response actions taken. Useful to consider what needs to be improved in future versions of the tool.


# Roles and Responsibilities

The effectiveness of the Disaster Recovery Plan (DRP) for the ELIXIR Beacon Network v2 relies on clearly defined roles and responsibilities. This section outlines the specific duties of the disaster recovery team and other key personnel involved in the disaster recovery process. Ensuring that each team member understands their responsibilities is crucial for a coordinated and efficient response to any disruptive event. As this project does not need a large number of people working on it, one person can have more than one role.

The roles and their responsibilities are the following:

- Disaster Recovery Coordinator: Oversees the DRP execution, evaluates the effectiveness of the recovery, and communicates with the Operations Team and the users.

- IT Manager: Manage the technical efforts and infrastructure restoration with the issues of hardware, software and network components. Also, ensure all the systems are functioning correctly and maintain the recovery procedures and updates.

- Back and Recovery Specialist: Ensure data is backed up according to the schedule and verify backup integrity for the restoration process.


## Communication Plan

Effective communication is critical during a disaster recovery process to ensure that all users and beacon maintainers are informed and coordinated.

The objectives are the following:

- Ensure clear, accurate, and timely communication with all people involved in EBN

- Provide regular updates on the status of the disaster recovery efforts to the users.

- Facilitate efficient coordination within the disaster recovery team.


## Internal Communication Channels

- Email: Primary channel for detailed updates and instructions.

- Instant messaging: It is recommended to use Slack (if all the member of the DRP have access to the same channel) or the Gitter channel of the ELIXIR Beacon Network.

- Zoom Meetings: For discussions and direct communication.


## External Communication Channels 

- Email: Use the EBN email list to notify the users and partners about the recovery status and updates.

- Website: A warning box can be posted in the ELIXIR Beacon Network Frontend.


## Communication Protocols

1. Incident Notification: When a incident or disaster is detected it must be informed to the Disaster Recovery team via mail or instant message.

2. Initial Assessment and Response: The completion of the initial assessment with the report of the nature of the incident, with affected systems and immediate response actions, must be made by mail. The mail can be extensive for the members of the DR team, and a summary for the users is enough.

3. Regular Updates: The status of the recovery to the other members of the DR team is must be send via mail or instant message at least every 4 hours. If the situation is critical, an online meeting for further discussion is recommended.

4. Incident Resolution: A mail with the successful recovery and restoration of services must be sent to everyone (User and partners).

5. Post-Incident Review: A meeting is recommended to discuss how to improve the service in future versions.

The Disaster Recovery (DR) coordinator is the person in charge of informing the users. Whereas for the resolution of the incident it is important that the person in charge of sending the email is the IT Manager, as it can give better technical details.


# Backup Restoration Procedures

These procedures ensure that data is quickly restored in the event of a disaster:

- Initiate Restoration: Activation of the disaster recovery plan due to data loss or corruption.

- Assess Damage: IT Manager retrieves the most recent data loss and identifies the most recent backup.

- Select Backup: Backup and Recovery Specialist selects the appropriate backup set based on the data loss assessment and recovery point objectives (RPO).

- Data verification: Verify data integration and functionality.
