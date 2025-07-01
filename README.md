# Kotlin

## What is Kotlin?

- An object-oriented programming language
- Compatible with the Java platform
  - Runs on Java Virtual Machines (JVMs) and other platforms, like Android
  - Similar syntax to Java
  - Many features and programming concepts are similar to those in Java
- A modern language suitable for developing:
  - Android applications
  - Web applications
  - Desktop applications
- Known as a practical programming language
- Designed to be **safe and concise**, allowing developers to write less code for simple tasks
- Offers advanced features such as:
  - Functional programming
  - Function extensions
  - Lambda expressions
- Facilitates writing asynchronous and concurrent code
- Its ease of reading makes it attractive for developers
- Enables faster and more enjoyable code writing

## History

- **2010**: Kotlin is developed by JetBrains, the creators of IntelliJ IDEA, designed as a modern, concise, secure, and Java-interoperable programming language for the JVM (Java Virtual Machine)
- **2011**: Kotlin is first publicly presented at the JVMLS (Java Virtual Machine Language Summit) conference
- **2016**: The official release of Kotlin 1.0 occurs
- **2017**: Google names Kotlin an official development language for Android
- **2019 & 2020**: Ranked as the **fourth most-loved programming language** in Stack Overflow's Developer Surveys
- **2021**: Drops to 14th place in the Developer Survey
- **2022**: Rises to 11th place in the Developer Survey, remaining among the most loved languages

## Why learn it?

- Modern, expressive, secure, and concise language
- Interoperability with Java, beneficial for those familiar with it
  - Leverages the ecosystem of the widely used Java language
- **Multi-platform capabilities: supports multiple programming paradigms**:
  - Object-oriented
  - Functional
  - Imperative
- Ranked among the 15 most widely used languages in 2021 (Stack Overflow survey) with 8.32% preference among developers
- **Adopted by** Trello, Google, Pinterest, Uber, Netflix
- Career Opportunities:
  - **Diverse profiles for specialized roles**, including:
    - Back-end developers
    - Java developers
    - Mobile developers
    - Game developers
    - Software engineers

## What is it for?

- Web
  - Back-end
    - Increasing adoption for **web development** and **server-side systems**
    - Availability of various frameworks and libraries to support developers
- Android
  - Popular due to **concise syntax and interoperability with Java**
  - Offers an easier and more efficient way to develop applications, depending on project needs
- Desktop
- Data Science

- Differences in Contexts
  - In Android development, code executes on an Android virtual machine
  - In back-end systems, code executes on an application server or a Java virtual machine

### Kotlin and Web Development

- Interoperability allows working with existing Java tools, libraries, and frameworks, facilitating commercial adoption
- Major Java frameworks such as ***Spring***, ***Quarkus***, and ***Javalin*** have been implemented
- Leverages its JVM-based architecture to ease the process of migrating from Java
  - Allows for gradual changes in large applications
    - New software features can be written in Kotlin and integrated into existing Java production systems without significant difficulties
    - Legacy Java code can be progressively migrated
- **Seamless migration from Java to Kotlin is possible without major conflicts and inconsistencies**

#### Kotlin for JavaScript

**Kotlin can relate to JavaScript through a process called "transpilation"**
- Unlike Java, where the *Java Virtual Machine (JVM)* is used for bytecode interpretation, utilizes a Kotlin-to-JavaScript compiler
  - This compiler generates JavaScript (.js) and TypeScript (.ts) files from native Kotlin code
- Allows for:
  - Creation of hybrid applications combining Kotlin with other languages
  - Development of front-end applications, such as those using React, and back-end applications with Node.js
  - Multi-platform applications, allowing code reuse in Kotlin/JS and mobile applications
  - Creation of libraries for consumption via JavaScript and TypeScript, facilitating hybrid application development

### Kotlin Native

- Developed as a variation of Kotlin that **compiles directly into the operating system's native binary instead of bytecode** for the JVM
  - Allows better optimization of hardware usage
- **Supports development for embedded systems**:
  - Examples include **cell phones and televisions**, where virtual machines can be costly due to hardware limitations
  - Enables native development for Android, iOS, and desktop operating systems (MacOS, Windows, Linux)
- Supports interoperability with languages such as C and Swift:
  - Allows generation of libraries for other languages from Kotlin code and utilizing libraries written in those languages

### Kotlin for Data Science

- Kotlin as a modern programming language has entered the Data Science domain, offering tools for **creating**:
  - **Pipelines**
  - **Machine learning models**
  - **Artificial intelligence** applications
- Benefits include:
  - Leveraging the features of the JVM
  - Incorporating *Null Safety*
  - Easy to learn
  - Ability to utilize Java libraries focused on data
- Can be used in Notebooks (e.g., Jupyter Notebooks), which are valuable for:
  - Exploratory data analysis
  - Research studies

## Kotlin vs Java: which one to use?

| | Kotlin | Java |
| --- | --- | --- |
| **Popularity** | More modern programming language | One of the most widely used programming languages globally |
| **Usage** | Increasingly adopted in Android and backend projects | Employed in a diverse range of projects |
| **Community Support** | Growing community support | Highly active community |
| **Learning Curve** | Easier to learn and use (than Java) | Steeper learning curve |
| **Learning Resources** | Good documentation and resources available | Numerous resources available, including comprehensive documentation |
| **Syntax** | Precise and concise syntax | More verbose syntax |
| **Null Safety** | ✔️ | ❌ |

- **Choosing a language**
  - Depends on several factors, including:
    - Project needs
    - Development team's preferences
  - Both Java and Kotlin have their own advantages and disadvantages
  - Evaluating each factor carefully is necessary for the best choice

