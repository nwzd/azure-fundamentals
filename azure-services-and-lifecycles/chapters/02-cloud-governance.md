# Cloud Governance Strategy

In this chapter on Cloud Governance Strategy, you will learn about access policies, resource locks, and tags. You will be introduced to Azure services such as Azure policy and Azure blueprints, and how they can help you build a comprehensive cloud governance strategy. The module emphasizes the importance of governance in maintaining control over applications and resources in the cloud, ensuring compliance with industry standards and organizational requirements. By the end of this module, you will be able to make organizational decisions about your cloud environment, define access to cloud resources, apply resource locks and tags, control resource creation using Azure policy, and enable governance at scale across multiple Azure subscriptions using Azure blueprints.

## Cloud Adoption Framework 

The Cloud Adoption Framework for Azure provides guidance and tools to help organizations successfully adopt and implement cloud technologies. It consists of several stages, including defining a strategy, creating a plan, preparing the organization, adopting the cloud, and governing and managing the cloud environment. Each stage has specific steps and exercises to follow. The framework emphasizes the importance of documenting motivations, meeting with stakeholders, and choosing the right first project. It also highlights the need to create a landing zone in the cloud, migrate applications, and innovate with cloud services. Finally, the framework emphasizes the importance of cloud governance and management to ensure resilience and optimization

## Subscription Governance Strategy

The hierarchical structure for managing an organization’s resources in Azure consists of four levels: resources, resource groups, subscriptions, and management groups.

- Resources are instances of services you create, such as virtual machines, storage, or SQL databases.
- Resource groups act as logical containers for these resources, allowing you to deploy and manage them together.
- Subscriptions group user accounts and the resources created by those accounts, with limits on the amount of resources you can create and use. Subscriptions help manage costs and resources for users, teams, or projects.
- Management groups help manage access, policy, and compliance across multiple subscriptions, with all subscriptions in a management group inheriting its conditions.
When creating and managing subscriptions, consider billing, access control, and subscription limits. You can generate one billing report per subscription, and organizing subscriptions by department or project can facilitate cost management. Resource tags can also be useful.

Each subscription is associated with an Azure Active Directory tenant, allowing administrators to set granular access controls using Azure role-based access control. When designing your subscription architecture, consider whether you need separate subscriptions for development and production environments to control access and isolate resources. Be aware of resource limitations, such as the maximum number of Azure ExpressRoute circuits per subscription, and plan accordingly. Management groups can assist in managing multiple subscriptions by overseeing access, policies, and compliance.

## Azure Role-Based Access Control (RBAC)

Azure role-based access control (RBAC) is a system that allows organizations to control who has access to their Azure resources and what they can do with those resources. RBAC is enforced through Azure Resource Manager, which provides a way to organize and secure cloud resources. 

RBAC allows organizations to grant users only the rights they need to perform their job and only to the relevant resources. It uses a role and scope model, where roles are assigned to users, groups, or applications at different levels of scope, such as management group, subscription, resource group, and resource. 

There are built-in roles in Azure, such as reader, contributor, and owner, which have different levels of access and permissions. If the built-in roles don't meet the specific needs of an organization, custom roles can be created. 

RBAC is enforced on any action initiated against an Azure resource that passes through Azure Resource Manager. It uses an allow model, where if multiple role assignments grant different permissions to the same resource, the user has both permissions. 

Access permissions are managed through role assignments, which attach a role to a security principle (user, group, service principal, or managed identity) at a particular scope. Role assignments control how permissions are enforced, and the scope determines the set of resources to which the permissions apply. 

RBAC allows organizations to segregate duties within teams and grant only the necessary access to users. It provides a way to control access to Azure resources and ensure security and compliance.

## Resource Locks

Resource locking is an additional layer of access control that prevents resources from being accidentally deleted or changed. It acts as a warning system to remind administrators that a resource should not be deleted or modified.

There are two types of resource locks in Azure - "Cannot delete" and "Read-only". "Cannot delete" allows authorized users to read and modify a resource but prevents them from deleting it without removing the lock. "Read-only" allows authorized users to only read the resource and restricts them from deleting or modifying it.

Resource locks can be applied at the subscription, resource group, or resource level. They can be managed from the Azure portal, PowerShell, Azure CLI, or Azure Resource Manager template.

To modify a locked resource, the lock must first be removed. This additional step helps protect administrators from making unintended changes.

