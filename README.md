# Ansible Cloud: Security Group role

An Ansible role for managing security groups on the Cloud in an agnostic cloud provider way.

This role is part of the [ansible-cloud](https://github.com/redhat-cip/ansible-cloud) broader effort.

## Pre-requisites

Please refer to [ansible-cloud](https://github.com/redhat-cip/ansible-cloud) [README.md](https://github.com/redhat-cip/ansible-cloud/blob/master/README.md) to see how to configure your system the proper way for the provide you wish to use.


## Role Variables

| Variable name             | Required  | Default | Type   | Description                          |
|---------------------------|-----------|---------|--------|--------------------------------------|
| cloud_securitygroup_name  | True      | N/A     | String | Name of the security group           |
| cloud_securitygroup_state | False     | present | String | Should the security group be present |


## Example

```
---
- hosts: localhost
  vars:
    ansible_cloud_provider: vultr
  tasks:
    - name: Create security group
      include_role:
        name: cloud-securitygroup
      vars:
        cloud_securitygroup_name: 'ansiblecloud-testsecuritygroup'
```


## License

Apache 2.0


## Authors Information

  - Ricardo Carrillo Cruz <ricarril@redhat.com>
  - Yanis Guenane <yguenane@redhat.com>
