# Describe Cloud Concepts

LP: https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/
LM: https://learn.microsoft.com/en-us/training/modules/describe-core-architectural-components-of-azure/

Identify Cloud Computing benefits, use GASHED:

* Geo-distribution
* Agility
* Scalability: Ability to adjust resources to meet demand. You only pay for what you use. Vertical scaling is focused on increasing or decreasing the capabilities of resources (scale up - scale down). Horizontal scaling is adding or subtracting the number of resources (sclae out - scale in).
* High Availability (SLA) High availability focuses on ensuring maximum availability, regardless of disruptions or events that may occur
* Elasticity
* Disaster Recovery
* Reliability: Ability of a system to recover from failures and continue to function
* Predictability: Predictability can be focused on performance predictability or cost predictability (Total Cost of Ownership (TCO) or Pricing Calculator)


## Azure Portal

Definition: Web-based unified console that allows you to build, manage, and monitor everything in Azure.

## Azure Marketplace

Definition: Connects users to partners and vendors that offer solutions/services for Azure

## Accounts

Azure Account -> Many subscriptions -> Many Resource groups -> Resources

## Types of Cloud

| Type | Description | Expenditure |
| --   | --          | -- | 
| Public | Services over the internet. Owned by a third party| OpEx |
| Private | Exclusive by users from a company. Can be on-premise, datacenter, or hosted by a third-party service provider.| CapEx |
| Hybrid | Combination of Public and Private| |


| Public cloud | Private cloud | Hybrid cloud |
| No capital expenditures to scale up | Organizations have complete control over resources and security	| Provides the most flexibility | 
| Applications can be quickly provisioned and deprovisioned	| Data is not collocated with other organizations’ data	| Organizations determine where to run their applications | 
| Organizations pay only for what they use	| Hardware must be purchased for startup and maintenance | Organizations control security, compliance, or legal requirements | 
| Organizations don’t have complete control over resources and security	| Organizations are responsible for hardware maintenance and updates | | 	

## Azure Arc
Azure Arc is a set of technologies that helps manage your cloud environment (public, private or hybrid)

## Azure VMware Solution
What if you’re already established with VMware in a private cloud environment but want to migrate to a public or hybrid cloud? Azure VMware Solution lets you run your VMware workloads in Azure with seamless integration and scalability.

## Expenses

Describe CapEx (Capital Expenditures) and OpEx (Operational Expenditures)

| Type | Description |
| -- | -- |
| Capital Expenditure (CapEx) | Up-front spending on infrastructure. Value is reduced over time | 
| Operational Expenditure (OpEx) | No up-front cost. Spending only on services and billed for what you use | 

## Consumption-Based Model

Is the basis of OpEx: 

* No up-front costs
* Only pay for what you use/need
* Pay for additional resources when they are needed
* Stop paying for what you don't use


## Cloud Service models


| Model | Description | Complexity/Ownership |
| -- | -- | -- | 
| IaaS | OS and Network owned by the user, including maintenance and configuration, suitable for lift-and-shift scenarios | High | 
| PaaS | Apps are deployed into a managed OS. No ownership of hardware or software requirements | Medium |
| SaaS | User only provides data. Everything else is managed. E.g. MS Office | Low |

## Subscriptions, Management Groups, and Resources

| Name | Definition | 
| -- | -- |
|Management Groups|Manage access, policy, compliance for multiple subscriptions|
|Subscriptions|Groups accounts with resources. Can be used to manage costs+resources|
|Resource Groups| A logical grouping of services (resources)|
|Resources| Services that you create. E.g. a Virtual Machine|

## Azure Regions

Definition: A geographical area with one or more datacenters nearby and networked together.

**Special Regions**: US DoD, US Gov: physically+logically isolated with additional compliance certifications. China 
is operated by 21Vianet.

There are some global Azure services that don't require you to select a particular region, such as Microsoft Entra ID, Azure Traffic Manager, and Azure DNS.

## Azure availability Zones

Definition: One or more physically separate datacenters within an Azure region. A.K.A. Isolation Boundary (HA/redundancy).

Availability Zones are interconnected with ultra high-speed, private, fiber network.

Not all regions have AZs.

Services that support AZs have these categories:

* **Zonal service**: Pins to a zone (for example, VMs, managed disks, IP addresses)
* **Zone-redundant**: Auto-replication across zones  (for example, zone-redundant storage, SQL Database)
* **Non-regional**: HA in an Azure geography. 

## Azure Region Pairs

Definition: Each Azure region is **always paired** with another region within the same geography.

AZs have one or more datacenters, and a Region has at least 3 zones. (¿?)

Helps protect against natural disasters or civil unrest. Separated at least 300 miles.

Replication resides always within the same Geography as the pair except for Brazil South.

Sovereign regions are instances of Azure that are isolated from the main instance of Azure. You may need to use a sovereign region for compliance or legal purposes. US DoD Central, China East..

## Azure resources and Azure resource Manager

**Resource**: A manageable item within Azure. Like a database or a VM
**Resource group**: A grouping of resources you want to manage as a group.

### Azure Resource Groups

Can contain anything you create in Azure to form a logical grouping of services (resources). Helps provide organization.

* **Life cycle**: If you delete a resource group, all contained resources are deleted as well. Makes it easier to get rid of.
* **Authorization**: A resource group is a scope for applying RBAC

### Azure Resource Manager

Definition: Deployment and management service for Azure. CRUD for Azure resources

* Manage infrastructure with templates
* Deploy, manage, and monitor
* Define dependencies between resources for correct ordering
* Apply RBAC and tags

## Azure subscriptions

Definition: Provides you with authenticated and authorized access to products and services. Always linked back to an account.

An account can have one or many subscriptions.

Types of subscription boundaries:

* **Billing boundary**: Determines how an Azure account is billed. You can create multiple subscriptions for different billing requirements.
* **Access Control boundary**: Access-management policies happen at the subscription level. You can control access+resources for specific subscriptions.

Additional subscription helps with:

* **Environments**: Separate environments via subscriptions. E.g. development and testing
* **Org structure**: Marketing and IT, helping manage access and limit resources
* **Billing**: Make it easier to track billing better.

## Azure management groups

Definition: Provides a level of scope above subscriptions. Helps organize subscriptions into groups.

Helps provide user access to multiple subscriptions with a single RBAC that gets inherited
A policy can be applied at management group so that it is inherited.
10,000 management groups can be supported in a single directory.
A management group tree can support up to six levels of depth. This limit doesn't include the root level or the subscription level.
Each management group and subscription can support only one parent.