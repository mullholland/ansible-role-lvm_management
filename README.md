# [lvm_management](#lvm_management)

|GitHub|GitLab|
|------|------|
|[![github](https://github.com/mullholland/ansible-role-lvm_management/workflows/Ansible%20Molecule/badge.svg)](https://github.com/mullholland/ansible-role-lvm_management/actions)|[![gitlab](https://gitlab.com/mullholland/ansible-role-lvm_management/badges/main/pipeline.svg)](https://gitlab.com/mullholland/ansible-role-lvm_management)|

description

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
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


## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
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





## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

-   [debian10](https://hub.docker.com/r/mullholland/docker-molecule-debian10)
-   [debian11](https://hub.docker.com/r/mullholland/docker-molecule-debian11)
-   [ubuntu1804](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu1804)
-   [ubuntu2004](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu2004)
-   [ubuntu2204](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu2204)
-   [centos7](https://hub.docker.com/r/mullholland/docker-molecule-centos7)
-   [centos-stream8](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream8)
-   [centos-stream9](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream9)
-   [fedora35](https://hub.docker.com/r/mullholland/docker-molecule-fedora35)
-   [fedora36](https://hub.docker.com/r/mullholland/docker-molecule-fedora36)
-   [amazonlinux](https://hub.docker.com/r/mullholland/docker-molecule-amazonlinux)
-   [rockylinux8](https://hub.docker.com/r/mullholland/docker-molecule-rockylinux8)
-   [rockylinux9](https://hub.docker.com/r/mullholland/docker-molecule-rockylinux9)
-   [almalinux8](https://hub.docker.com/r/mullholland/docker-molecule-almalinux8)
-   [almalinux9](https://hub.docker.com/r/mullholland/docker-molecule-almalinux9)

The minimum version of Ansible required is 2.10, tests have been done to:

-   The previous versions.
-   The current version.



## [Exceptions](#exceptions)

Some variations of the build matrix do not work. These are the variations and reasons why the build won't work:

| variation                 | reason                 |
|---------------------------|------------------------|
| ubi8/9 | Packages not available |


If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-lvm_management/issues)

## [License](#license)

MIT


## [Author Information](#author-information)

[Mullholland](https://github.com/mullholland)

## [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
