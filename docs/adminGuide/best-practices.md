---
date: 2024-10-22
---

# Best Practices

## Adding your own filters

As an ELIXIR Beacon Network (EBN) maintainer, along its steering commitee, you decide which filtering terms a Beacon Network (BN) can query. You can avoid all the filtering terms of the beacons in the network, and only use the ones from the static ontologies of the Aggregator.

## User certificates

To ensure the privacy and anonymity of the data, a BN should keep track of the metadata of the queries done by the users. As an example, a user can make multiple queries to retrieve all the genomic data of a patient. This can potentially compromise the privacy of the patient and confidentiality of the data.

To address the issue, Beacon Networks can use User Certificates to know who makes queries to the Beacons. By monitoring their activity we can prevent users from accessing too much data at once and identify suspicious activities. A possible solution is to limit the number of queries per user in a day or to stop giving access to a user when the queries are mistrustful.

This mechanism will build trust and confidence among users and data owners.

## Known issues

Here there are issues that we have found in different Beacons when importing them to the network. In order to solve them, the propietary of such beacon need to be contacted and fix the issue.

### Query per second

When the EBN fetches the Beacons, first it needs to query the metadata in order to parse and put it in the cache. These queries are done in consequential order. If one of your Beacons API has limited the queries per second, this would cause trouble to the Network as it won’t let it search for all the needed metadata.

### Correct paths

The most common mistake when inserting a beacon to the network is having wrong URL paths in the `/map` endpoint. If you are a Beacon maintainer, you must check that all the URLs work properly.

The ELIXIR Beacon Network need to check all the paths in order to query them or retrieve the correct specification. If the path returns any value, the beacon will not be queried.

### Beacon ID and general information

The Beacon ID of the beacon must be unique. If not, the Beacon Network won't be able to process the responses.

If you deploy your beacon based on another instance or [Reference Implementation](https://github.com/EGA-archive/beacon2-ri-api), you should change the general information of the given beacon with the name of your organisation, project, and other info.

### Filtering terms

The scope of the filtering terms endpoint must be per schema.

## Types of Beacon Network

### BN Opaque

This type of Beacon Network allows the user to query the data without knowing its origin. The user knows the data is present in the network but is unaware of which specific Beacon it comes from. This type is particularly useful for rare diseases or situations where identifying the data source is not necessary.

### BN Transparent

Type of Beacon Network where the source is known. When querying data, the BN will provide information about the Beacon holding that information. It will allow users to track the source of data and be able to ask for access to the full dataset, thus allowing data sharing.