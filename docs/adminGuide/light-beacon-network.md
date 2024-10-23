---
title: "Light an ELIXIR Beacon Network"
date: 2024-10-22
layout: default
parent: "Installation"
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


# Light a Beacon v2 Network

When multiple institutions or organizations deploy a Beacon and make it accessible to a network, they form a Beacon Network. This network enables federated querying across multiple beacons without the need of centralized data storage or direct access to the data. Thus, it allows researchers to discover data from multiple beacons in a single query.

If you want to deploy the ELIXIR Beacon v2 Network instance made by the [BSC](https://www.bsc.es/discover-bsc/organisation/scientific-structure/national-institute-bioinformatics-elixir-node-0) (Backend) and [EGA-CRG](https://www.crg.eu/en/programmes-groups/ega-team) (Frontend), follow the next steps.

## Full Docker install (Backend & Frontend)

Download the code from this [repository](https://github.com/elixir-europe/beacon-network-docker.git),

```
git clone https://github.com/elixir-europe/beacon-network-docker.git
cd beacon-network-docker
```

Edit the `config.json` file located in [frontend/](frontend/) to point to the URLs where you will be making the queries. Here's an example of how the `config.json` file should look:

```
{
  "API_URL": "http://localhost:8080/beacon-network/v2.0.0",
  "REDIRECT_URL": "https://yourUIdomain.com",
  "KEYCLOAK_URL": "https://yourKEYCLOAKdomain.com"
}
```
Then, replace [http://localhost:8080/beacon-network/v2.0.0](http://localhost:8080/beacon-network/v2.0.0) and the other URLs with the appropriate URL where your backend is hosted.

Run [docker compose](https://docs.docker.com/compose/) to build and start the containers:

``` 
 docker compose up -d
```
 
Congrats! You have created Beacon Network FrontEnd in [http://localhost:8080/](http://localhost:8080/) and the backend in [http://localhost:8080/beacon-network/v2.0.0/](http://localhost:8080/beacon-network/v2.0.0/). Adjust the URLs based on your setup.


## Backend Installation

Download the code from this [repository](https://github.com/elixir-europe/beacon-network-backend.git), and run [docker compose](https://docs.docker.com/compose/):

```
git clone https://github.com/elixir-europe/beacon-network-backend.git
cd beacon-network-backend/docker
docker compose up -d
```

Congrats! You have created Beacon Network in [http://localhost:8080/beacon-network/v2.0.0/](http://localhost:8080/beacon-network/v2.0.0/). You can now view and query the backend as needed. Adjust the URLs as necessary based on your setup.

## FrontEnd Installation

Download the code from this [repository](https://github.com/elixir-europe/beacon-network-ui.git):

```
git clone https://github.com/elixir-europe/beacon-network-ui.git
cd beacon-network-ui
```

Create a `.env` file inside the folder and modify the following variables:

```
REACT_APP_CLIENT_ID="ID of your LS Login"
REACT_APP_CLIENT_SECRET="password of your LS Login"
```

Run [docker compose](https://docs.docker.com/compose/):

```
docker-compose up -d –build
```

Edit `config.json` from [frontend/src](frontend/src) to point the URLa where you are making the queries. Example:

```
{
  "API_URL": "https://yourAPIdomain.com/beacon-network/v2.0.0",
  "REDIRECT_URL": "https://yourUIdomain.com",
  "KEYCLOAK_URL": "https://yourKEYCLOAKdomain.com"
}

```

You have deployed the Beacon Network Frontend in [http://localhost:3000](http://localhost:3000). Adjust the URLs as needed based on your setup.

# Update the EBN

To update the ELIXIR Beacon Network (EBN) with a new image, follow these steps:
Pull the latest image:
```
docker-compose pull
```
Recreate and rebuild the containers with the new image:
```
docker-compose up --force-recreate --build -d
```
These commands will download the latest image for the EBN and recreate the containers using the new image. The `--force-recreate` flag ensures that the containers are recreated even if they are already running, and the `--build` flag rebuilds the containers if necessary. The `-d flag runs the containers in detached mode.
