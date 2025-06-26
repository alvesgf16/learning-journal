# Cloud Computing

- Delivery of Information Technology (IT) resources on demand via the Internet, with pay-as-you-go pricing
- Instead of buying, owning and maintaining physical data centers and servers, you can access technology services

## History

- 2000s: Cloud computing technology gains momentum as it is offered commercially
  - 2006: The emergence of Amazon Web Services (AWS), which allowed businesses and individuals to rent virtual computers
    - This suite of services included storage, computing, and networking, all based on the cloud
  - 2007: Netflix launches its video streaming service, using the cloud to stream movies and other content
  - 2008: launch of Google Cloud Platform (GCP)
  - 2010: launch of Microsoft Azure

## Characteristics

- Ease of creating resources
- Ease of scalability and maintenance of computing resources
- Possibility of using Infra as Code (IaC)
- Ease of thinking about Disaster Recovery
- Cost control

## Service models

### Infrastructure as a Service (IaaS)

- Virtual machines (e.g., AWS instances, Azure VMs)

### Platform as a Service (PaaS)

- Virtual machines, servers, networks, databases
- Tools to support the application lifecycle (e.g., Heroku)

### Software as a Service (SaaS)

- Virtual machines, servers, networks, databases
- Tools to support the application lifecycle
- Software (e.g., SharePoint, Slack, Google Docs, Office 365, Trello)

# Azure

## Main advantages

- Second largest cloud computing service provider used in the world
- Easily scalable according to customer demands
- Maximum capacity of a VM is 128vCPU and 3.5 TB memory
- Supports a wide variety of frameworks and languages, like Java and C#
- Allows working with different databases and operating systems
- Offers many services without necessarily being Microsoft
- Offers very simple and direct integration with Microsoft tools
- Ease of migrating on-premises Microsoft tools to the cloud

## Resource groups

- Group items for a specific project to facilitate navigation
  - All used resources are displayed when clicking on the group
- Use grouping for cost estimation of a project
  - Access the console to search the group for the estimated project value
- To remove all resources after finishing a project, select the resource group and delete it
  - No need to remove resources one by one

### Creating a resource group

- Subscription
- Resource group name
- Region
- Tags

## Azure CLI

### Initial steps

#### Check version

```az version```

#### Login

```az login```

#### Find commands

```az find```

#### Interactive mode

```az interactive```

#### Resource group

```az group create –location x –name y```
```az group list```
```az group delete –name y```

#### Service plan

```az appservice plan create –name z –resource-group y –sku a [--is-linux|?]```

#### Runtimes

```az webapp list-runtimes```

#### Web app

```az webapp create –name b –plan z –resource-group y –runtime c```
```az webapp browse -n b –resource-group y```

## Azure Virtual Machines

Software computers (which can have different operating systems) that perform the same function as physical computers.

Avoid the cost of maintaining a physical environment of equipment in operation. For large applications, this can make a huge difference.

## Azure Container Instances

A solution for any scenario that can operate in isolated containers, without orchestration.

## SQL Database

