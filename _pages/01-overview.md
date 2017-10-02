---
title: "Overview"
permalink: /overview/
layout: single
excerpt: "Overview of NepalEHR."
last_modified_at: 2017-10-02T10:01:43-04:00
---

_NepalEHR_ is an implementation of [Bahmni](http://bahmni.org) open source electronic health record system and [Commcare](https://commcarehq.org) mobile platform that allows for digital storage, secure access, and maintenance of individual patient’s medical records - simple enough to be used by mid-level practitioners and community health workers but complex enough to meet demanding population health needs. The integrated system includes a supply chain management component critical for an efficient healthcare system.

{% include toc %}

_NepalEHR_ is currently implemented at two public health facilities in Nepal:
* Bayalpata Hospital, Achham: Since February 2015
* Charikot PHC, Dolakha: Since February 2016

### About Bahmni
Bahmni is an easy to use, complete, open source Hospital Information System (HIS) and Electronic Medical Record (EMR) under development since November 2012. Bahmni aims to meet the needs of hospitals in low resource environments by leveraging a tapestry of existing open source products. The information that Bahmni makes accessible helps healthcare providers to improve efficiency and quality of patient care, reduce errors in clinical encounters and advocate for issues related to public health.

* An Integrated Solution - Manage patient information across registration, point of care, investigations, and billing
* Intuitively Designed - Simple to use at the point of care, with minimal training required
* Flexible - Allows for unique workflows and processes based on each hospital's needs
* Modular - Choose parts of Bahmni and integrate with existing systems 
* Infrastructure Appropriate - Hosted and operated at the hospital site, requiring no dependence on Internet
* Adaptable - Bahmni can be used on a variety of devices including tablets and laptops

**For more about Bahmni**, see [Bahmni Wiki](https://bahmni.atlassian.net/wiki/display/BAH/Bahmni+Home)
{: .notice--info}

### Underlying platforms
* [OpenMRS](http://openmrs.org/): Open source medical records system
* [OpenELIS](http://openelis.org/): Open source lab information system
* [OpenERP/Odoo](http://odoo.com): Open source inventory and resources management tool
* [DCM4Che](/http://www.dcm4che.org/): Open source clinical image and object management
* [Commcare](/http://www.commcarehq.org/): Mobile data collection platform

## NepalEHR Implementation
_NepalEHR_ is an implementation of [Bahmni](http://bahmni.org) and [Commcare](https://commcarehq.org) that as been configured for Nepal's public healthcare system. It builds upon Bahmni, with configuration to include Nepal's HMIS (http://dohs.gov.np/information-systems/health-management-information-section/) forms for data entry, and HMIS reports generation. Work is ongoing to integrate the system with Nepal Ministry of Health's DHIS2.

***Included in the package***
* Bahmni 0.89
* NepalEHR default database
* NepalEHR configuration files
* NepalEHR additional features
{: .notice--info}

### Features of the integrated system
* Patient registration (OpenMRS)
* Patient medical records (OpenMRS)
* Lab orders and results (OpenMRS <> OpenELIS)
* Prescription and dispensing (OpenMRS <> OpenERP)
* Inpatient bed management (OpenMRS)
* Supply chain management (OpenERP)
* Radiology orders and DICOM image viewing (DCM4Che <> OpenMRS)
* HMIS reporting (OpenMRS)
* Mobile data collection with assisted decision making (Commcare)
