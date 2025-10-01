# Cloud Computing

- Delivery of Information Technology (IT) resources on demand via the internet, with pay-as-you-go pricing
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
- Offers straightforward integration with Microsoft tools
- Ease of migrating on-premises Microsoft tools to the cloud

## Resource groups

- Group items for a specific project to facilitate navigation
  - All used resources are displayed when clicking on the group
- Use grouping for cost estimation of a project
  - Access the console to search the group for the estimated project value
- To remove all resources after finishing a project, select the resource group and delete it
  - No need to remove resources one by one

### Creating a resource group

- Basics
  - Subscription
  - Resource group name
  - Region
- Tags

## Virtual machines

Computing resources offered by the clouds, in which we can select disk capacities, memory, and processing power, among other resources

### Creating a virtual machine

#### Basics

- Project details
  - Subscription
    - Resource group
- Instance details
  - Virtual machine name
  - Region (normally the same as the resource group)
  - Availability options:
    - **No infrastructure redundancy required**
    - Availability zone: separate resources within a region
    - Availability set: distribute resources across multiple fault domains (distribute VMs across multiple physical hosts)
    - Virtual machine scale set: distribute VMs across zones and fault domains at scale
  - Security type: **Standard**, or Trusted launch virtual machines
  - Image (OS)
  - VM Architecture: Arm64 or **x64**
  - Run with Azure Spot discount: idle Microsoft Azure resources they leave available
  - Size
  - Enable Hibernation
- Administrator account
  - Authentication type: **SSH public key** or Password
  - Username
  - SSH public key source
  - SSH Key Type
      - RSA: suitable for older systems or when compatibility is a primary concern
      - Ed25519: recommended for new systems and applications where security and performance are critical
  - Key pair name
- Inbound port rules
  - None: the machine will be completely inaccessible via the internet
  - **Allow selected ports**
    - Select inbound ports: HTTP (80), HTTPS (443), **SSH (22)**

#### Disks

- VM disk encryption
  - Encryption at host
- OS disk
  - OS disk size
  - OS disk type: Premium SSD, Standard SSD, or **Standard HDD** in a **locally-** or zone-redundant storage
  - **Delete with VM**: When we remove the VM, the disk will be deleted along with it
  - Key management: **platform-**, customer-, or platform- and customer-managed keys
  - Enable Ultra Disk compatibility

#### Networking

- Network interface (automatically created when creating a virtual machine)
  - Virtual network
  - Subnet
  - Public IP
  - NIC network security group: None, **Basic**, or Advanced
  - Public inbound ports
    - None: the machine will be completely inaccessible via the internet
    - **Allow selected ports**
      - Select inbound ports: HTTP (80), HTTPS (443), **SSH (22)**, RDP (3389)
  - **Delete public IP and NIC when VM is deleted**
  - Enable accelerated networking
- Load balancing
  - Load balancing options: **None**, Azure load balancer, or Application gateway

#### Management

- Microsoft Defender for Cloud
- Identity
  - Enable system-assigned managed identity
- Microsoft Entra ID
  - Login with Microsoft Entra ID
- Auto-shutdown
  - Enable auto-shutdown
- Backup
  - Enable backup
- Guest OS updates
  - Enable periodic assessment
  - Patch orchestration options: Image default

#### Monitoring

- Alerts
  - Enable recommended alert rules: warn when the CPU percentage is 80%, when the available memory bytes are less than a certain number, and so on
- Diagnostics
  - Boot diagnostics
    - **Enable with managed storage account**
    - Enable with custom storage account
    - Disable
 Enable OS guest diagnostics
- Health
  - Enable application health monitoring

#### Advanced

- Extensions
- VM applications
- Custom data and cloud init: we can include some script in the "custom data" box that will run when starting the VM
- User data
  - Enable user data
- Performance (NVMe)
  - Higher remote disk storage performance with NVMe
- Host
  - Host group
- Capacity reservations
  - Capacity reservation group
- Proximity placement group
  - Proximity placement group

#### Tags

### Connecting to a virtual machine

#### Using SSH

- Store the key we received on the machine and chmod it to 400 if it is Linux
  - If it is Windows, use WSL to edit or create (using sudo) /etc/wsl.conf and add the following:
    ```
    [automount]
    options = "metadata"
    ```
  - Shut down all WSL instances and restart an instance, and any chmod changes are now retained
- Provide a path to the key:
  ```
  ssh -i <SSL key file> <Administrator account username>@<VM public IP address>
  ```

### Configuring the virtual machine as a web server (Node.js)

#### Installing Node.js

- Inside the Azure VM, run the commands below to prepare it as a web server
  ```
  sudo apt-get update
  sudo apt-get install nodejs
  sudo apt-get install npm
  ```
