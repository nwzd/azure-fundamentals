# Monitoring & Managing in Azure

In this chapter, you'll learn about monitoring and management tools and services from Microsoft Azure.

## Monitoring Services in Azure
In this section, you will discover the various Microsoft monitoring options and examine the selection criteria used by professionals to determine which service is best for a certain situation. 

### Product Options

At a high level there are three primary Azure monitoring offerings: Azure Advisor, Azure Monitor, and Azure Service Health. 

1. Azure Advisor: This tool evaluates your Azure resources and provides recommendations to improve reliability, security, performance, **cost optimization**, and operational excellence. It helps you save time on cloud optimization by offering actionable suggestions that you can implement right away or postpone for later.

2. Azure Monitor: It is a comprehensive platform for collecting, analyzing, visualizing, and taking action based on **metric and logging** data from your Azure and on-premises environment. Azure Monitor allows you to view real-time and historical performance across different layers of your architecture, set up alerts for critical events, and use the data to trigger auto-scaling functionality. Some popular products such as Azure application insights uses Azure Monitor under the hood.

3. Azure Service Health: This tool notifies you about Azure service incidents and planned maintenance events, helping you mitigate downtime. It provides a personalized view of the health of Azure services, regions, and resources you rely on. You can set up alerts, access incident reports, and track planned maintenance events to minimize the impact on your **availability**. Service Health provides official incident reports called Root Cause Analysis or RCA's, which you can share with stakeholders.
 
### Decision Criteria

- Azure Advisor is the right choise to better understand and optimize both cloud costs and security
- Use Azure Monitor when you want to gain insight into performance of services and troubleshoot specific issues
- Use Azure Service Health to know about upcoming planned downtime in advance, service interruptions that affects many Azure customers.


## Management Tools

Administrators, developers, and managers can use Azure management tools to interact with the cloud environment and perform tasks such as deploying resources, configuring services, and viewing reports.

### Product Options

1. Visual Tools: These tools provide a user-friendly interface for accessing Azure functionality. The Azure portal is a web-based user interface that allows you to view and manage all your Azure services. It provides features like creating new services, configuring existing services, and generating reports.

2. Code-based Tools: Code-based tools are more suitable for setting up large deployments of resources with complex interdependencies and configuration options. Azure PowerShell and Azure CLI are two code-based tools provided by Microsoft. Azure PowerShell allows developers and IT professionals to execute commands called cmdlets, which interact with the Azure REST API to perform management tasks. Azure CLI, on the other hand, allows you to execute commands in Bash and interact with the Azure REST API. This approach to managing hardware and Cloud resources which developers use when they write application code is referred to as infrastructure as code


Although it's possible to write imperative code in Azure PowerShell or
the Azure CLI to setup and tear down an Azure resource, by using Azure Resource Manager templates, you can describe the resources you want to use in a declarative JSON format. The benefit is that the entire ARM template is verified before any code is executed to ensure that the resources will be created and connected correctly. The template then orchestrates the creation of those resources in parallel. 

### Decision Criteria

* Using their Azure PowerShell or the Azure CLI if you need to quickly obtain the IP address of a virtual machine you've deployed, reboot a VM, or scale an app. These tools are more suitable to perform **one-off** management, administrative, or reporting actions

* Azure Resource Manager templates express the infrastructure
requirements for your application for a **repeatable and reliable** deployment. ARM templates aren't intended for one-off scenarios, but depending on the scenario, it's possible to use them for this purpose.

* If you need to set up and manage resources infrequently, or prefer a visual interface for viewing reports, it makes sense to take advantage of the **visual** presentation that the Azure Portal offers.

*  Azure mobile app, which you can access **remotely** via an iOS or Android phone or tablet. is likely the best choice when a laptop isn't readily available and you need to view and triage issues immediately.