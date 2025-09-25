# Software Architecture

## What is software architecture

When an application is small, it’s easy to navigate, understand where each piece of logic is and identify what needs to be read or changed to add functionality. As the application grows, the lines of code increase into the thousands, and its complexity rises; adding or maintaining features can become difficult.

Therefore, it’s crucial to **plan how the application will be organized** to facilitate modifications or the addition of new code, as well as to make each section’s **responsibilities** – **its role within the system** – clear, especially for newcomers to the development team. That is: how will we manage our logic? What files will we have? In which directories? What combinations will we implement so that one or multiple teams can handle the same application without confusion?

In short, we need to establish a set of organizational patterns, standards, principles, and techniques for building our application. In Computer Science, this is known as **Software Architecture**: the fundamental structure or skeleton of a software system that defines its components, their relationships, and the principles that guide its design, realization, evolution and life-cycle. It captures the key concepts and properties of the system in its surrounding environment and the governing rules that determine how the system is organized, built, and maintained.

It’s a field rich in analysis and experimentation with different application structures and it's a **crucial** decision in system development, as it defines the software’s basic structure and how its components interact. It ensures the system is **scalable**, **secure**, **robust**, and **performant**, while also allowing the software to be easily modified or updated in the future. In other words, a good software architecture facilitates maintenance and reduces the costs of fixing bugs or adding new features.

There are many approaches to designing software: Layered Architecture, Hexagonal Architecture, among others. In other words, various architectures can be employed in the software development process. Each architectural model has its own characteristics and is suitable for different types of systems, scenarios, and business models. They offer advantages and disadvantages that should be weighed when choosing.

### What is NOT software architecture

**Software design** and **code-writing** principles, such as SOLID, don’t provide a project architecture. This doesn’t mean you should exclude them from software architecture, as you can and should apply design principles to the architecture chosen for your project. For example, you can apply SOLID, KISS, DRY, etc., to the service-oriented architecture (SOA) pattern.

Beyond principles, the concepts of **software design approaches** can also be confused with software architecture. For instance, **DDD** (Domain-Driven Design) is not considered a software architecture in isolation, as it does not encompass the creation of a structure for organizing components, namespaces, or methods for dividing classes and interfaces. However, it is possible to apply DDD to understand the domains of the business model and, from there, choose the architecture that best fits the project, such as **hexagonal architecture**, for software development.

By understanding the distinction between design principles, such as SOLID, approaches, such as DDD, and software architecture, we highlight the importance of integrating these principles and approaches within the context of an architectural pattern. After all, it’s not just about writing efficient code, but about building a robust structure that meets the specific demands of each business model.

## Software architecture patterns

Software architecture patterns are fundamental to achieving the entire abstraction process, and choosing the right one for your business model is essential, as it avoids rework and high costs for the client and the team.

Furthermore, we can work with different architectural patterns in the same software, whether to meet specific business requirements, facilitate maintenance, or leverage various technologies.

An architectural pattern is an already established solution for software development, a reusable model for known problems. These patterns have already been studied, tested in real-world projects, and undergone improvements, making them widespread and accepted solutions in the market. Check out some advantages of using architectural patterns:

- Greater software flexibility and scalability
- Ease of maintenance and evolution
- Security
- Better application performance
- Reduced costs and risks

In addition to these benefits, using architectural patterns facilitates dialogue between teams and individuals, as they are market-leading solutions.

The architectural patterns presented offer distinct solutions to different challenges. The choice between them must be carefully considered, taking into account not only the current trend but also the project requirements, desired scalability, future maintainability, and the nature of the domain.

As stated by Robert C. Martin, **the goal of software architecture is to minimize the required human resources, reflecting the continuous pursuit of efficiency and quality**.

### Client-server architecture

The idea of ​​thinking about software in layers is not new, and this perspective gained greater visibility in the 1990s with the arrival of **client-server systems**.

According to Martin Fowler, in his book *Patterns of Enterprise Application Architecture*, systems were separated into two layers:

1. **Client:** Responsible for maintaining the user interface and some application code. For example, Delphi and VB provided visual components for working with databases.
2. **Server:** Typically a relational database, such as SQL.

