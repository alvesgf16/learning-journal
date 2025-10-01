# Mobile Development

## What is an app?

- An **application**, commonly known as an app, is a program designed to help perform specific tasks on devices
- **Applications** serve various functions and share the goal of **solving specific problems or simplifying tasks in daily life**
- The term **application** comes from the Latin word *applicare*, meaning "to place on" or "to bring near"
- In technology, applications are tools we "apply" to execute tasks on computers or smartphones
- The concept of apps significantly changed in 2007 with the launch of the first iPhone by Apple
- Prior to the iPhone, programs existed for computes and older cell phones, but the iPhone popularized easy-to-download and install small programs 
- Apps revolutionized technology usage in daily life, transforming smartphones into command centers
- Today, apps are essential in everyday tasks, such as waking up with an alarm clock or relaxing with a video app before bed

## What is an app for?

- Apps are designed to **simplify and enhance our lives**
  - They automate tasks and make processes faster and more accessible
  - Provide tailored experiences that fit our needs conveniently

### App stores

- Serve as secure, centralized platforms for downloading and installing apps
- Minimize concerns about viruses or malfunctioning software
- Users experience enhanced security when downloading apps
- Developers gain a dependable method to distribute their apps
- Instant access to apps without needing to leave home or wait for extended periods
- Quick downloads and installations with just a few taps on the screen

## How apps work

- Each app communicates with your phone and uses the device's own tools to perform tasks
- Each app is designed to utilize different features of the device, ensuring an optimal user experience
- Not all apps are created equal; **different types interact with the phone in unique ways**, even if they have similar functions

### Global Positioning System (GPS)

- GPS allows the phone to know your real-time location
- Maps apps use this information to display routes and suggest nearby places

### Camera

- Allows users to take photos, record videos, and share them with friends
- Apps like Instagram or WhatsApp communicate with the phone's camera features

### Gyroscope

- A sensor that detects device orientation (e.g., turning the phone)
- Enables the screen to adjust as you turn the device
- Used in games that require physical phone movements (e.g., steering wheels)

## Types of applications

### Native apps

- Created specifically for an operating system (e.g., Android, iOS)
- **Developed using OS-specific languages and tools**
  - iOS: Swift (or Objective-C), exclusive to Apple devices (iPhones, iPads, Apple Watch)
  - Android: Kotlin (or Java), tailored for millions of devices (smartphones, tablets, smartwatches running Android Wear)
  - Smart TVs and Native Apps: e.g., Samsung's Tizen, LG's webOS, optimized for remote controls and large screens
- This diversity makes native development appealing to developers
- **Full access to device features** (e.g., camera, GPS, gyroscope)
- Developing a native app requires thorough knowledge of each system
- Results in an app that looks and functions precisely as intended for that specific platform
- Fast and efficient performance

#### Advantages

- Choosing to create a native app directly impacts its performance and device power utilization
  - E.g., developing a game for iPhone allows access to iOS features (e.g., enhanced graphics, camera use for augmented reality)
  - Apps run more smoothly by leveraging all device features tailored for the operating system
- Native development allows teams to specialize in either Android or iOS, resulting in a more refined user experience
- Companies can create features reliant on specific device sensors (e.g., facial recognition on iPhone) without adapting for other systems
- Each platform has distinct tools and languages, enabling the formation of specialized teams
  - This specialization encourages deeper exploration of advanced features
- Creating native applications provides the freedom to maximize hardware and system benefits, resulting in highly optimized applications for end-users

#### Disadvantages

- **Cost** issues
  - Separate development for each operating system (iOS and Android)
  - Requires multiple teams of developers, increasing budget and development time
  - Results in two different app versions rather than a single version
- **Maintenance** concerns
  - Native apps must be updated with platform changes and updates
  - Regular updates needed for iOS and Android to work with new features or internal changes
  - High long-term costs due to specificities and constant updates of each system
- Flexibility limitations
  - Native apps are tailored to specific platforms, creating a "lock-in" effect
  - Launching on new platforms (e.g., Windows, Tizen, Wear OS) often requires starting from scratch
  - Lack of flexibility can be a significant hurdle for startups or companies wanting to be present on multiple platforms without excessive time and financial investment

#### Examples

**WhatsApp**

- A prime example of a native app
- Deep integration with the phone's system
- Utilizes features such as camera, microphone, and notification system
- Seamless operation for sending photos and making voice calls
- Uses native push messaging for immediate notifications

**Spotify**

- Designed to leverage the device's audio system
- Integrates with volume controls and background playback
- Allows playback while multitasking (e.g., sending messages or browsing)
- Connects with hardware to adjust audio based on bluetooth headphones or speakers

