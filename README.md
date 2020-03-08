# motd

[![Build Status](https://cloud.drone.io/api/badges/rolehippie/motd/status.svg)](https://cloud.drone.io/rolehippie/motd)

Ansible role to configure motd

## Table of content

* [Default Variables](#default-variables)
  * [motd_disable](#motd_disable)
  * [motd_files](#motd_files)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

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

## Dependencies

None.

## License

Apache-2.0

## Author

Thomas Boerger
