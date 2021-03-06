# Welcome to the Gluu Server Docker Edition (DE) Documentation

The Gluu Server is an Identity and Access Management (IAM) suite. It consists
of several fee open source components integrated together. [Community Edition 
(CE)](http://gluu.org/docs), uses a `chroot` file system container. Docker containers
offer process and network isolation. Docker is the future! This distribution
is a starting point--it's experimental. We don't recommend using it in production.

There are several goals for the [DE][de] distribution:
 1. Elasticity: rapidly scale up and down compute resources based on demand.
 2. Mutli-cloud: support deployment on hybrid cloud or heterogenous cloud providers
 3. Self-healing: system smart enough to adjust capacity based on demand

In addition to the components found in CE, [DE][de] includes several
other standard components. Gluu Engine provides API's to automate devops--
deployment of VM's, network, containers, software and data. These API's also have 
an optional Web interface to facilitate administration by people.

While one instance of CE is deployed on a single VM, [DE][de] components are 
distributed. The diagram below provides an overview of where these components reside.

![Gluu Server DE components]
(https://raw.githubusercontent.com/GluuFederation/docs-cluster/master/sources/img/de-components.png
"Gluu Server Topology Overview")

The control node can run anywhere on the network, even on your laptop. The discovery
node is a single instance. One Master node is required for each DE deployment. It includes
the Swarm master server, and it is the only node on which you can deploy oxTrust (which is
not a stateless application). The worker nodes is where you would scale--you can deploy
any number of worker nodes.


# Admin Guide
- [Overview](./admin-guide/overview/index.md)
- [Installation](./admin-guide/installation/index.md)
- [Getting Started](./admin-guide/getting-started/index.md)
- [Cluster Management](./admin-guide/cluster-management/index.md)
- [Components](./admin-guide/components/index.md)
- [Web Interface](./admin-guide/webui/index.md)
- [Troubleshooting](./admin-guide/troubleshooting/index.md)
- [Recovery](./admin-guide/recovery/index.md)
- [Migration](./admin-guide/migration/index.md)
- [Known Issues](./admin-guide/known-issues/index.md)

# Reference
- [API](./reference/api/index.md)
  - [Cluster](./reference/api/cluster.md)
  - [Provider](./reference/api/provider.md)
  - [Node](./reference/api/node.md)
  - [Container](./reference/api/container.md)
  - [Container Log](./reference/api/container_log.md)
  - [License Key](./reference/api/license_key.md)

[de]: "Docker Edition"
