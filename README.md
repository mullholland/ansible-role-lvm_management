# [Ansible role lvm_management](#lvm_management)

Configures lvm drives on the server.

|GitHub|Downloads|Version|
|------|---------|-------|
|[![github](https://github.com/mullholland/ansible-role-lvm_management/actions/workflows/molecule.yml/badge.svg)](https://github.com/mullholland/ansible-role-lvm_management/actions/workflows/molecule.yml)|[![downloads](https://img.shields.io/ansible/role/d/mullholland/lvm_management)](https://galaxy.ansible.com/mullholland/lvm_management)|[![Version](https://img.shields.io/github/release/mullholland/ansible-role-lvm_management.svg)](https://github.com/mullholland/ansible-role-lvm_management/releases/)|
## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/mullholland/ansible-role-lvm_management/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true
  # vars:
  #   example_var: "value"
  roles:
    - role: "mullholland.lvm_management"
```



## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/mullholland/ansible-role-lvm_management/blob/master/defaults/main.yml):

```yaml
---
lvm_management_max_gap_kb: 1024
lvm_management_devices: []
#  - partition: /dev/vda      # Which HDD should be resized
#    number: 2                # which partition number should be resized

lvm_management_lvm_configuration: []
#  - name: "lv_root"  # Name of the logical volume group
#    size: "10G"      # What should happen to the colume
#                     # 10G => sets the size to 10G regardless of the current size (WARNING DO NOT SHRINK IT!!!!!!)
#                     # +10G => adds 10G after each ansible run (NOT idempotent!!!)
#                     # +100%FREE => adds all Free Space to the lv
#    vg: "system"     # The name of the VolumeGroup the LV resides
#    fstype: "ext4"   # The filesystem the lv uses
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/mullholland/ansible-role-lvm_management/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://mullholland.net) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/mullholland/ansible-role-lvm_management/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/r/mullholland/enterpriselinux)|all|
|[Amazon](https://hub.docker.com/r/mullholland/amazonlinux)|Candidate|
|[Fedora](https://hub.docker.com/r/mullholland/fedora/)|all|
|[Ubuntu](https://hub.docker.com/r/mullholland/ubuntu)|all|
|[Debian](https://hub.docker.com/r/mullholland/debian)|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-lvm_management/issues).

## [License](#license)

[MIT](https://github.com/mullholland/ansible-role-lvm_management/blob/master/LICENSE).

## [Author Information](#author-information)

[Mullholland](https://mullholland.net)
