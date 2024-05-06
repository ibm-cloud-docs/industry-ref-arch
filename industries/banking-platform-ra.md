---

copyright:
  years: 2024
lastupdated: "2024-05-06"

keywords:

subcollection: industry-ref-arch

authors:
  - name:
    url:

version: 1.0

deployment-url:

docs: https://cloud.ibm.com/docs/industry-ref-arch

use-case: Banking and finance, Banking customer experience, Banking security, Core banking, Corporate finance, Open banking, Cloud banking

industry: Banking, FinancialSector

content-type: reference-architecture

---

{{site.data.keyword.attribute-definition-list}}

# Banking
{: #banking-platform}
{: toc-content-type="reference-architecture"}
{: toc-industry="Banking"}
{: toc-use-case="Banking and finance"}
{: toc-version="1.0"}

The IBM Cloud framework for Financial Services provides multiple reference architectures that can be used as a basis for meeting the security and regulatory requirements that are defined in the framework. They implement these main guidance principles:

### Defense in depth
Cloud infrastructure provides multiple redundant layers of security safeguards to prevent the compromise of a service from a single point of attack.

### Restricted privileged rights
No individual should be given enough privileges to misuse a system on their own. Give people the minimum required authorizations to complete their activities.

### Safeguard data
Data is a valuable asset that needs to be protected from unauthorized disclosure, modification, and destruction.

### Continuous controls assurance
Security controls must be configured securely by default through automation and checked continuously for compliance to provide continued controls assurance.

### Detection and response
Enable traceability through the logging, monitoring, alerting, and collection of audit information in real time.

### Service resilience
The availability of services and data are critical to the operation of business applications. They incorporate multiple levels of resilience to maintain cloud services even after multiple component failures.

### Secure by design and software integrity
Follow secure development and operations processes and ensure software integrity through automation.


## Banking platform architecture
{: #architecture-diagram}


IBM Cloud for Financial Services provides multiple reference architectures that enable and support the security and compliance requirements for different types of environments:

* IBM Cloud® Virtual Private Cloud, with options for using one or both of Virtual Servers for VPC and Red Hat® OpenShift®
* IBM Cloud for VMware® Regulated Workloads
* IBM Cloud Satellite

Here is the VSI on VPC reference architecture. For more information, please refer to [IBM Cloud for Financial Services](https://cloud.ibm.com/docs/framework-financial-services?topic=framework-financial-services-reference-architecture-overview) documentation.


![Banking platform reference architecture - VSI on VPC](../images/banking-vpc-high-level-v3-with-edge.svg "Banking platform reference architecture - VSI on VPC"){: caption="Figure 1. Banking platform reference architecture - VSI on VPC" caption-side="bottom"}


## Nonfunctional requirements

A banking industry architecture has several nonfunctional requirements.

### Security
All application systems must implement robust controls over their communication network for these purposes:

* Safeguarding data
* Tightly controlling access to network devices through management approval and subsequent audits
* Disabling remote communications when no business need exists
* Logging and monitoring remote access
* Securing remote access devices
* Using strong authentication and encryption to secure communications

All confidential bank data must be encrypted while in transit on any network or stored on any device on premises, or on a private or public cloud. Confidential bank information, including authentication credentials, must be encrypted while in transit over any public network or wireless network. Key management procedures must be employed that assure the confidentiality, integrity, and availability of cryptographic key material. The use of encryption products must comply with local restrictions and regulations in the relevant country.

### Scalability
The architecture must be able to support large-scale deployments. The largest banks in the world support more than 300 million customers, over a billion transactions per day, and manage assets of more than USD 4 trillion. The architecture must not only meet the current requirements but also anticipate the future needs of a dynamic, growth-focused institution. The infrastructure must boost the business, not limit it. It must provide a demonstrated ability to scale and align to the business objectives as the financial institution grows.

### Availability
Financial institutions need to operate in a 24 x 7 environment. The infrastructure must be available to the customers whenever they want, wherever they are, and on whatever channel they prefer to interact. Mission-critical applications such as payment processing and other core banking transaction processing might require 99.999% availability.

### Performance and response times
Some of the application components in the banking industry need a high throughput, low-latency, real-time performance. Examples include card authorizations and transactions, payment transactions, fraud detection, and securities processing.

### Business continuity and disaster recovery
Application systems must have formal documented recovery plans and tools to identify the resources and specify actions that are required to minimize losses if a disruption occurs to the business unit, its supporting group units, applications, or infrastructure components. Business continuity and disaster recovery (DR) plans ensure timely and orderly recovery of the business, support processes, operations, and technology components within an agreed-upon timeframe. These plans include the orderly restoration of business activities when the primary work environment is unavailable.

### Backup and offsite storage
All application systems must have a defined backup policy and associated procedures for backing up data in a scheduled and timely manner. Effective controls must be established to safeguard backed-up data onsite and offsite. They must also ensure that the bank data is securely transferred or transported to and from backup locations and conduct periodic tests to ensure that data can be safely recovered from backup devices.
