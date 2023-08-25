## Files
* README.md - This file
* ansible_hosts - Ansible inventory
* linux_agent.yml - Linux/RPM
* linux_setting.yml - Ansible variables file for Linux/RPM
* win_setting.yml - Ansible variable file for Windows
* win_agent.yml - WinRM/MSI 

## linux_setting.yml
* appliance_ip: IP address of appliance
* appliance_url_user: admin
* appliance_url_password: Some_Password
* download_rpm_pkg: Full RPM package name such as bushido-agent-ng-2-334-16-GA.x86_64.rpm
* agent_domain: Agent domain name such as BUSHIDO-GENERAL
* agent_domain_desc: Agent domain name description such as "Bushido Agent Group"
* agent_version: Agent version such as 2-334-16
* os: It is set to Redhat for RHEL and derivatives
* rpm_pkg: Don't change. 

## win_setting.yml:
* ansible_user: Windows login (Administrator)
* ansible_password: Windows password
* ansible_winrm_transport: basic
* ansible_winrm_scheme: http
* ansible_port: 5985
* ansible_connection: winrm
* appliance_ip: Appliance IP to download Agent from
* url_user: Fortress UI Username
* url_password: Fotress UI password
* msi_pkg: MSI package name
* agent_version: Bushido Agent version
* os: Windows

## Example:
* Linux: ansible-playbook linux_agent.yml -i ansible_hosts
* Windows: ansible-playbook win_agent.yml -i ansible_hosts