This model worked well for performing simpler data updates and only required displaying the information. However, if there was a need to implement more complex **domain logic**, including validations, business rules, checks, and calculations, code manipulation became more challenging. This problem often occurred because developers wrote the logic on the client, leading to code duplication and other issues, such as creating multiple screens for simple changes in search processes.

Another, though less common, possibility was to keep the domain logic embedded in the database, in the form of stored procedures. However, the code remained limited and rigid.

Simultaneously with the rise of client-server architecture, the object-oriented paradigm was also growing, and the community itself was providing answers to domain logic issues. Among them, one solution was to abstract the complexity of domain logic into a structured layer.

While the three-layer separation seemingly solved the problems of maintaining business rules, many systems were simple, and the tools used to build client-server systems don’t work well with the three-tier model. We should also remember that simple problems were well solved with the client-server architecture.

The scenario changed with the advent of the web, as people began to use browsers to install client-server applications. Today, we recognize that this is not an adequate solution, as it would require difficult maintenance and necessitate refactoring the web interface for any change in business logic. This practice will, at the very least, increase software development costs, as it requires more people and time to implement new features. However, this doesn’t mean that client-server architecture is bad or shouldn’t be used; it’s essential to understand the business logic and evaluate the application of the architecture. This is especially true when considering *two-tier* and *layered* systems, as they are closely related concepts.

Fowler describes client-server systems as two-tier systems because there is a physical separation: the client is a *desktop* or workstation, and the server is the dedicated computer system.

On the other hand, the author describes the idea of ​​a *layer* as a **functional separation** and emphasizes that a domain logic layer, for example, can run on both a desktop computer and the database server. This means you can have two devices (nodes), but there are still three distinct layers. Even when using a local database, all three layers can run on a single laptop, maintaining the functional separation between them.

This perspective aligns with what Sommerville, in the book *Software Engineering*, describes as the client-server pattern for distributed systems:

> In a client-server architecture, the system’s functionality is organized into services, each of which is provided by a server. Clients are the users of these services and access the servers to use them.

Sommerville continues by stating that this pattern is used when there is a need to share data in a database from different locations. Again, it’s the idea of separating servers for each service and domain logic.

### Layered architecture

In the **layer-based architectural model**, also known as **Layered Architecture**, each **layer** contains a set of files with a specific, well-defined and documented responsibility and functionality within the program. A layer's functionality depends on the resources and services provided by the layer below it. These are the layers that provide services. Thus, we have a representation that progresses from the highest level to the lowest, not in terms of importance, but in relation to the system’s architecture.

Sommerville, in his book *Software Engineering*, points out that this model is typically used in different situations:

- When we want to build a new feature from an existing system.
- When development is done by different teams, each of which is responsible for a layer of functionality.
- When the software has multi-layered protection requirements.

The number of layers is not fixed or predetermined, as they can be divided into more layers if needed. Here, we will work with three: **Model**, **Service**, and **Controller**. 

#### Model

Responsible for retrieving data from data storage tools, which can range from a DBMS (such as MySQL or Postgres) to a file system (including .csv and .json files), or even other RESTful APIs. Its role is to retrieve this data and provide an easy way for the rest of the application to access it, without anyone else needing to know how the data is obtained.

The layer itself will be a directory within the application’s `src/` folder, `src/models/`. Within this directory, there are several ways to organize data in the literature on the topic. When the application serves a front-end, some advocates suggest having a file in the Model for each screen. Very commonly, there’s a file for each table in the database—so each file is responsible for returning data from a specific table.

Each file in the layer will be a different Model. Think of it this way: the Model layer receives data from the database, separates it neatly, boxes it, and sends it to the rest of the application. Each Model is a “boxer” for a portion of the data.

#### Service

Located at the center of the flow, it “talks” to all other layers.

This layer is limited to the **business rules** of an application. This term is often used in the backend. It can be defined as the validations and process definitions that an application must follow to perform its designated tasks, or procedures and regulations that generate value for a business, organization, or individual. In other words, **the business rule pertains to how the program should perform its core function.** For example, when a bank grants a loan, it calculates the interest rate based on a specific business rule.

