# Changelog

All notable changes to avocado-bsp-raspberrypi5 are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.1]

### Changed
- `kernel-module-hailo-pci` moved under `kernel-6.6.*`: the in-tree Hailo
  driver is not in rpi-6.12.y, so the common list failed to install on the
  6.12 kernel the 2026 feed boots by default.

### Added
- `wireless-regdb-static`, so cfg80211 has a regulatory database (the board
  booted with `regulatory.db` missing and WiFi pinned to country 00).

## [0.1.0]

### Added
- Initial release: Board support for the Raspberry Pi 5.
- CI via the shared `avocado-linux/actions` reusable workflows: PR build check
  (`test.yml`) and tag-driven package + publish to the Avocado feed (`release.yml`).
