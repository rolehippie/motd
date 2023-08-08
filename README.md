# motd

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/motd)
[![General Workflow](https://github.com/rolehippie/motd/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/motd/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/motd/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/motd/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/motd/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/motd/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/motd)](https://github.com/rolehippie/motd/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.motd-blue)](https://galaxy.ansible.com/rolehippie/motd)

Ansible role to configure a custom message of the day.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [motd_disable](#motd_disable)
  - [motd_files](#motd_files)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### motd_disable

List of modules to disable

#### Default value

```YAML
motd_disable:
  - 10-help-text
  - 50-motd-news
  - 80-livepatch
  - 97-overlayroot
```

### motd_files

List of modules to override

#### Default value

```YAML
motd_files:
  - template: updates-available.j2
    dest: 90-updates-available
  - template: release-upgrade.j2
    dest: 91-release-upgrade
  - template: fsck-at-reboot.j2
    dest: 98-fsck-at-reboot
  - template: reboot-required.j2
    dest: 98-reboot-required
```

## Discovered Tags

**_motd_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
