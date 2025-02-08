rpi_wordclock
=============
[![Ansible Lint](https://github.com/oxivanisher/role-rpi_wordclock/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-rpi_wordclock/actions/workflows/ansible-lint.yml)

This role installs and configures the software stack for the [rpi_wordclock of bk1285](https://github.com/bk1285/rpi_wordclock). It basically does some stuff that https://github.com/bk1285/rpi_wordclock/pull/250 would implement ... Open since March 2023.

Role Variables
--------------

| Name                          | Comment                              | Default value                    |
|-------------------------------|--------------------------------------|----------------------------------|
| rpi_wordclock_bcm2835_version | Version of the bcm2835 driver to be used | `1.68` |
| rpi_wordclock_bcm2835_tar_url | The URL for the bcm2835 driver download | `http://www.airspayce.com/mikem/bcm2835/bcm2835-{{ rpi_wordclock_bcm2835_version }}.tar.gz` |
| rpi_wordclock_pywapi_version  | Version of pywapi to be used | `0.3.8` |
| rpi_wordclock_pywapi_tar_url  | The URL for pywapi download | `https://launchpad.net/python-weather-api/trunk/{{ rpi_wordclock_pywapi_version }}/+download/pywapi-{{ rpi_wordclock_pywapi_version }}.tar.gz` |
| rpi_wordclock_user            | The user for which the software will be installed | `pi` |


Dependencies
------------

None

Example Playbook
----------------
```yaml
- name: Install wordclock software
  hosts: rpis
  roles:
    - role: oxivanisher.raspberry_pi.rpi_wordclock
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.raspberry_pi](https://galaxy.ansible.com/ui/repo/published/oxivanisher/raspberry_pi/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-raspberry_pi).
