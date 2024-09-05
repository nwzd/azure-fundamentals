# Azure Identity Services
This chapter explains how Azure Active Directory helps you manage and secure identities. You will also see how to use single sign-on, multifactor authentication, and Conditional Access to enable your users to securely access resources and applications from your intranet and from public networks.


## Authentication & Authorization

Authentication: This is the process of establishing the identity of a person or service that wants to access a resource. It involves a challenge-response mechanism where the user or service provides credentials to prove their identity. These credentials are used to create a security principle, which is then used to establish the user's identity and access control.

Authorization: Once a user or service has been authenticated, authorization comes into play. Authorization determines the level of access that an authenticated person or service has. It specifies what data they are allowed to access and what actions they can perform. It is similar to a doorman allowing access to specific rooms based on the information on an identity card.

Authentication and authorization occur sequentially in the identity and access process. Authentication establishes the user's identity, while authorization defines what they are allowed to do.

Authentication proves who you are, while authorization defines what you are allowed to do. 

## Azure Active Directory

Azure AD allows employees to securely sign in and access both internal and external resources. This includes external resources like Microsoft 365, the Azure portal, and various SaaS applications, as well as internal resources such as corporate network apps, intranet, and any cloud apps developed by the organization.

While related, Active Directory and Azure AD have key differences. Introduced in Windows 2000, Active Directory helps manage on-premises infrastructure with a single identity per user. It provides an Identity and Access Management Service managed by the organization itself.

Azure AD, on the other hand, is a cloud-based Identity and Access Management Service. You control the identity accounts, while Microsoft ensures global availability. Unlike on-premises Active Directory, Azure AD can detect suspicious sign-in attempts when connected.

Azure AD is used by various end-users. IT administrators can control access to applications and resources based on business needs. App developers can add functionalities like single sign-on to their apps. End users can manage their identities.

Azure AD offers services such as authentication, self-service password reset, multi-factor authentication, banned password lists, and smart lockouts. Single sign-on (SSO) allows users to access multiple applications with one username and password. This simplifies security, as access changes are tied to a single identity.

You can manage both cloud and on-premises apps using Azure AD. Features like application proxy, SaaS apps, the My Apps portal (Access Panel), and SSO enhance user experience. Azure AD also supports device registration, enabling management through tools like Microsoft Intune and device-based conditional access policies.

Connecting Active Directory with Azure AD provides a consistent identity experience. Azure AD Connect is a popular method for synchronizing user identities and changes between on-premises Active Directory and Azure AD, allowing the use of features like SSO, multi-factor authentication, and self-service password reset. This helps prevent the use of compromised passwords.

## Single Sign-On (SSO) & Multifactor Authentication (MFA) &Conditional Access


Single Sign-On (SSO):
-  SSO allows users to sign in once and use that credential to access multiple resources and applications from different providers.
-  It simplifies the security model by granting access across applications to a single identity tied to the user.
-  Managing multiple identities and passwords can be challenging and increases the risk of security incidents.
-  SSO reduces the effort needed to change or disable accounts when users change roles or leave an organization.

Multi-Factor Authentication (MFA):
- MFA is a process that requires users to provide an additional form of identification during the sign-in process.
- It provides an additional level of security by requiring two or more elements to fully authenticate.
- These elements can include something the user knows (e.g., password), something the user has (e.g., code sent to their phone), or something the user is (e.g., biometric property like fingerprint or face scan).
- Azure AD MFA is a Microsoft service that provides multi-factor authentication capabilities.
- It offers various authentication methods such as phone call, mobile app notification, or SMS code.

Conditional Access:
- Conditional Access is a tool in Azure Active Directory that allows or denies access to resources based on identity signals.
- It considers factors like user identity, location, and device to make access decisions.
- It provides a more granular multi-factor authentication experience by challenging users for a second authentication factor based on specific conditions.
- Conditional Access helps IT administrators empower users to be productive while protecting the organization's assets.