These checks should be, or are, decoupled from data access or request processing, and can be divided into two types:

- **Input validations:** These are rules such as "it is not possible to register a product whose name has fewer than five letters" or "it is not possible to edit a non-existent field." This type of rule can be validated in the **Service** layer or in a **Middleware** layer.
- **Complex business rules:** These are rules such as "it is only possible to sell products that are in stock" or "it is not allowed to pay in more than 5 installments for purchases under R$100.00."

Separating these responsibilities in an architecture provides many benefits for developers and applications. To better understand these benefits, imagine that an application has been developed for years, and the technology initially used has become obsolete, or a more advanced technology has emerged. If business rules are too tightly coupled to these technologies (such as databases or web frameworks), migrating to the new technology can be very costly and error-prone.

Furthermore, as projects grow, applications become increasingly larger and more complex, accumulating more business rules. These business rules are sometimes revisited to add, remove, or update requirements. Furthermore, it's very common for these maintenance tasks to be performed by multiple people throughout an application's lifecycle.

Software requirements can be conflicting, as people within an organization where the software is being developed or maintained may have different views on what a given business rule should or shouldn’t do. Furthermore, developers use technologies according to their level of expertise, preferences, or project needs.

When we isolate our business rules in the **Service** layer, we allow for easier visibility of potential conflicts in our code. Furthermore, we don’t limit our business rules to only doing what technology X or Y allows. **It’s the business rule that defines the technology to be used, not the other way around.**

A good **Service** layer needs to:

- Abstract complex business rules from your model;
  - *Example:* Define movie recommendations based on the user’s profile.
- Centralize business rule validations:
  - *Example:* A person who hasn’t yet paid their monthly bill shouldn’t have access to the movie platform.

A good Service should**n’t**:

- Have any information about access to the data layer (**Model**);
  - *Example:* No SQL queries.
- Receive anything related to HTTP, either the `request` or the `response`.
  - The **Controller** layer should only send what’s necessary to the **Service** layer.

#### Controller

Any REST API, regardless of the programming language or framework chosen, will always receive requests from various devices. It’s the API’s responsibility to receive and respond to these requests appropriately. This data can be obtained via body, query, or params, and the response can also have different types. The most common in the market today is JSON.

In principle, data is sent from an application, be it a React, Android, iOS, Desktop, or other application. This data should be sent already processed and validated. However, the person (or team of people) developing a back-end application would be naive to believe that every request always arrives with reliable data.

Malicious individuals can make requests to APIs with the intention of discovering exploitable flaws and gaining an advantage. Remember that there are software programs available to create requests for REST APIs. Anyone can use them to send requests to REST APIs with incorrect, forged, missing data, or any other possible combination.

Knowing this, one of the basic tasks when building any REST API is to validate the data received from a request to ensure the application’s correct functioning. In other words, all the data necessary for the request to be fulfilled must be available in the request itself.

Validations performed in the service layer focus on **business rules** (which we can also refer to as qualitative validations). In contrast, controller validations ensure that all data passed in the request exists and that the service layer can perform its task.

As an example, consider the following situation: imagine we have a person registration endpoint and a rule stating that two people cannot have the same email address. This is an example of a business rule that requires the service layer to validate before inserting a new person into the database.

On the other hand, the controller layer must ensure that the fields exist in the request body. Then, it calls the service layer component! If the email address is not provided during the request, the registration process will not be possible, and the response should return a `status 400`.

Some people may argue that all data validation should be performed in the controller layer! While others say that specific validations (such as minimum password length or verifying a string as a valid email address) should be performed in the service layer. Keep in mind that building an application based on an architectural model means making a set of choices that make sense within the context of the people involved in developing the application. Therefore, nothing is set in stone, and variations on these rules are common.

In addition to validations, the **controller** layer is also responsible for directing data received from the request to the relevant components in the **service** layer; that is, a component in the controller receives the request and makes a function call to an element in the service. This function call performs all necessary processing, including accessing the **model** if required. Finally, the process returns between the layers until it returns to the controller.

