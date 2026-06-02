<div align="center">

# Linux Networking Shell Basics

UNIX/Linux command collection for networking lookups, system inspection, and a few Bash utilities.

[![Shell checks](https://img.shields.io/github/actions/workflow/status/itkrivoshei/linux-networking-shell-basics/shell.yml?branch=main&style=for-the-badge&label=shell%20checks&logo=githubactions&logoColor=white)](https://github.com/itkrivoshei/linux-networking-shell-basics/actions/workflows/shell.yml)
[![Bash](https://img.shields.io/badge/Bash-scripts-4eaa25?style=for-the-badge&logo=gnubash&logoColor=white)](scripting)
[![License](https://img.shields.io/github/license/itkrivoshei/linux-networking-shell-basics?style=for-the-badge)](LICENSE)

</div>

## Repository Areas

| Directory | Contents |
| --- | --- |
| `network/` | Commands around interfaces, routing, DNS, ARP, traceroute, and services |
| `system/` | System information, users, processes, packages, paths, and permissions |
| `scripting/` | Bash scripts plus an interactive menu for browsing/running items |

Some commands reflect BSD/macOS style output (`ifconfig en0`, `netstat -nr`) and may need adjustment on a modern Linux host.

## Run

Inspect a command file:

```bash
cat network/04
cat system/01
```

Run the menu:

```bash
cd scripting
./03
```

Run the user listing script:

```bash
cd scripting
./01
```

`scripting/02` can delete local users. It is blocked by default and requires an explicit opt-in:

```bash
cd scripting
ALLOW_USER_DELETE=1 ./02
```

Review it before running on any real machine.

## Check Syntax

```bash
bash -n network/* system/* scripting/*
```

The GitHub Actions workflow runs Bash syntax validation for all files under `network/`, `system/`, and `scripting/`.

## License

[GPL-3.0](LICENSE)
