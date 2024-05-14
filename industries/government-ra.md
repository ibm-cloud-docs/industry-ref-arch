---

copyright:
  years: 2024
lastupdated: "2024-05-13"

keywords:

subcollection: industry-ref-arch

version: 1.0

deployment-url:

use-case: GovernmentIndustry

industry: Government

content-type: reference-architecture

---

{{site.data.keyword.attribute-definition-list}}

# IBM Cloud Satellite for Government
{: #government}
{: toc-content-type="reference-architecture"}
{: toc-industry="Government"}
{: toc-use-case="GovernmentIndustry"}
{: toc-version="1.0"}

This architecture demonstrates the best practices with IBM Cloud Satellite deployments in the government space.
{: shortdesc}

## Architecture diagram
{: #architecture-diagram}

![High-Level Diagram.](../images/government-satellite.png "Automotive High-Level Diagram"){: caption="Figure 1. Best Practice Architecture for Regulated Government Applications in IBBM Cloud Satellite" caption-side="bottom"}

The overall architecture consists of a three tier application (presentation, application, database) deployed in a IBM Cloud Red Hat Openshift cluster in a Satellite location within a regulated on-prem datacenter. In this design: the presentation tier has a basic webpage that displays content fetched from an API in the application tier. The application tier connects to the database tier to determine the content to display.