It’s worth noting that the request doesn’t enter the service and model layers. The controller calls a function within the service, passing the necessary data for its execution, and then awaits its return before responding to the request, whether with responses indicating the success of the request or with responses indicating the occurrence of an error and the reason. Here, we can classify errors into two categories:

- **Client-Initiated Errors:** Errors in this category occur when the client sends a request with incomplete, missing, or invalid data. Therefore, the request cannot be processed, and the error and its reason are returned to the client.
- **REST API-Initiated Errors:** Errors in this category occur when: the database is unavailable, the API is down, among others. These errors are usually responded to with a `status 500` and a generic error message.

Responses to API-Initiated Errors are generic, intended to prevent the sharing of information about how the application works. Depending on the error information shared, it can be used against the API itself through a malicious attack. For example, suppose the attacker is informed that the database is MySQL. In that case, they only need to focus their efforts on attempting to compromise MySQL, thereby eliminating the need to spend time and effort figuring out which database is being used.

Here are two points to highlight:

- The control layer doesn’t necessarily manage routes. This can be done in a dedicated file.
- To validate the existence of fields in the request body, we can use middleware.

### Model-View-Controller (MVC) architecture

Perhaps one of the oldest and most widely used software architecture patterns in web development learning, the MVC pattern is quite flexible and has high scalability and reusability.

The pattern was developed in the 1980s at Xerox for creating graphical interfaces, but its adoption in web applications made it more widely known.