Resource locks apply regardless of RBAC permissions. Even if someone is an owner of the resource, they still need to remove the lock before performing any blocked activity.

Azure blueprints allow you to define a set of standard Azure resources for your organization. You can specify that a certain resource lock must exist, and if the lock is removed, Azure blueprints can automatically replace it.

## Resource Tags

Resource tags are a powerful tool for organizing resources and providing extra information or metadata about them. We discuss various use cases for tags, including cost management, operations management, security, governance and regulatory compliance, and workload optimization and automation. 


## Azure Policy

Azure Policy allows you to define policies that enforce rules and effects on your resource configurations to ensure compliance with corporate standards. It enables you to create individual policies and groups of related policies known as initiatives. Azure Policy evaluates your resources and highlights non-compliant resources. It can prevent non-compliant resources from being created and automatically remediate non-compliant resources and configurations.

To implement a policy, you need to create a policy definition that expresses what to evaluate and what action to take. Policy definitions have conditions and effects that determine when they are enforced.
Azure Policy provides built-in policies that you can use, such as VM skew size restrictions, geographic compliance requirements, multi-factor authentication, and more.

Policy assignments are policy definitions applied to specific scopes, such as management groups, subscriptions, or resource groups. Assignments are inherited by child resources within the scope. You can review the evaluation results of policy assignments and take necessary actions.

Azure Policy initiatives group related policies into sets to track compliance for larger goals. Initiatives contain multiple policy definitions and can be assigned to specific scopes. Azure Policy includes built-in initiatives for monitoring security recommendations and supporting regulatory compliance standards.

## Azure Blueprints

Azure Blueprints allow us to define a repeatable set of governance tools and standard Azure resources that can be enforced across multiple subscriptions. The three steps involved in implementing a blueprint: creating a blueprint, assigning the blueprint, and tracking the blueprint assignments. Blueprints preserve the relationship between the blueprint definition and the deployed resources, enabling tracking and auditing deployments. Blueprint can have versions and parameters for flexible configuration. 

# Privacy & Compliance & Data Protection Standards

The Microsoft Privacy Statement outlines the personal data Microsoft collects, how it is used, and for what purposes. It applies to all Microsoft services, websites, apps, software, servers, and devices, ranging from enterprise products to home devices and educational software. The statement also includes information specific to products like Windows and Xbox.

The Online Services Terms (OST) is a legal agreement between Microsoft and its customers, detailing the responsibilities of both parties regarding the processing and security of customer and personal data. The OST is specific to Microsoft Online Services licensed through subscriptions, such as Azure, Dynamics 365, Office 365, and Bing Maps.

The Data Protection Addendum (DPA) further specifies the data processing and security terms for Online Services. It covers compliance with laws, data disclosure, security practices and policies, data encryption, data access, customer responsibilities, auditing compliance, data transfer, retention, and deletion.

Azure Government is a distinct version of Microsoft Azure designed to meet the security and compliance needs of U.S. federal, state, and local governments, as well as their solution providers. It ensures physical isolation from non-U.S. government deployments and employs screened U.S. personnel. Azure Government handles data subject to specific government regulations, such as those from the National Institute of Standards and the Department of Defense, using data centers and networks located exclusively in the U.S.

Customers, including government entities and their partners, must validate their eligibility to use Azure Government. It offers the highest level of compliance, including Level 5 Department of Defense approval, and is available in eight regions, boasting the most compliance certifications of any cloud provider.

Azure China 21Vianet is a separate instance of Microsoft's cloud services located in China, operated independently by Shanghai Blue Cloud Technology Company (21Vianet), a subsidiary of Beijing 21Vianet Broadband Data Center Company. This setup ensures compliance with Chinese regulations, which require cloud service providers to have value-added telecom permits and be locally registered with less than 50% foreign investment.

Azure China 21Vianet uses the same technologies as Microsoft's global services, such as Azure, Office 365, and Power BI, but operates independently. Contracts in China are signed between customers and 21Vianet, leading to differences in operation models and service availability compared to global Azure. Despite these differences, Azure China 21Vianet maintains high service quality and complies with Chinese security regulations, making it the first foreign public cloud service provider in China to do so.

# Azure Costs

The cost of Azure implementation is influenced by various factors, including:

- Resource Type and Customization: Different types of Azure resources have different costs associated with them. For example, when creating a storage account, you can choose the type of storage (e.g., block blob or table storage), performance tier (standard or premium), and access tier (hot, cool, or archive). Each option has its own cost implications.

- Usage Meters: Azure uses meters to track the usage of resources. These meters generate usage records, which are used to calculate your bill. Meters track specific types of usage, such as CPU time, network traffic, disk size, and operations. The usage tracked by meters correlates to billable units, and the rate per unit depends on the resource type.

- Azure Subscription Types: Different Azure subscription types have different pricing structures. For example, an Azure free trial subscription provides access to certain Azure products for free for 12 months, while other subscription types may include usage allowances or discounts.

- Azure Marketplace: Azure Marketplace allows you to purchase Azure-based solutions and services from third-party vendors. These solutions may have their own pricing structures, set by the vendor.

- Azure Region and Network Traffic: When provisioning resources in Azure, you need to choose the location (Azure region) where they will be deployed. Different regions may have different associated prices. Additionally, network traffic between regions can incur additional costs, so it's important to consider the location of your resources and the flow of network traffic.

- Billing Zones: Some Azure services have pricing based on billing zones, which are geographical groupings of Azure regions. The cost of outbound data transfers can vary based on the zone.

To estimate and manage costs effectively, Azure provides tools like the Azure pricing calculator. This tool allows you to select Azure products and configure them according to your requirements, providing a consolidated estimated price with a breakdown of costs for each resource. It's important to note that the pricing calculator provides estimates and not actual price quotes, as actual prices can vary based on factors like the date of purchase and payment currency.

## Minimize and Manage Costs

Before deploying any solution on Azure, it is important to carefully consider the products, services, and resources needed. Reading the relevant documentation and using tools like the pricing calculator and TCO calculator can help in estimating the costs.

Azure Advisor is a tool that identifies unused or underutilized resources and provides recommendations to optimize resource usage. These recommendations are sorted by impact and can range from automatically fixing issues to requiring human intervention.

If you have a free trial or credit-based Azure subscription, you can set spending limits to prevent accidental overruns. When the credit is exhausted, resources are removed from production, and virtual machines are stopped and de-allocated.

Azure reservations offer discounted prices on certain Azure services. By reserving services and resources in advance, you can save up to 72% compared to pay-as-you-go prices. Azure reservations are available to customers with an enterprise agreement, Cloud Solution Providers, and pay-as-you-go subscriptions.

The cost of Azure products, services, and resources can vary across locations and regions. It is recommended to use them in locations where they cost less. However, it is important to consider the outgoing egress network bandwidth consumption when provisioning connected resources.

Azure Cost Management and Billing is a free service that helps understand Azure bills, manage accounts and subscriptions, monitor and control spending, and optimize resource use. It provides features like reporting, data enrichment, cost and usage budgets, alerts, and recommendations to eliminate idle resources and optimize provisioned resources.

7. Resource Resizing and Shutdown: Azure Cost Management and Billing, as well as Azure Advisor, recommend resizing or shutting down underutilized or idle resources. By resizing virtual machines to a lower size or de-allocating them when not in use, compute costs can be reduced significantly.

8. Gradual Transition to PaaS: As an evolution in cloud adoption, it is recommended to gradually move from Infrastructure as a Service (IaaS) to Platform as a Service (PaaS) services. PaaS services provide ready-made development and deployment environments that are managed for you, potentially reducing costs and eliminating the need for managing underlying infrastructure.

9. Licensing Optimization: Licensing can have a significant impact on cloud spending. Choosing a cost-effective operating system and repurposing licenses for Windows Server or SQL Server on Azure VMs can help reduce licensing costs.

These strategies and best practices can help optimize costs and maximize the value of Microsoft Azure services.

## TCO Calculator

Total Cost of Ownership (TCO) calculator, which helps estimate the cost savings of operating a solution on Azure compared to an on-premises data center. The TCO calculator allows you to enter the details of your on-premises workloads, such as servers, storage costs, IT labor costs, and other assumptions specific to your business. You can review suggested industry average costs and adjust them to match your situation.

The TCO calculator generates a side-by-side report comparing the costs of running workloads on-premises versus on Azure. The report includes cost breakdowns for compute, data center, networking, storage, and IT labor. You can choose a time-frame between one and five years for the report. The report can be downloaded, shared, or saved for later review.