## Flutter vs Kotlin: what is the difference?

| | Kotlin | Flutter |
| --- | --- | --- |
| **What is it?** | Programming language | Framework (Dart) |
| **For what is it best?** | Accessing native resources and platform features | Applications targeting multiple platforms with a single codebase |

### Kotlin Multi-platform (KMM)

  - Addresses multi-platform development
  - Allows sharing a codebase centered on business rules across various platforms
  - Each platform implements the business logic and presents the UI using its preferred frameworks

## Is Kotlin object-oriented or functional?

- Classified as a **multiparadigm language**
- Robustly **supports both object-oriented and functional paradigms**
- Being derived from Java, shares several aspects with it, including being object-oriented
  - Both Kotlin and Java have a **superclass**: 
    - Kotlin uses `Any` as its superclass
    - Java uses `Object` as its superclass
  - Supports **interface inheritance**.
  - Enables the creation of applications using the object-oriented paradigm
- Introduces new or improved features that distinguish it from Java, more focused on functional programming, incorporating:
  - *Callback* functions
  - *Higher-order* functions

## Features

- Is derived from Java and runs in the Java ecosystem
- Code compiles to bytecode, interpreted by the Java Virtual Machine (JVM)
- **Interoperability**: Can utilize Java code within its applications
- Ability to use existing Java libraries without rewriting code
  - Contributes to Kotlin's robustness, similar to that of Java

### Syntax

- **Concise and easy-to-understand**
  - Makes programming more accessible to developers.

```
fun main(){
    println("Hello, world!")
}
```

- Uses **variable inference** as the standard for declaring variables
  - There is no need to explicitly state the type of the variable
  - The compiler determines the type of the variable automatically, based on the assigned value
  - Use the `var` keyword to declare a variable, followed by the variable name and assigned value
    - It is crucial to assign a value when declaring variables to avoid compilation errors

    ```
    var hello = "Hello, world!"
    ```

  - Unlike JavaScript and Python, **does not support dynamic typing**
    - Once a variable is assigned a value, its type cannot be changed.
  - Eliminates the need for a semicolon at the end of each instruction.

#### Basic types

- Primitive types

  | Category | Type |
  | --- | --- |
  | Numeric | Int, Double, Float |
  | Logical |  Boolean |
  | Text | String, Char |

- Complex types
  - Classes
  - Enums
  - Interfaces

#### Functions

- One of the language's greatest strengths is its **functional approach**
  - The functional paradigm emphasizes the importance of functions in development
    - Key concepts include:
      - Function composition
      - Higher-order functions
      - Lambdas
  - This approach changes the way functions are handled in:
    - Development context
    - Language itself
    - Virtual machine
- Functions can be used in a:
  - Object-oriented context
  - Procedural manner
- The syntax is leaner compared to its parent language

  ```
  fun sum(a: Int, b: Int): Int {
      return a + b;
  }
  ```

  - The `fun` keyword indicates a function in Kotlin
  - The function is named `sum` and is followed by parentheses for parameters
    - Parameters must explicitly include the names of scope variables and their types
  - The function returns a value of type `Int`, as it calculates the sum of two integers
    - If a function does not return a value, specifying the return type is unnecessary (unlike Java, where `void` is required for no return)
- **Kotlin's handling of functions differs from Java** and **resembles JavaScript**:
  - Functions can be treated as parameters
  - Functions can be assigned to variables
  - Example: It's possible to rewrite the `sum()` function as previously shown

    ```
    fun main() {
        var sum: ((Int, Int) -> Int) = {a, b -> a + b}
    }
    ```

    - The code may seem confusing at first glance
    - It functions similarly to the previously shown function but is written differently
    - A lambda expression is used: `{a, b -> a + b}`
      - This means: "Given a and b, return a plus b"
    - The lambda function is assigned to the variable `sum`
    - An unusual piece of code illustrates what happens inside the function
      - Key point:
        - The syntax `((Int, Int) -> Int)` indicates:
          - It receives two integers as parameters
          - The final result will be an integer
      - The return type is determined by what follows the expression arrow (->)
- Functions encompass a broad topic with numerous features due to the functional paradigm, including *Named Parameters*, which ensure correct arguments are passed to the functions

### Null Safety

- Mitigates *NullPointerException* (NPE) occurrences
  - When a reference is null and a call is made to it
  - It is a runtime issue, making it hard to predict during development since there's no compile-time assistance

#### Safe Calls Operator

- Prevents implicit NPEs
  - In Kotlin, **an NPE will only occur if explicitly thrown or through interoperability with Java**
- Checks if a property value is non-null
  - If the value is non-null, it returns the property
  - If the value is null, it returns `null`

```
account?.holder?.getName()
```

- The compiler first attempts to access the value of the `account` variable
- If the `account` variable exists, it then tries to access the value of the `holder`
- The `getName()` method is called only if both `account` and `holder` are not null
- If either `account` or `holder` is null, the code returns `null` and avoids calling `getName()`, preventing a null reference exception
- This approach eliminates the need for separate error handling for null values

#### Nullable Receiver

- Used when the goal is to store values in variables
  - When declaring a variable, specify its type followed by the "?" operator

    ```
    val account: Account? = null
    ```

    - The `?` operator indicates that the variable can hold either an Account type object or a null value
  - **Without the "?" operator, objects cannot assume the null value**
- Includes treatments to prevent Null Pointer Exceptions (NPE)
  - One treatment allows calling the `toString()` method on an object:
    - If the object is null, the compiler returns the String `"null"` instead of causing an error
      - This behavior is useful for debugging code

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