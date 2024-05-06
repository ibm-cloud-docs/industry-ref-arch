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
{: #banking-app}
{: toc-content-type="reference-architecture"}
{: toc-industry="Banking, FinancialSector"}
{: toc-use-case="Banking and finance, Banking customer experience, Banking security, Core banking, Corporate finance, Open banking, Cloud banking"}
{: toc-version="1.0"}

The Banking industry reference architecture uses methods and industry-standard models to drive toward greater IT and business alignment.

Financial institutions can follow a consultative method to identify opportunities for improvement and innovation by using the Banking Industry Architecture Network (BIAN), IBM Information Framework (IFW), and IBM Component Business Models (CBM) for Financial Services. These assets provide industry-specific frameworks and can be used for creating an overall banking modernization program.

To address the key business imperatives and to realize the expected business value, an enterprise can adapt a standardized business architecture as defined by BIAN.org. BIAN defines a canonical business architecture as a functional decomposition of the banking landscape, which is composed of atomic building blocks that are called Service Domains: a “periodic table for banking”. For an identified project in the overall modernization program, BIAN provides high-level descriptions of business capabilities.

While BIAN provides a semantic layer, implementation planning considerations are largely left for the financial institution to define. Implementation planning is where IBM Business Process and Services Models and Data Warehouse Models (IFW Models) come into play. IFW models provide a detailed fine-grain level-4 and 5 processes, service definitions, message modes, and data models to drive an implementation. You can create scoped low-level design models and implementation details for each of the BIAN service domains that are included in project scope.

IBM’s banking solution reference architectures combine these components with a Domain-Driven Design method to deliver a true microservices architecture that allows the bank to integrate modern technologies more easily into their environment. The architecture is a pattern that consists of defining and implementing small, specialized, and self-contained application components that interact with each other through APIs and messages, providing a network of loosely coupled components.

The Banking industry reference architecture includes a zero-trust approach that aims to wrap security around every user, every device, and every connection, every time. A zero-trust approach provides advanced protection from cyberthreats.

Zero-trust technologies help to discover and classify all assets in the cloud so that your organization can establish the right protections and access controls. By centralizing visibility and policy management, compliance efforts can be maximized while monitoring and reporting are improved.

## Banking application architecture
{: #architecture-diagram}

The IBM Banking industry reference architecture is built over several technical domains. The heart of the architecture has three major domains.

#### Digital agility services
The digital agility services layer provides a microservices platform such as Financial Services Workbench, which is used to create container and containerized components running on secured cloud infrastructure. New application components are designed and developed in this platform by using the Domain-Driven Design method and by using BIAN and IFW models. These loosely coupled components interact with each other, external systems, or both through exposed APIs and messaging by using an API gateway and an enterprise event bus. Some examples of application components in this layer include party data management, customer offer, and loan agreement.

#### Business automation
The business automation layer provides a proven set of methods and tools that deliver on a value proposition to support the business process reengineering and transformation. Data and AI capabilities are used to collect, prepare, and govern data and to analyze and infuse insights in applications, processes, and business microservices. These capabilities are used for process automation, process mining and modeling, robotic process automation, content services, document processing, decision management, workflow orchestration, and task management.

#### Analytical insights
The analytics insights domain helps financial institutions transform to a cognitive enterprise by gaining the most value from the data in a cost-effective way, irrespective of data origin and data store. Insight services play a key role in delivering differentiated digital experiences to users, achieving higher growth through better insights and predictability. This domain provides capabilities that include an AI and machine learning platform, operational and main data stores, data warehouse and data lake, multicloud data access, integration and data virtualization, intelligent knowledge catalog, and data governance and lineage.

### Supporting domains
Several supporting domains integrate into the architecture domains.

#### Integration fabric
The integration platform provides an automated, closed-loop approach that supports multiple styles of integration within a single, unified experience. This layer provides banks with end-to-end enterprise-grade security and encryption and many other capabilities:

* Unlock business data and assets as APIs
* Connect cloud and on-premises applications
* Reliably move data with enterprise messaging
* Deliver real-time event interactions
* Transfer data across any cloud
* Deploy and scale with cloud-native architecture and shared foundational services

#### Core systems and systems of record
This layer hosts the core product processing and operational support systems such as general ledger, payment processing, and customer master. In large banks, these applications are high-volume, mission-critical applications and often run on mainframe computers. While mainframe computing provides high availability, low latency, and high performance, banks are moving middle tier subsystems and processes to distributed and cloud environments to achieve better flexibility and deployment options.

#### External data providers and ecosystem partners
Banking systems often require data from external data sources such as credit bureaus, regulatory bodies such as FinCEN and OFAC, third-party data aggregators such as Lexis-Nexis and Factiva, and public databases such as CFPB and Law Enforcement. Often, banking systems also connect with ecosystem partners such as payment gateways (SWIFT and ACH), correspondence banks, merchant and card networks, and financial technology (fintech) companies (online payments and crypto). This layer provides and manages secured connectivity to these external data providers and other ecosystem partners.

#### Traditional and new banking channels
This domain enables applications that allow customers to interact with the bank through multiple channels such as online banking, mobile applications, brick and mortar branches, e-branches, ATMs, and virtual agents. With the rise of fintechs, a customer can interact with a bank through several new channels. For example, a bank customer can ask about current loan interest rates on Zillow. This domain addresses the specific needs of omnichannel applications, including channel APIs, authentication and authorization, personalization, seamless and integrated cross-channel experience, and customer-centric processes.

#### Secured, compliant cloud infrastructure
This layer provides cloud infrastructure that is designed to build trust and enable a transparent public cloud ecosystem with the specific features for security, compliance, and resiliency that financial institutions require. It enables delivery against regulatory imperatives through a consistent set of embedded controls that are designed to meet the needs of financial institutions’ control stakeholders. Those stakeholders include Chief Risk Officers (CROs), Chief Compliance Officers (CCOs), Chief Information Security Officers (CISOs), and Chief Privacy Officers (CPOs).

![Banking application reference architecture](../images/banking-app-ref-architecture.svg "Banking application reference architecture"){: caption="Figure 1. Banking application reference architecture" caption-side="bottom"}


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
