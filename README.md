Wazuh Agent
=========

Ansible role to install and configure Wazuh Agent on Linux and Windows hosts

Requirements
------------

None

Role Variables
--------------

- wazuh_version: "4.x"
- wazuh_manager_ip: "" #(required)
- wazuh_manager_port: "1514"
- wazuh_registration_port: "1515"
- wazuh_manager_protocol: "tcp"
- wazuh_agent_group: ["default"]
- wazuh_registration_password: "" #(required)
- wazuh_autoupdate: true

Dependencies
------------

- libyanspider.firewall_ansible_role

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: all
      roles:
         - { role: libyanspider.wazuh_agent_role, wazuh_manager_ip: 127.0.0.1, wazuh_registration_password: strongpassword }
```

License
-------

BSD

Author Information
------------------

Ahmed Shibani (#shumbashi)
sheipani@gmail.com