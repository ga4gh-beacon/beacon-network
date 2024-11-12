---
date: 2024-10-22
---


# Add a Beacon in the ELIXIR Beacon Network

In this section you will learn how to add a Beacon in the ELIXIR Beacon Network. There are two sections depending on your role:

- Beacon Owner: You are an owner or mantainer of a Beacon and you want to add it to an ELIXIR Beacon Network.
- ELIXIR Beacon Network (EBN) mantainer: You are an owner or mantainer of an ELIXIR Beacon Network and a Beacon has requested to add their API URL to the network.

## Add a Beacon to a Network (Beacon owner view)

### Add an ID

To being able to classify your beacon in the EBN, you need to create an unique identifier to your Beacon. This ID should be located in the `info` endpoint, inside the `meta` object. Here it is an example:

```
"meta":{
	"apiVersion":"vX.X.X",
	"beaconId":"your.beacon.id",
	"returnedSchemas": {...}
}
```

The `beaconId` must be unique inside the network and it is mandatory to enable individual identification and prevention of duplicates.

### Validate your Beacon

Before asking to add your beacon to the network, you should pass your Beacon to the validator. The Validator can be accessed via Frontend in most of the EBN instances, but it is not mandatory. Here it will be described how to validate your Beacon via command-line:

To validate a Beacon before adding it to the ELIXIR Beacon Network, follow these steps:

1. Ensure you have [Apache Maven](https://maven.apache.org/) installed.

2. Download the validator  repository and navigate to the `tool` folder:

```
git clone https://github.com/elixir-europe/neat-beacon-v2-validator
cd neat-beacon-v2-validator
```

3. Build the code using Maven: 

```
mvn install
```

4. After building, you'll find a `target` directory within the `neat-beacon-v2-validator-tool` folder. This directory contains the validator Java application.

5. Run the validator application with the Beacon's API endpoint to be validated. You can use the following command:

```
java -jar neat-beacon-v2-validator.jar -f https://beacons.bsc.es/beacon/v2.0.0/

java -jar neat-beacon-v2-validator.jar -f https://beacons.bsc.es/beacon/v2.0.0/ -o report.json
```

This command will validate the beacon instance located at the specified API endpoint.
Optionally, you can specify an output file for the validation report using the `-o` or `--output` flag. 

### Send it to the Network

After passing the validator, the Beacon owner might need to send an email to the ELIXIR Beacon Network mantainer asking them to add the Beacon to the network. It is recommended to send the validator output, if any, or specify that the Beacon has passed the validation.

The Beacon owner is responsible for addressing any errors reported by the validator. While the Beacon may still function within the Beacon Network despite reported errors, critical errors may prevent it from returning data.

{: .important }
> ELXIIR Beacon Network maintainers may request the output of the validator before adding the instance to the network.

## Add a Beacon to a Network (ELIXIR Beacon Network mantainer view)

The ELIXIR Beacon Network Mantainer is responsible for requesting the validator output file to confirm that any Beacon meets validation criteria to add it to the network. Subsequently, the Beacon owner should forward the validated Beacon's URL to the EBN Maintainer.

Then, the EBN Maintainer will incorporate the URL of the Beacon into the ELIXIR Beacon v2 Network. This involves adding the Beacon's URL to the `wildfly/BEACON-INF/beacon-network.json` file. 

The structure of this JSON file should be an array containing the URL of the validated Beacon, like this:

```
[
	"new.beacon.url/api"
]
```

After adding the URL to the `beacon-network.json` file, the Beacon Network will automatically fetch the new Beacon, ensuring its integration into the network. This process facilitates the incorporation of Beacons into the ELIXIR Beacon Network.

To remove the Beacon, you just need to remove the URL from the `beacon-network.json` file. 
