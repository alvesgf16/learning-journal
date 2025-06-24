# Cloud Computing

## IaaS

- Virtual machines (e.g., AWS instances, Azure VMs)

## PaaS

- Virtual machines, servers, networks, databases
- Tools to support the application lifecycle (e.g., Heroku)

## SaaS

- Virtual machines, servers, networks, databases
- Tools to support the application lifecycle
- Software (e.g., SharePoint, Slack, Google Docs, Office 365, Trello)

# Azure

## Main advantages

- Supports a wide variety of frameworks and languages, like Java and C#
- Allows working with different databases and operating systems
- Easily scalable according to customer demands

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

