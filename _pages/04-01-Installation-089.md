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
1. Ensure the serveris  running CentOS 6.7
2. For offline installation, enable yum cache so the downloaded packages can be used when offline. However, note that you will need to be online for packages to download in the first place - but downloaded packages will be used in any subsequent installation.
```
Refer to https://bahmni.atlassian.net/wiki/display/BAH/Bahmni+Installation+Without+Internet)
```
3. Follow the steps in the provided link to install the default Bahmni package (see 3.1 to 3.4 for additional instructions to follow before triggering installation)
```
https://bahmni.atlassian.net/wiki/pages/viewpage.action?pageId=35291242
```
3.1 When setting up installation variables, use the following for setup.yml
```bash
timezone: Asia/Kathmandu
implementation_name: nepalEHR
selinux_state: disabled
```
3.2 Git clone database dump files provided in the NepalEHR database repositories in the deployment-artifacts folder to ensure these databases are restored by the installer
3.3 Git clone NepalEHR_config files to deployment-artifacts to ensure these configurations are used by the installer
3.4 Git clone NepalEHR inventory file ("local") to /etc/bahmni-installer. "localhost" can be replaced with an IP, and any bahmni-subsystems that are not required can be commented out.
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