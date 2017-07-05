---
title: "System requirements"
permalink: /system-requirements/
layout: single
excerpt: "Why the need for an EHR in Nepal?"
last_modified_at: 2017-06-05T10:01:43-04:00
---

***Note:*** This recommendation is for production environment setup.
{: .notice--info}

### Server specification
The following server configuration is recommended for running complete Bahmni with all sub-systems, i.e. OpenMRS, OpenERP and OpenELIS.
* CPU - Quad core (8 core, if in future you would want to run PACS integration from the same server)
* Memory - 8 GB (16 GB, if in future you would want to run PACS integration from the same server)
* Hard disk - 500GB  (doesn't include the disk space needed for PACS integration or if you plan to upload a lot of files/images)

### Setup
Three servers are recommended in a production environment:
* Active server
* Passive server with replication, can be made active in case of Active server failure
* Pre-production server to test changes

A blue-green setup is recommended for new releases to minimize downtime. The pre-production server is updated, tested and can be made the active server when ready.