**Pokémon Go**

- Native app that heavily uses mobile features
- Utilizes GPS for location tracking, camera for augmented reality, and gyroscope for immersive experience
- Facilitates Pokémon appearances in the real world through sensor integration

**Waze**

- Popular navigation app with accurate GPS connection
- Guides users through traffic in real time
- Integrates network data for traffic updates, speed camera alerts, and accident reports
- Utilizes native notification system
- Capable of running in the background for alerts when the app is closed

### Web apps (Progressive Web Apps, PWAs)

- **Accessed directly through a browser**; no download required
- Function like websites with app-like features (e.g., large buttons, notifications, offline capability)
- **Built with web technologies (HTML, CSS, JavaScript)**
- Can run on any device with a browser
- Convenient for saving device store space
- Quick access to services without instalation hassle
- Can work offline if some data has been loaded
  - In areas with limited internet access, basic functions of a PWA remain usable
  - Temporary data storage on the device allows continued use of certain features
- Limited access to device resources compared to native apps
- Generally slower than native apps

#### Advantages

- For companies:
  - **Flexibility**:
    - Web apps function across devices: iPhones, Androids, and computers, needing only a browser and internet connection
    - No dependence on app stores for access
    - Direct access via a link, bypassing store approval processes and compatibility issues
    - Continuous updates without waiting for external approvals, ensuring quick feature releases and bug fixes
    - Users are not required to download new versions
  - Improved **reach**:
    - Lower barriers to entry for users who don’t need to worry about storage or system compatibility
    - Users can access the app directly through a browser link
    - Ideal for targeting a diverse audience without developing multiple app versions
- For teams:
  - Simplified development:
    - Focus on a **single version** rather than separate apps for Android and iOS
    - Centralized **code management** for easier updates and efficiency
    - Leaner, more agile teams, eliminating the need to cater to specific operating systems
- For users:
  - Convenience:
    - Accessing apps without using device storage
    - Practical solution for those reluctant to download too many apps or limited by storage space
    - Progressive Web Apps (PWAs) provide essential functionality without compromising user experience

#### Disadvantages

- Web applications provide numerous benefits but also have notable issues that need consideration in relation to company goals
- Limitations can affect both user experience and development strategies
- PWAs function similarly to native apps but cannot access all device features equally
  - Advanced uses of GPS, specific camera controls, and sensors (like gyroscopes) may be limited
  - Barriers may be faced based on the user’s device and browser
- PWAs operate within browsers, subjecting them to limitations imposed by those browsers
  - Feature support varies among different browsers (e.g., an app may work well in Chrome but not in Safari)
  - This inconsistency can be frustrating for developers and users
- Many PWAs offer some offline support, but full functionality typically relies on a good internet connection
  - Weak signals or lack of connectivity can hinder app performance and usability

#### Examples

**Google Docs**

- A web app that allows direct document editing in the browser
- No downloads required
- Offers features similar to traditional text editors, including automatic saving
- Accessible from any device with internet, enhancing collaborative work

**Netflix**

- Known for its mobile app, but also functions well in the browser
- Watch movies and series in the same quality as the app, without downloads
- Useful for computers without the app installed or smart TVs using the browser
- Intuitive navigation with quick video loading

**Trello**

- Excellent web app for organizing tasks and projects
- Features a visually convenient interface to create lists, drag cards, and track progress
- Boards are synchronized across devices (phone, tablet, computer) for easy access

**Airbnb**

- Quick search and booking of accommodations directly in the browser
- Smooth website experience with user-friendly filters and interface
- Simplifies the process of finding accommodations for short or long trips, ideal for users who prefer not to install apps or are using temporary devices

### Hybrid apps

- **A cross between native apps and web apps**
- Developed with a single codebase usable on both Android and iOS
- Do not rely on web technologies like PWAs
- Utilize frameworks such as: **Flutter, Kotlin Multiplatform (KMP), Xamarin, React Native, Ionic**
  - **Flutter**
    - Developed by Google
    - Draws everything on the screen using the device’s canvas
    - Provides **complete control over app design**
    - Native components are not used; specific plugins required for features (e.g., camera, GPS)
    - Plugin maintenance depends on the developer community
  - **React Native**
    - Created by Facebook
    - Code is written in JavaScript
    - Utilizes native components of each system
    - **Ensures familiar behavior and appearance** consistent with native Android/iOS
    - Uses plugins for device resources, maintained by the developer community
  - **Ionic**
    - Follows a web-like approach
    - Utilizes HTML, CSS, and JavaScript; runs within a WebView
    - **Functions like a website installed on a phone**
    - Accesses some native features (e.g., notifications, GPS) through plugins
    - Ideal for those with web development experience
  - **Kotlin Multiplatform (KMP)**
    - Developed by JetBrains
    - **Allows writing shared code while keeping platform-specific parts separate**
    - Common foundation for app logic and business rules
    - Flexibility to use native features when necessary
    - Shares maximum code between platforms without compromising native capabilities
