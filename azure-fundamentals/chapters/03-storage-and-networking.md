# Azure Storage Services

Azure Storage is a versatile service for storing various types of data, including files, messages, tables, and more. It supports data access and storage for clients like websites, mobile apps, desktop applications, and custom solutions. Additionally, Azure Storage is utilized by Infrastructure as a Service (IaaS).

To start using Azure Storage, you need to create an Azure Storage account, which can be done via the Azure portal, PowerShell, or the Azure CLI. It's important to note that Azure Storage is distinct from Azure Database Services. Your storage account will house all your Azure Storage data objects, such as blobs, files, and disks. For Azure VMs, Azure Disk Storage is used to store virtual disks, but it cannot store disks outside of a virtual machine.

A storage account provides a unique namespace for your Azure storage data, accessible globally over HTTP or HTTPS. The data is secure, highly available, durable, and massively scalable. Azure offers several access tiers to balance storage costs with access needs:

- **Hot Access Tier**: Optimized for frequently accessed data, like website images.
- **Cool Access Tier**: Suitable for infrequently accessed data stored for at least 30 days, such as customer invoices.
- **Archive Access Tier**: Ideal for rarely accessed data stored for at least 180 days, like long-term backups.

Only the hot and cool tiers can be set at the account level, while the archive tier is set at the blob level during or after upload. Cool tier data can tolerate slightly lower availability but still requires high durability and similar retrieval latency and throughput to hot data. Archive storage offers the lowest storage costs but the highest costs to rehydrate and access data.

**Azure Blob Storage** is an object storage solution for the cloud, capable of storing vast amounts of unstructured data, such as text or binary data. It supports thousands of simultaneous uploads, large volumes of video data, and growing log files, accessible from anywhere with an internet connection. Blobs can contain diverse data types, from binary data streamed from scientific instruments to encrypted messages for other applications.

**Disk storage** provides persistent storage for Azure Virtual Machines, accessible similarly to on-premises scenarios. Disks come in various sizes and performance levels, from SSDs to traditional HDDs, with different performance tiers. Standard SSD and HDD disks are suitable for less critical workloads, while premium SSD disks are for mission-critical applications, and ultra disks are for data-intensive workloads like SAP HANA and top-tier databases.


# Azure Networking Services

Azure Virtual Networks allow Azure resources like VMs, web apps, and databases to communicate with each other, users on the Internet, and on-premises client computers. Think of an Azure network as a collection of resources that connect other Azure resources. Key networking capabilities of Azure Virtual Networks include isolation and segmentation, internet communications, communication between Azure resources, communication with on-premises resources, routing network traffic, filtering network traffic, and connecting virtual networks.

With Virtual Network, you can create multiple isolated virtual networks. When setting up a virtual network, you define a private IP address space using either public or private IP address ranges. This space can be divided into subnets, allocating parts of the address space to each subnet. For name resolution, you can use Azure's built-in service or configure the network to use an internal or external DNS server. By default, VMs in Azure can connect to the Internet, and you can enable incoming connections by defining a public IP address or a public load balancer.

Azure Virtual Networks also enable you to link resources in your on-premises environment with those in your Azure subscription, creating a network that spans both local and cloud environments. There are three ways to achieve this connectivity:

1. **Point-to-Site VPN**: Similar to a VPN connection from a computer outside your organization to your corporate network, but in reverse. The client computer initiates an encrypted VPN connection to Azure.
2. **Site-to-Site VPN**: Links your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network, making Azure devices appear as part of the local network. The connection is encrypted and works over the Internet.
3. **Azure ExpressRoute**: Provides dedicated private connectivity to Azure, bypassing the Internet, ideal for environments needing higher bandwidth and security.

A Network Security Group (NSG) is an Azure resource containing multiple inbound and outbound security rules. These rules can be defined to allow or block traffic based on factors like source and destination IP addresses. You can also link virtual networks using virtual network peering, enabling resources in each network to communicate with each other, even if they are in different regions, creating a global interconnected network through Azure.

