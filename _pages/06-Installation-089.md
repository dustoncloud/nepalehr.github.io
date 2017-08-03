---
title: "Bahmni 0.89 Installation"
permalink: /install-bahmni-089/
layout: single
excerpt: "Instructions for installation of Bahmni 0.89"
last_modified_at: 2017-06-05T10:01:43-04:00
---

**Note:** The instructions are for a fresh installation of Bahmni 0.89 on a single server
{: .notice--warning}

## Installation steps
1. Ensure the server is  running CentOS 6.7 6.8 or 6.9. (Make sure to  have more than 200 GB in / partition)
2. For offline installation, enable ```yum cache``` so the downloaded packages can be used when offline. However, note that you will need to be online for packages to download in the first place - but downloaded packages will be used in any subsequent installation. Refer to [this link](https://bahmni.atlassian.net/wiki/display/BAH/Bahmni+Installation+Without+Internet) for detailed instructions.
3. Follow the steps detailed in this [link](https://bahmni.atlassian.net/wiki/pages/viewpage.action?pageId=35291242) to install the default Bahmni package (see following bullet points for additional instructions to follow before triggering installation) 
  - Git clone ```setup.yml``` to ```/etc/bahmni-installer/```
  - Git clone database dump files provided in the NepalEHR database repositories in the deployment-artifacts folder to ensure these databases are restored by the installer
  - Git clone NepalEHR_config files to deployment-artifacts to ensure these configurations are used by the installer
  - Git clone NepalEHR inventory file ```local``` to ```/etc/bahmni-installer/```. References to "localhost" can be replaced with an IP, and any bahmni-subsystems that are not required can be commented out.
4. Check whether all the applications are up and running (MRS, ELIS, ERP, PACS, Reports)
```bash
sudo service openmrs status
sudo service bahmni-lab status
sudo service bahmni-reports status
sudo service bahmni-erp-connect status
sudo service pacs-integration status
```
5. Check if the sync between applications are working fine.
6. Make sure the markers tables has the right IP address mentioned in the entries.
7. Check for sanity on all applications
8. Make sure the custom erp module for NepalEHR is added in OpenERP. Also make sure the "assets" module is setup properly
9. Conduct UAT
