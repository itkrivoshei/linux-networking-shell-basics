<div align="center">

# Linux Networking Shell Basics

UNIX/Linux command collection for networking lookups, system inspection, and Bash utility scripts.

[![Shell checks](https://img.shields.io/github/actions/workflow/status/itkrivoshei/linux-networking-shell-basics/shell.yml?branch=main&style=for-the-badge&label=shell%20checks&logo=githubactions&logoColor=white&labelColor=0f172a)](https://github.com/itkrivoshei/linux-networking-shell-basics/actions/workflows/shell.yml)
[![Bash](https://img.shields.io/badge/Bash-scripts-4eaa25?style=for-the-badge&logo=gnubash&logoColor=white&labelColor=0f172a)](scripting)
[![License](https://img.shields.io/github/license/itkrivoshei/linux-networking-shell-basics?style=for-the-badge&labelColor=0f172a)](LICENSE)

</div>

## Overview

This repository contains small UNIX/Linux command references and Bash scripts for:

- networking lookups and diagnostics;
- system inspection;
- basic shell scripting practice;
- running commands through a simple interactive menu.

Some commands reflect BSD/macOS-style output, such as `ifconfig en0` or `netstat -nr`, and may need adjustment on a modern Linux host.

## Repository Areas

| Directory                 | Contents                                                                |
| ------------------------- | ----------------------------------------------------------------------- |
| [`network/`](network)     | Commands around interfaces, routing, DNS, ARP, traceroute, and services |
| [`system/`](system)       | System information, users, processes, packages, paths, and permissions  |
| [`scripting/`](scripting) | Bash scripts plus an interactive menu for browsing and running items    |

## Usage

Inspect command examples:

```bash
cat network/04
cat system/01
```

Run the interactive menu:

```bash
cd scripting
./03
```

Run the user listing script:

```bash
cd scripting
./01
```

## Safety Note

[`scripting/02`](scripting/02) can delete local users.

It is blocked by default and requires an explicit opt-in:

```bash
cd scripting
ALLOW_USER_DELETE=1 ./02
```

Review the script before running it on any real machine.

## Checks

Run Bash syntax validation locally:

```bash
bash -n network/* system/* scripting/*
```

The [GitHub Actions workflow](.github/workflows/shell.yml) runs Bash syntax validation for files under [`network/`](network), [`system/`](system), and [`scripting/`](scripting).

## License

[GPL-3.0](LICENSE)
