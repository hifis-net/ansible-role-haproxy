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

[List of commits](https://gitlab.com/hifis/ansible/haproxy-role/-/compare/v1.0.1...main)

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
