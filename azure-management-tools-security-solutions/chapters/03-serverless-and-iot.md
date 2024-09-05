# Microsoft Azure Serverless & IoT

In this chapter you will be introduced to Azure serverless computing technologies and an array of Azure IoT services.

## Microsoft Azure Serverless Technology

Serverless computing refers to an execution environment that is pre-configured and managed on your behalf. You simply define the desired outcomes by writing code or using a visual editor to connect and configure components. You then specify the triggers for your functionality, such as a timer or an HTTP request. The best part is that you don't need to worry about outages. Your code can scale instantly to meet demand, and you only pay for the actual usage of your code.

The section focuses on two serverless computing solutions in Azure: Azure Functions and Azure Logic Apps. 

### Product Options

1. **Azure Functions** is a service that allows you to host a single method or function in the cloud, which runs in response to an event. It supports multiple programming languages and **scales** automatically based on demand. Azure Functions is ideal for tasks that can be completed quickly within seconds or less.

2. **Azure Logic Apps** is a low-code development platform that helps automate and orchestrate tasks, business processes, and workflows. It simplifies the design and building of scalable solutions by linking **triggers** to actions with connectors. Logic Apps can integrate apps, data, systems, and services across enterprises or organizations.

The main difference between Azure Functions and Azure Logic Apps is their intent. Azure Functions is a serverless compute service, while Azure Logic Apps is a serverless orchestration service. 

Additionally, the two services are priced differently. Azure Functions pricing is based on the number of executions and the running time of each execution. Logic Apps pricing is based on the number of executions and the type of connectors that it utilizes.

Both Azure Functions and Azure Logic Apps are core Azure services for serverless computing and help developers build robust cloud apps with minimal code.

### Decision Criteria

Azure Logic Apps and Azure Functions both offer orchestration capabilities, but they cater to different user preferences and needs:

- **Azure Logic Apps**: Designed for orchestration with a web-based visual configurator. It excels at connecting various services via APIs, abstracting away the details of API calls. It's ideal for users who prefer a **visual**, low-code environment, such as IT professionals and business analysts.

- **Azure Functions**: Allows for the full expressiveness of programming languages, making it suitable for **complex** algorithms and data operations. It's best for developers who prefer an imperative programming environment and have existing code in languages like C#, Java, or Python.

Ultimately, the choice depends on whether you prefer a declarative (visual) or imperative (code-based) approach to automation and orchestration.

## Microsoft Azure IoT Services

IoT devices equipped with sensors can gather and send data to Azure IoT services for analysis. This data can be aggregated into reports and alerts. Additionally, Azure IoT services can send firmware updates to devices to fix issues or add new features.

### Product Options

1. **Azure IoT Hub** is a cloud-hosted service that acts as a central hub for bidirectional communication between IoT applications and devices. It supports reliable and secure communication for millions of devices, enabling device-to-cloud telemetry, file uploads, and cloud-to-device commands. IoT Hub can route messages to other Azure services and allows for remote control of devices. It also provides monitoring to track device health and events.

2. **Azure IoT Central** is an application platform that builds on IoT Hub by adding a user-friendly dashboard. This dashboard allows you to connect, monitor, and manage IoT devices easily. Key features include:

    * Visual Interface: Quickly connect new devices and monitor their telemetry.
    * Performance Monitoring: View overall performance across all devices.
    * Alerts: Set up notifications for device maintenance needs.
    * Updates: Push hardware and software updates to devices.

    To help you get started, IoT Central offers starter templates for various industries like retail, energy, healthcare, and government. These templates can be customized directly in the UI, including themes and logos.

    You can also control devices remotely, such as adjusting the temperature of refrigerated vending machines. Device templates are crucial, as they allow devices to connect without service-side coding, defining dashboards, alerts, and more. However, device developers still need to create code that matches the device template specifications.

3. **Azure Sphere** Azure Sphere provides a secure, end-to-end IoT solution, covering hardware, operating systems, and secure communication. It consists of three main components:

    * Micro-controller Units (MCUs): Process the OS and sensor signals.
    * Customized Linux OS: Manages communication with the security service and runs vendor software.
    * Azure Sphere Security Service (AS3): Ensures devices are not compromised, handles authentication, and pushes updates.

    These components work together to securely connect, manage, and update IoT devices.

### Decision Criteria

* **Azure Sphere**:  Whether you're a manufacturer or a customer, it's crucial to ensure your devices aren't compromised for criminal activities. If **security** is a top priority in your product design, Azure Sphere is the best choice

* **Azure IoT Hub**: If your needs are simpler, such as connecting to remote devices for telemetry and **occasional** updates without requiring reporting capabilities, Azure IoT Hub is a suitable option.

* **Azure IoT Central**: For those who want predefined **templates** for common industry scenarios or the ability to customize, IoT Central is the ideal choice.