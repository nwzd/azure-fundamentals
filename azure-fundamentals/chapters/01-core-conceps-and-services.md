# Cloud Concepts

## Benefits of Cloud

Cloud-based applications utilize a variety of strategies to enhance their functionality and reliability:

- **High Availability**: Depending on your chosen service level agreement, cloud-based applications can ensure a seamless user experience with minimal downtime, even during issues.
- **Scalability**: Cloud applications can scale vertically by adding more RAM or CPUs to a virtual machine, or horizontally by adding more instances, such as additional virtual machines.
- **Elasticity**: These applications can automatically scale resources up or down as needed, ensuring they always have the necessary resources.
- **Agility**: Cloud resources can be quickly deployed and configured to meet changing application requirements.
- **Geo-distribution**: Applications and data can be distributed across regional data centers globally, providing optimal performance for users in different locations.
- **Disaster Recovery**: Utilizing cloud-based backup services, data replication, and geo-distribution, applications can be deployed with confidence that data is secure in case of a disaster.

Cloud service providers operate on a consumption-based model, meaning users only pay for the resources they use. This model offers several benefits, such as no upfront costs, no need to manage underutilized infrastructure, and the flexibility to pay for additional resources as needed or stop paying for unused resources. When evaluating cloud computing benefits, consider two types of expenses: capital expenditure (CapEx) and operational expenditure (OpEx). CapEx involves upfront spending on physical infrastructure, which depreciates over time, while OpEx involves spending on services as they are used. Cloud services fall under OpEx due to their consumption-based nature, contrasting with the significant upfront costs and ongoing maintenance associated with CapEx.

## Cloud Service Models

If you're familiar with cloud computing, you've likely encountered the terms Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS). These models represent different levels of shared responsibility between the cloud provider and the cloud tenant.

- **IaaS**: This is the most flexible cloud service model, offering complete control over the hardware running your applications. Instead of purchasing hardware, you rent it.
- **PaaS**: While providing the same benefits as IaaS, PaaS also offers additional advantages, such as managing the underlying infrastructure.
- **SaaS**: This model involves software that is centrally hosted and managed for users. Typically, a single version of the application is used by all customers and is licensed through a subscription, either monthly or annually. SaaS also includes the benefits of IaaS, with added features.

As you move from IaaS to PaaS to SaaS, the client's responsibilities decrease while the provider's responsibilities increase. This progression illustrates the varying levels of responsibility between the cloud provider and the tenant, with more responsibilities shifting to the provider as you move from on-premises solutions to IaaS, PaaS, and finally SaaS.

## Cloud Computing Models

Cloud computing can be deployed using three main models: public cloud, private cloud, and hybrid cloud. Each model has unique characteristics to consider when migrating to the cloud.

- **Public Cloud**: Services are provided over the public internet and are available to anyone who wants to purchase them. The cloud resources, such as servers and storage, are owned and managed by a third-party provider and delivered via the internet.
- **Private Cloud**: This model uses computing resources exclusively for one business or organization. A private cloud can be located on-site at the organization's data center or hosted by a third-party provider.
- **Hybrid Cloud**: This model combines public and private clouds, allowing data and applications to be shared between them. This setup offers flexibility and optimization of existing infrastructure, reducing costs and administrative requirements as resources move from on-premises to off-premises.

## Azure subscriptions, management groups, resources, and regions

To use Azure, you need an Azure subscription, which grants authenticated and authorized access to Azure services and allows resource provisioning. An Azure subscription is linked to an Azure account, which is an identity in Azure Active Directory (Azure AD) or a trusted directory.

There are two types of subscription boundaries:

1. **Billing Boundary**: Determines how an Azure account is billed. You can create multiple subscriptions for different billing needs, with separate billing reports and invoices for each.
2. **Access Control Boundary**: Manages access policies at the subscription level. You can create separate subscriptions to reflect different organizational structures, allowing distinct access controls for different departments.

Creating additional subscriptions can help manage resources and billing, such as separating environments for development and testing or isolating data for compliance. Subscriptions also help manage costs and resource limits, like the maximum number of Azure ExpressRoute circuits per subscription.

For efficient management, Azure allows organizing subscriptions into management groups, which provide a higher level of scope. Governance conditions applied to a management group are inherited by all subscriptions within it, facilitating access policy and compliance management.

Azure resources are manageable items like virtual machines, storage accounts, web apps, and databases. These resources are organized into resource groups, which are containers that hold related resources for an Azure solution. Resource groups help manage and organize resources by usage, type, or location. Each resource must belong to a single resource group, and while many resources can be moved between groups, some have specific limitations.

**Azure Resource Manager (ARM)** is the service that manages and deploys Azure resources. It provides a management layer for creating, updating, and deleting resources. ARM ensures consistent results across different tools by handling all requests through the same API. It also allows for the use of management features like access control, locks, and tags to secure and organize resources.

ARM offers several benefits, including the ability to manage infrastructure through declarative templates, deploy and monitor resources as a group, and apply access control and tags for better organization and billing clarity. This approach simplifies resource management and ensures consistent deployment throughout the development lifecycle.

## Azure Regions and Availability Zones

Azure resources are created in various regions, which are distinct geographical areas around the world that house Azure data centers. When you use a service or create a resource like a SQL database or Virtual Machine, you're utilizing physical equipment in one or more of these locations. Users don't interact directly with specific data centers; instead, Azure organizes them into regions.

A region is a geographical area that contains at least one, but often multiple, data centers connected by a low-latency network. Azure manages and balances resources within each region to ensure optimal performance. When deploying resources in Azure, you typically need to choose the region for deployment. Some services or VM features are only available in certain regions, such as specific VM sizes or storage types. However, some global Azure services, like Azure Active Directory, Azure Traffic Manager, and Azure DNS, don't require a specific region selection. Global regions enhance scalability and redundancy while maintaining data residency.

Examples of regions include West US, Canada Central, West Europe, Australia East, and Japan West.

Azure also has specialized regions for compliance or legal purposes, such as US Department of Defense Central, US Government Virginia, and US Government Iowa. These regions are isolated instances of Azure for US government agencies and partners, operated by screened US personnel with additional compliance certifications. In China, regions like China East and China North are available through a partnership with 21Vianet, where Microsoft doesn't directly manage the data centers.

Regions are used to identify the location for your resources. Additionally, there are geographies and Availability Zones. Availability Zones are physically separate data centers within an Azure region, each with independent power, cooling, and networking. They are designed to be isolation boundaries, so if one zone goes down, the others continue to function. Availability Zones are connected through high-speed private fiber optic networks.

Not all regions support Availability Zones. For an updated list, refer to Azure documentation. Availability Zones can be used to run mission-critical applications and build high availability into your architecture by co-locating resources within a zone and replicating them in other zones. Note that there may be costs associated with duplicating services and transferring data between zones.

Azure services that support Availability Zones fall into two categories: zonal services, where resources are pinned to a specific zone (e.g., VMs, managed disks, IP addresses), and zone-redundant services, where the platform automatically replicates across zones (e.g., zone-redundant storage, SQL databases).
