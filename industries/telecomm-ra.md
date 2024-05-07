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

use-case: Telecommunications, Telecommunications infrastructure

industry: Telecommunications

content-type: reference-architecture

---

{{site.data.keyword.attribute-definition-list}}

# Telecommunications
{: #telecommunications}
{: toc-content-type="reference-architecture"}
{: toc-industry="Telecommunications"}
{: toc-use-case="Telecommunications, Telecommunications infrastructure"}
{: toc-version="1.0"}


If edge computing brings computation and data storage as close to the point where data is created and actions are taken, edge networking provides the two key features of low latency and high bandwidth to deliver the data and applications where required.

While the goal of edge computing is to move computation away from the cloud and data centers toward the edge of the network, the focus of edge networking is on network-specific components. Moving services closer to network edge locations makes content caching, storage, device management, and service delivery easier and contributes to improved transfer rates and response times.

Network in this context refers to what communications service providers (CSPs) offer and control. The network forms the backbone of all the different types of services that CSPs offer, such as voice, data, and video. Automation for the operation of services and the underlying resources that are required to test them before deployment are key to the service providers and network operators. The ability to virtualize functions and use virtualized resources is a major shift in paradigm for the CSP industry.

The network edge platform architecture contains three layers: hardware resources, virtualization layer, and virtualized functions.


## Architecture diagram
{: #architecture-diagram}


![Telecommunications reference architecture](../images/network-automation-ref-diagram.svg "Telecommunications reference architecture"){: caption="Figure 1. Telecommunications reference architecture" caption-side="bottom"}

The major components in a network automation architecture are the hardware resources, virtualization layer, management and orchestration, OSS/BSS, and applications. Multi-access edge computing (MEC) enables the implementation of MEC applications as software-only entities that run on top of a virtualization infrastructure, which is located in or close to the network edge.

MEC and Network Functions Virtualization (NFV) are complementary concepts. The MEC architecture is designed in such a way that a number of different deployment options of MEC systems are possible.


## Nonfunctional requirements
{: #nonfunctional-requirements}

Network automation architectures must satisfy several nonfunctional requirements.

* Scalability

The combination of NFV and edge computing brings about scalability and low latency. NFV delivers scalability for networking computing, scaling the network’s resources up or down depending on need, and application usage. Edge computing offers low latency. The latency time from transmitting data to the data center and back to the user equipment (UE) is shortened because the edge is closer to the user, creating a faster computing experience.

* Reliability

Network slicing is possible through NFV. Different partitions (or slices) can be targeted for specific network functions. This practice ensures that high-bandwidth applications receive the networking capabilities they need without hindering the computing functions for other applications that use the same network. This also minimizes the chances for network problems. Edge computing gives network slicing an additional boost in throughput by ensuring consistent services and connectivity for high-bandwidth applications and products.

* Security

Security is a major issue with NFV. You must be aware of the numerous attack points. Only then can a secure solution be architected. A secure NFV environment can be ensured by using a vendor-certified hardware layer and by enabling these capabilities:

  - Trust in the hypervisor layer
  - Access control in the MANO layer
  - Network segmentation
  - Traffic filtering and perimeter security in the network layer
  - Continuous scanning and monitoring
  - Proper Identity and Access Management (IAM) and certificate management at the VNF/application layer
