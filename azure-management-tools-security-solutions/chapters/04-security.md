# General Securiy & Network Security

In this chapter, you'll discover how Azure can assist in safeguarding your workloads, whether they're in the cloud or your on-premises datacenter. Additionally, you'll explore the Azure services available to help maintain a secure, reliable, and trusted network.

## Protect Against Security Threats

In this section you'll learn about how Azure can help you protect the workloads that you run in both the Cloud and in your On-premises data center. You will also learn about the Azure services you can use to help ensure that your network is safe, secure, and trusted.

### Azure Security Center

Azure Security Center is a monitoring service that provides visibility into your security posture across both Azure and on-premises services. It helps predict, prevent, and respond to security threats by monitoring security settings, applying necessary configurations, and offering security recommendations. The service continuously assesses resources for vulnerabilities, uses machine learning to block malware, and employs adaptive application controls. It also detects and analyzes potential attacks, investigates threats, and provides just-in-time access control for network ports. The Secure Score feature measures and reports on an organization's security posture, improving as more security controls are satisfied. Additionally, it includes advanced cloud defense capabilities for virtual machines, network security, and file integrity.

### Azure Sentinel

A SIEM system aggregates security data from various sources that support open standard logging formats and provides threat detection and response capabilities. Azure Sentinel, Microsoft's cloud-based SIEM system, uses intelligent security analytics and threat analysis to collect data at scale from users, devices, applications, and infrastructure across on-premises and multiple clouds. It detects previously undetected threats, minimizes false positives, and investigates threats using AI. Azure Sentinel leverages Microsoft's cybersecurity expertise to respond rapidly to incidents with built-in orchestration and automation. It includes built-in analytics templates for known threats and attack vectors, customizable templates, and machine learning behavioral analytics. Custom analytics rules can be created to search for specific criteria, preview results, schedule queries, and set alert thresholds for suspicious events.

### Azure Key Vault

Azure Key Vault is a centralized cloud service for securely storing application secrets like tokens, passwords, certificates, and API keys. It provides access control and logging capabilities to manage these secrets effectively. Key Vault also helps manage encryption keys and SSL/TLS certificates, making it easier to create, control, and deploy them. Benefits include centralized secret storage, secure storage using industry-standard algorithms, access monitoring, simplified administration, and integration with other Azure services. This integration allows services to securely reference the secrets stored in Key Vault.


### Azure Dedicated Host
 
Azure Dedicated Host offers dedicated physical servers that host your Azure VMs, ensuring isolation from other customers' workloads. This is particularly useful for organizations with regulatory compliance requirements.

It provides visibility and control over the server infrastructure running your Azure VMs. It helps address compliance requirements by deploying workloads on isolated servers. You can choose the number of processors, server capabilities, VM series, and sizes within the same host. After provisioning a dedicated host, Azure assigns it to a physical server in the datacenter. For high availability, you can provision multiple hosts in a host group and deploy your VMs across them.

VMs and dedicated hosts can take advantage of maintenance control, allowing you to control when regular maintenance updates occur within a 35-day rolling window.

You are charged per dedicated host, regardless of the number of VMs deployed on it. The host price is based on the VM family, type, or hardware size and region. Software licensing, storage, and network usage are billed separately.

## Secure Network Connectivity on Azure

In this section, you’ll learn to identify the layers of a defense in depth strategy. You’ll also understand how Azure Firewall helps control network traffic, configure network security groups to filter traffic to and from Azure resources within a virtual network, and explain how Azure DDoS protection safeguards your resources from DDoS attacks.

### Defense in Depth

The goal of defense in depth is to safeguard information and prevent unauthorized access. This strategy employs multiple mechanisms to slow down attacks aimed at gaining unauthorized data access. Each layer offers protection, ensuring that if one layer is compromised, another layer is ready to prevent further breaches. This method avoids dependence on a single protection layer, delays attacks, and provides alerts for security teams to respond to, either automatically or manually.