- Next, confirm the installation and version with the command:
  ```
  node --version`
  ```

#### Deploying a web application

- First, clone the application repository and enter it:
  ```
  git clone <repository URL>
  ```
  - Enter the repository folder you just cloned
    ```
    cd <application directory>
    ```
- Update any configuration files to use information from Azure resources
- Install the dependencies
  ```
  npm install
  ```
- Prepare the server to be a *webserver*
  ```
  npm install express --save
  ```
- Start the application
  ```
  DEBUG=<application directory>:* npm start
  ```


## Databases

### Creating an Azure Database for MySQL

#### Basics

- Project details
  - Subscription
    - Resource group
- Server details
  - Server name
  - Region (normally the same as the resource group)
  - MySQL version
  - Workload type:
    - For small or medium size databases
    - Tier 1 Business Critical Workloads
    - **For development or hobby projects**
  - Compute + storage
  - Availability zone
- High availability
  - Enable high availability
- Authentication
  - Authentication method:
    - **MySQL authentication only**
    - Microsoft Entra authentication only
    - MySQL and Microsoft Entra authentication
  - Administrator login
  - Password
  - Confirm password

#### Networking

- Network connectivity
  - Connectivity method:
    - **Public access (allowed IP addresses) and Private endpoint**
    - Private access (VNet integration)
- Public access
  - **Allow public access to this resource through the internet using a public IP address**
  + **Add current client IP address**
  + **Add 0.0.0.0 - 255.255.255.255**
- Firewall rules
  - Allow public access from any Azure service within Azure to this server
- Private endpoints
- Encrypted connections

#### Security

- User assigned managed identity
- Key selection method:
  - Enter a key identifier
  - Select a key
- Key

#### Tags

### Overview

- Essentials
  - Status
  - Location
  - Server name: the URL we will use to make the connections
  - Administrator login
  - Configuration
  - MySQL version
  - Availability zone
  - Created on
- Getting started
- Properties: more detailed information, such as machines, high availability, and backup, among other data
- Recommendations: if we were not following good practices, it would be informed here
- Monitoring: graphs showing database usage information (CPU and memory usage, I/O percentage, DB connections and queries)

### Connecting to a database

#### Remove SSL

- In the search field at the top of the "Settings > Server parameters" page, search for "ssl"
  - A parameter called "require_secure_transport" will be displayed
- In the "value" column, change from "ON" to "OFF"
- Click "Save" in the upper left corner

#### Add a database

- Click on the "Add" button in the "Settings > Databases" page
  - A pop-up will appear on the right side, titled "Create Database," below which are two buttons: "Save" and "Cancel"
  - Right after that, we have three fields: "Name," "Character set," and "Collation"
- Then we click on the "Save" button
  - After clicking, a pop-up will appear in the upper right corner with the message "Creating MySQL database"
  - After waiting a few minutes, the previous message will change to "Successfully created MySQL database"

#### Log into the database

- In "Connection details" on the "Connect" page, it tells us the hostname, username and password, which we entered at the time of configuration
- Below, we have the option to connect via browser or locally
  - Clicking on it, when expanded, displays the URL that we will use to connect in a command:
    ```
 mysql -h <server name> -P 3306 -u <username> -p
    ```
      - In the option below to "Import and export data," it is in case we already have data to insert into the database
  - However, before we use this instruction, we need to log into the virtual machine
    - In the terminal, we will run the ssh command to log in, passing the key, the user, and the IP of the virtual machine
      ```
 ssh -i <SSL key file> <Administrator account username>@<VM public IP address>
      ```
  - Once logged into the virtual machine, we can access the database
  - Therefore, we will copy the mysql command and paste it into the terminal to run it
    - In return, it will ask for a password
  - We will type the password that we chose during configuration and select "Enter"
    - In return, a welcome message will be displayed with some information 

## Azure CLI

### Initial steps

#### Check version

"`az version` "

#### Login

"`az login` "

#### Find commands

"`az find` "

#### Interactive mode

"`az interactive` "

#### Resource group

```az group create –location x –name y```
"`az group list` "
"`az group delete –name y'  "

#### Service plan

"`az appservice plan create –name z –resource-group y –sku a [--is-linux|?]` "

#### Runtimes

```az webapp list-runtimes```

#### Web app

"`az webapp create –name b –plan z –resource-group y –runtime c` "
```az webapp browse -n b –resource-group y```

## Azure Virtual Machines

Software computers (which can have different operating systems) that perform the same function as physical computers.

Avoid the cost of maintaining a physical environment of equipment in operation. For large applications, this can make a huge difference.

## Azure Container Instances

A solution for any scenario that can operate in isolated containers without orchestration.

## SQL Database