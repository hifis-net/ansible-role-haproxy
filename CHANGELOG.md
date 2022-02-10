<!--
SPDX-FileCopyrightText: 2020 Helmholtz Centre for Environmental Research (UFZ)
SPDX-FileCopyrightText: 2020 Helmholtz-Zentrum Dresden-Rossendorf (HZDR)

SPDX-License-Identifier: Apache-2.0
-->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Group your changes into these categories:

`Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`.

## Unreleased

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.3.0...main)

### Fixed

* Fix failing dry-run if ppa changes
  ([!50](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/50)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [1.3.0](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v1.3.0) - 2021-11-23

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.2.0...v1.3.0)

### Changed
* Increase HAProxy version in file README
  ([!45](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/45)
  by [christian.hueser.hzdr](https://gitlab.com/christian.hueser.hzdr)).
* Bump project dependencies python version to 3.9
  ([!47](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/47)
  by [Normo](https://gitlab.com/Normo)).
* Update project dependencies
  ([!48](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/48)
  by [Normo](https://gitlab.com/Normo)).

### Fixed
* Set empty default value for backends and frontend_ip
  ([!46](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/46)
  by [Normo](https://gitlab.com/Normo)).

## [1.2.0](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v1.2.0) - 2021-06-18

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.1.1...v1.2.0)

### Added
* Copy TLS chain file when self-signed cert creation is disabled
  ([!42](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/42)
  by [Normo](https://gitlab.com/Normo)).

### Changed
* Set more restrictive file permissions for others
  ([!43](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/43)
  by [Normo](https://gitlab.com/Normo)).

## [1.1.1](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v1.1.1) - 2021-06-14

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.1.0...v1.1.1)

### Added
* Automate import to Ansible Galaxy via GitHub Actions
  ([!39](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/39)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

### Fixed
* Fix initial role execution if SSL certificate generation disabled
  ([!40](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/40)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

## [1.1.0](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v1.1.0) - 2021-06-11

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.0.1...v1.1.0)

### Changed
* Reduce DHParam size in molecule tests
  ([!32](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/32)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Update all Python dependencies to the most recent version
  ([!35](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/35)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

### Fixed
* Fix initial dry run and improve molecule test sequence
  ([!33](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/33)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Use FQDN for Ansible modules
  ([!34](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/34)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
* Add galaxy namespace hifis to the role metadata
  ([!37](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/37)
  by [Normo](https://gitlab.com/Normo)).
* Prefix unprefixed variables with haproxy_
  ([!36](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/36)
  by [tobiashuste](https://gitlab.com/tobiashuste)).

### Deprecated
* Deprecate the variables `frontend_ip` and `backends` which are replaced
  by `haproxy_frontend_ip` and `haproxy_backends`.
  Support for the unprefixed variables will be removed in version 2.0.

## [1.0.1](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v1.0.1) - 2021-01-29

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.0.0...v1.0.1)

### Fixed
- Check HAProxy configuration file via an Ansible handler
  ([!27](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/27)
  by [christian.hueser.hzdr](https://gitlab.com/christian.hueser.hzdr)).

## [1.0.0](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v1.0.0) - 2021-01-25

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v0.2.0...v1.0.0)

### Added
- Check HAProxy configuration via a role task
  ([!22](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/22)
  by [christian.hueser.hzdr](https://gitlab.com/christian.hueser.hzdr)).
  
### Changed
- Update role meta information
  ([!24](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/24)
  by [Normo](https://gitlab.com/Normo)).
- Update README.md
  ([!25](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/25)
  by [Normo](https://gitlab.com/Normo)).

### Fixed
- Check package version of HAProxy to decide on install / upgrade step
  ([!21](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/21)
  by [christian.hueser.hzdr](https://gitlab.com/christian.hueser.hzdr)).

## [0.2.0](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v0.2.0) - 2020-12-03

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v0.1.0...v0.2.0)

### Added
- Configure DH param size via variable
  ([!15](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/15)
  by [Normo](https://gitlab.com/Normo)).

### Changed
- Improve and speed up the CI pipeline
  ([!12](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/12)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
- Add missing Pipfile.lock file and update Ansible to 2.10.0
  ([!11](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/11)
  by [tobiashuste](https://gitlab.com/tobiashuste)).
- Resolve "HAProxy isn't restarted/reloaded on SSL config change"
  ([!16](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/16)
  by [Normo](https://gitlab.com/Normo)).
- Resolve "Make self-signed SSL generation optional"
  ([!17](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/17)
  by [Normo](https://gitlab.com/Normo)).
- Bump Ansible to 2.10.4
  ([!19](https://gitlab.com/hifis/ansible/haproxy-role/-/merge_requests/19)
  by [Normo](https://gitlab.com/Normo)).

## [0.1.0](https://gitlab.com/hifis/ansible/haproxy-role/-/releases/v0.1.0) - 2020-08-14

### Added
Initial release of the Ansible HAProxy Role.