The physical security layer is the first defense line, protecting data center hardware. The identity and access layer manages access to infrastructure and change control. The perimeter layer uses distributed denial of service (DDoS) protection to filter large-scale attacks before they can disrupt services. The network layer restricts communication between resources through segmentation and access controls. The compute layer secures access to virtual machines. The application layer ensures applications are secure and free from vulnerabilities. The data layer controls access to sensitive business and customer data.

These layers guide security configuration decisions across all application layers. Azure offers security tools and features at every level of the defense in depth concept.

The core principles defining a security posture are confidentiality, integrity, and availability (CIA). Confidentiality follows the principle of least privilege, restricting information access to only those explicitly granted and only to the extent necessary for their work. This includes protecting user passwords, email content, and access levels to applications and infrastructure. Integrity prevents unauthorized changes to information both at rest and in transit, using methods like one-way hashing algorithms to ensure data hasn't been altered. Availability ensures services are operational and accessible only to authorized users, with denial of service attacks aimed at reducing system availability.

### Azure Firewall

A firewall is a network security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules. You can set firewall rules to specify IP address ranges, allowing only clients within those ranges to access the destination server. These rules can also include specific network protocols and port information.

Azure Firewall is a managed, cloud-based network security service designed to protect resources in your Azure virtual networks. A virtual network functions similarly to a traditional network in your data center, serving as a foundational element for your private network. It enables secure communication between virtual machines, the internet, and on-premises networks.

Azure Firewall is a stateful firewall, meaning it analyzes the entire context of a network connection rather than just individual packets. It offers high availability and unlimited cloud scalability. Azure Firewall provides a centralized location to create, enforce, and log application and network connectivity policies across subscriptions and virtual networks. It uses a static public IP address for your virtual and network resources, allowing external firewalls to identify traffic from your virtual network. The service integrates with Azure Monitor for logging and analytics.

Azure Firewall includes features such as built-in high availability, unrestricted cloud scalability, inbound and outbound filtering rules, inbound destination network address translation (DNAT) support, and Azure Monitor logging. Typically, Azure Firewall is deployed on a central virtual network to manage general network access. With Azure Firewall, you can configure application rules that define fully qualified domain names (FQDNs) accessible from a subnet, network rules that specify source address, protocol, destination port, and destination address, and network address translation (NAT) rules that define destination IP addresses and ports for inbound requests.

Additionally, Azure Application Gateway offers a Web Application Firewall (WAF) for centralized inbound protection of your web applications against common exploits and vulnerabilities. Azure Front Door and Azure Content Delivery Network (CDN) also provide WAF services.

### Azure DDoS Protection

DDoS attacks aim to overwhelm and exhaust application resources, making the application slow or unresponsive to legitimate users. These attacks can target any publicly reachable resource, including websites.
Azure DDoS Protection Standard uses Microsoft's global network to bring DDoS mitigation capacity to every Azure region. It analyzes and discards DDoS traffic at the Azure network edge before it can affect your services' availability. It helps provide a defense against DDoS attacks when combined with recommended application design practices.
DDoS Protection Standard ensures that Azure infrastructure itself is not affected during a large-scale DDoS attack, provides additional mitigation capabilities specifically tuned to Azure virtual network resources. It requires no changes to your applications and can be easily enabled and offers always-on traffic monitoring and real-time mitigation of common network-level attacks.

DDoS Protection Standard can help prevent volumetric attacks, protocol attacks, and resource layer or application layer attacks. Volumetric attacks flood the network with a substantial amount of seemingly legitimate traffic. Protocol attacks exploit weaknesses in the Layer three and Layer four protocol stack. Resource layer or application layer attacks target web application packets to disrupt data transmission.

DDoS Protection Standard helps ensure that the network load reflects customer usage, preventing unnecessary resource allocation and expenses. During a DDoS attack, you can receive credit for any costs incurred for scaled-out resources.

### Network Security Groups (NSG)

NSGs act as internal firewalls, allowing you to filter network traffic to and from Azure resources within a virtual network. They contain inbound and outbound security rules that filter traffic based on source and destination IP address, port, and protocol. Azure creates default rules when you create an NSG, but you can overwrite them by creating new rules with higher priorities. NSGs provide an extra layer of defense for protecting internal networks on Azure.