Like any architectural pattern, MVC organizes and divides an application’s code into layers, each with its own responsibilities. It consists of three layers: the **Model** layer, the presentation/**View** layer, and the **Controller** layer.

This division enables business rules to be separated from the presentation layer, allowing for greater code reuse.

What MVC provides is a general framework for organizing an application that supports user interaction.

#### MVC vs Layered (MSC) architecture

In the **MVC** context, the **model** still handles data manipulation and structure definition, and all data access must go through this layer. However, without a **service** layer, it also manages the application’s business rules, including validations and data processing. Additionally, just like in **MSC**, it should remain decoupled from the other layers—**views and controllers**—and should not be aware of them.

The **controller** still handles receiving requests and sending responses. However, it now acts as a bridge between the **view** and the **model**, receiving actions from the view and determining what should be displayed, consulting the model if necessary.

In **MVC**, unlike **MSC**, each layer can be modified independently; for example, we can add or change an existing **view** without altering the data within the **model**.

#### View

The **view** is the presentation layer, that is, the part that interacts with the person using the system. It basically serves as data input and output. It is responsible for two key functions: creating a visualization of the data generated by the **model** and providing a means for the user to interact with the system.

The **view** communicates with the **controller** (receiving instructions on what to display and communicating events that occur as the person interacts with the system) and with the **model**, receiving the data it should present.

Here, once again, we see the benefits of separating responsibilities. Since the **view** is only responsible for displaying a representation of the data, it doesn’t need to know how it is stored.

Imagine if, every time we needed to change the view (such as changing the layout of an HTML page), we also had to change our models or, worse still, our database schema. Since the **model** abstracts all these details behind an API, we don’t have to worry about them.

This separation even allows for more than one presentation of the same data to be created for different contexts.

In web applications, the view is typically an **HTML** page, but it can also be in other formats, such as **JSON** and **XML**.

### Service-oriented architecture (SOA)

In this pattern, the system is divided into independent services, with each service responsible for a specific functionality. Then, well-defined interfaces are developed so that communication between services occurs without relying on a particular language or platform.

The idea is for a piece of software to provide a service to another service.

**A service is an independent, well-defined function that represents a unit of business functionality.** Among the characteristics of service-oriented architecture, each service can exchange information with another service. A service is also *stateless*, meaning it does not depend on the state of another service.

Instead of separating the system into distinct applications, each with its own business logic, we can create a service layer for each functionality and work on different interfaces that consume these services. This approach enables the centralization of services and business rules, saving time, reducing infrastructure costs, and eliminating code redundancy.

With SOA architecture, a system composed of services that other applications can utilize can be developed. Between the services and the interface is an intermediate layer called the Enterprise Service Bus (ESB).

According to AWS, the bus works like this:

1. The bus receives incoming or outgoing messages from an endpoint.
2. It determines the address of the destination endpoints by checking the business policy rules.
3. It processes the message and sends it to the destination endpoint.

The enterprise service bus is a fundamental part of the integration between the software components that represent the system’s functionalities.

Although SOA architecture is interesting in several cases, its application and use of ESB become limited in situations involving the complex integration of legacy systems. Therefore, it is necessary to study new solutions, such as Microservices architecture, and analyze the application needs.

### Pipes and filters (PF) architecture

The pipes and filters architecture divides the system into independent components, called filters. Each filter is responsible for a specific operation on the data flow at runtime. First, data enters through a pipe, then it is transformed, and the processed data is sent to an output pipe.

Each filter can also be modified or replaced without affecting the other filters. This modularity facilitates system maintenance and evolution. In this sense, the PF pattern becomes an option for applications that require efficient and scalable data processing, but whose maintenance can be complex.

The pipe and filter nomenclature originates from the original Unix Shell system. The Shell is a type of software called an interpreter, whose model allows processes to be linked using **pipes**, which facilitate the flow of text from one process to another. After the data is input, **filters** are applied to effectively process the data that can be handled within the program flow.

By briefly understanding how the pipe and filter architecture model works, we note that its application is quite helpful for sequential data processing and transformations, because it presents an easy-to-understand flow and allows for the reuse of transformations through **filters**.

### Monolithic architecture

It’s a single, vertically created block with all components, functionalities, and structures implemented together. This means that functionalities can run in a single process, or if modularized, all layers of the software are interdependent. Each modified part of the software can affect the behaviour of the whole.

According to Sam Newman’s analysis in *Building Microservices*, we can categorize frequently occurring monolithic systems into three types: single-process monolithic systems, modular monolithic systems, and distributed monolithic systems.

A web application can be defined as a monolith based on its production-ready package. Therefore, if you have a single package, your application is monolithic.

We refer to a **modular monolithic system** as one that presents a characteristic division into modules of its service layer. This division does not negate the concept of monolithic architecture, but aims to organize the code so that each service represents a functional unit. It also allows for its development with a certain degree of independence, ensuring greater readability and ease of maintenance compared to a **monolithic system with a single process**. Modular systems enable some degree of parallelism in work, but this must be designed according to the business logic.

A **monolithic system with a single process** has its entire codebase executed within a single process. Due to their integration, the system’s functionalities share resources and the same memory address space within a single process.

Sam Newman also describes the **distributed monolithic system**. The author states that the definition closely resembles SOA architecture, but often lacks the advantages of service-oriented architecture. In practice, a distributed monolith typically arises when there is a lack of focus on understanding the problem to be solved, resulting in a highly coupled architecture where theoretically small changes encompass a much larger scope and cause failures at various points in the system.

However, with initial planning and analysis of the business logic, it is possible to work with modularized monoliths and avoid complete coupling of all components.

While it has disadvantages such as using a single technology, being inflexible for scalability, and presenting the infamous single point of failure—when the entire process is prevented from executing if one of the components fails—**the advantages are very interesting for certain businesses**, such as:

- Lower implementation complexity.
- Deployment of a single unit, a single package, into production.
- Rapid development, as it allows an application to be executed by a smaller team, enabling an MVP (minimum viable product) or even a proof of concept more quickly.

The technical advantages and disadvantages depend on the project’s scope and purpose. Using a single stack can be seen as an advantage if the application doesn’t require resource sharing or significant decoupling, as this will likely facilitate smoother maintenance and team interaction. However, depending on the problem being solved, it may be perceived as lacking flexibility for developing new features.

It’s due to some of the factors mentioned that monolithic systems are perceived as legacy, and monolithic architecture is viewed as outdated by some in the technology community. However, we know that **not everything is suited for microservices**, and the success or failure of implementing this architecture will depend on understanding the problem being solved.

Monolithic architecture is a valuable and worthwhile approach to explore. There are success stories of its application in large companies, such as Amazon Prime Video, which migrated after realizing that the monolith works best for its business model, resulting in a 90% reduction in maintenance costs. Stack Overflow, Shopify, and GitHub also employ a monolithic architecture in their business models.

### Microservices-based architecture

Microservices are distributed applications composed of several smaller applications to create complex systems. Each service operates independently, and its modelling is based on a business domain. It is possible to encapsulate functionality through one service and make it available to others through, for example, REST APIs or messaging services.

Microservices architecture can be considered a variant of service-oriented architecture, in which services are decomposed into smaller, more independent services, providing greater flexibility for the division of work within the team and the implementation of new services. Microservices also allow for the use of different technologies and languages, something not possible in a monolith. Another important business point is that microservices make it easier to scale infrastructure resources for products according to peak access.

Microservices facilitate system scalability and mobility. However, the requirements for their implementation are higher, as the costs and complexity of deployment and maintenance are high. The question to ask in these cases is: “Is the complexity of the microservices architecture justified?”

Therefore, the application of a microservices-based architecture must be carefully analyzed due to its complexity, and above all, considering the need for its implementation tailored to the business domain.

### Hexagonal architecture

The hexagonal architecture pattern, also known as ports and adapters, treats business logic and implementation logic separately. The hexagonal architecture is advantageous because it decouples the application from the environment through the concepts of ports and adapters, facilitating maintenance and integration with other application components.

Ports are the interfaces that enable business logic to communicate with the outside world, and adapters are responsible for implementing these interfaces. In this sense, its application is advantageous because it also allows for the implementation of other architectures with a certain degree of flexibility. Therefore, the core (the essence) of the application must be well defined.

Business logic is fundamental to creating the system’s functionalities, and Domain-Driven Design helps in understanding the domains and acting efficiently in building the hexagonal architecture.

The architecture is divided into self-contained layers isolated from the outside world. The application domain is the piece that governs the development of the components. The premise of the hexagonal architecture is to protect the domain layer at the center and allow it to connect to the outside world through a standard interface, simply by replacing the adapter you use. This means you need to integrate your system with a library, infrastructure, or other relevant components.

The hexagonal architecture aims to solve one of the main problems in software development: coupling. This architecture presents a distinct view of an application’s layering, where the first layer typically serves as the interface and the last as a database for storage. The idea is to understand the front-end and back-end as layers external to your domain!

The hexagonal architecture is applied through principles such as dependency inversion.

Users interact with the system through different interfaces. Regardless of the access method, this interaction is always facilitated by adapters. Adapters, in turn, connect to an input port, which specifies the methods for performing various operations. These methods are concretely implemented by the classes that represent the domains in the system.

To store important information, the system uses an output port. Connected to this port is an adapter.

A system may have multiple input and output ports, always located near the domain classes. One or more adapters can be connected to a specific port, whether it is an input or output port. This organization facilitates efficient and structured user interaction with the system because it is pretty flexible.

## What is the best software architecture?

There are several other types of software architecture patterns, such as cloud architecture, distributed architecture, cluster architecture, configuration management architecture, performance management architecture, security management architecture, event-driven architecture, publish-subscribe (Pub/Sub) architecture, clean architecture, and peer-to-peer architecture. Understanding the problem is crucial to developing an effective solution.

Therefore, choosing the best software architecture begins with understanding the problem that will be transformed into a solution. Using models and patterns greatly helps develop quality software, but to do so, you need to understand your business model and the limitations and advantages of each pattern. Next, keep in mind that software architecture is not a closed format; it is not rigid, and it allows you the freedom to make the best decisions in your code.

Software architecture isn’t a one-size-fits-all; it’s a living thing that can grow and evolve. In practice, it requires continuous study, and while it’s a complex subject to define theoretically, it’s not inaccessible. You are fully capable of applying patterns, and your primary skill is understanding the problem well enough to design and architect a solution based on patterns and best practices. After all, inappropriate choices generate rework and higher software development costs.

Given the vast array of patterns and approaches to software architecture presented, it’s clear that choosing the right one plays a crucial role in developing efficient and sustainable systems. Furthermore, all patterns have advantages and disadvantages, and the journey of transforming an idea into functional software requires, in addition to technical skills, a deep understanding of the business requirements and the nuances of the domain in question.