- Allows code to be written once and deployed across multiple platforms, saving time and resources
- **Heavy reliance on plugins for native features**
  - Plugins are often community-created and maintained
  - Potential issues with plugin updates and feature support

#### Advantages

- Combines the **benefits of both native and web apps**
- **Enables development for multiple platforms simultaneously**
- Ideal for smaller development teams or companies with tight timelines
- Reduces resources spent on developing separate native apps for Android and iOS
- Allows for seamless integration and compatibility across platforms
- Saves time, enabling the team to focus on new features instead of duplicating work
- Maintains the look and feel of native components while using shared code
- Enables adjusting the app for each platform as needed
- Ensures smooth functionality and familiarity for both Android and iOS users
- Updates and fixes can be implemented in one place
- Changes are reflected across all platforms, reducing complexity
- **Streamlines the management of app versions**
- Facilitates quicker deployment of updates

#### Disadvantages

- **Dependence on plugins for native device features (camera, GPS, facial recognition)**
  - Many plugins are community-maintained, creating both benefits and drawbacks
  - New iOS or Android versions may change functions, requiring timely plugin updates for compatibility
  - Outdated plugins can lead to app crashes or loss of features
  - Development teams rely on third parties to maintain app performance after OS updates
- Can be optimized to mimic native apps, but will never be completely identical
  - **Minor differences in component behaviour** may arise, especially on older/mobile devices with uncommon configurations
  - Companies aiming for the best user experience might need to make manual adjustments for platform compatibility
- Generally provide good **performance** but may struggle with complex features (e.g., games, augmented reality)
  - Companies should assess whether the time and cost savings of hybrid development outweigh potential performance limitations

#### Examples

**Instagram**

- Initially developed as a native app
- Evolved to a hybrid approach with React Native for added features and multi-platform support
- Maintains fluid navigation and integration with native mobile features (camera, notifications)
- Allows quick implementation of new features without rewriting code for both Android and iOS

**Uber**

- Primarily uses React Native as a hybrid app
- Quickly accesses device GPS to locate the user’s position and display nearby drivers
- Essential integration with native features (maps, notifications) enhances user experience
- The development team can share code across platforms while ensuring quality

**Microsoft Teams**

- Utilizes a hybrid approach for seamless operation across devices and systems
- Focuses on accessibility as a work communication tool
- Available on both computers and mobile devices
- Ensures a consistent experience, facilitating easy transition between platforms
- Supports seamless messaging, calls, and file sharing, showcasing hybrid technology benefits

## How to choose the best type of application?

- The answer isn’t simple; it **depends on the goals and methods for developing the app**
  - Consider **what you want your app to achieve**
  - Assess **willingness to invest** money, time, and effort
- Several approaches are available, each with unique characteristics
- Ideal solutions may vary based on the organization’s size:
  - What works for a giant tech company may not suit a startup
  - Smaller projects may require different considerations
- Choice depends on the project's needs and the team's capabilities
  - Each approach comes with its own advantages and challenges
  - **Understanding goals and available resources** is crucial for making the best decision

### What is the goal?

<table>
  <thead>
    <tr>
      <th></th>
      <th>Native Apps</th>
      <th>Web or Hybrid Apps</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Best choice for</td>
      <td><strong>Functionalities needing direct hardware interaction</strong></td>
      <td><strong>Reaching the largest audience quickly and easily</strong></td>
    </tr>
    <tr>
      <td>Ideal for</td>
      <td>
        Advanced games<br>
        Augmented reality apps<br>
        High-performance features
      </td>
      <td>
        Projects requiring flexibility<br>
        Applications working across multiple platforms<br>
        Management systems<br>
        Communication apps<br>
        Limited use of the device’s native capabilities
    </tr>
    <tr>
      <td>Offers</td>
      <td>
        Deeper control over app capabilities<br>
        Full utilization of device features
      </td>
      <td></td>
    </tr>
  </tbody>
</table>

### How much investment is available?

| Native Apps | Web or Hybrid Apps |
| --- | --- |
| Ideal for larget budgets and dedicated teams | Great for those starting or working with a tight budget |
| Guarantee a more customized and polished experience | Allow for functional apps on multiple platforms with less development effort |
| Suitable for projects that require high quality and specific features | A smart alternative for optimizing time and resources |
| | Balance cost and results effectively |

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