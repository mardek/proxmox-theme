# Proxmox Infrastructure

Centralized configuration and automation for Proxmox VE homelab environment.

## Overview

Infrastructure as code for Proxmox-based virtualization platform.

## Structure

| Directory | Purpose |
|-----------|---------|
| `themes/` | UI theme backups |
| `vm-configs/` | VM definitions |
| `scripts/` | Automation scripts |
| `docs/` | Runbooks |

## Themes

| Theme | Location | Source |
|-------|----------|--------|
| Proxmox VE | `themes/pve/` | pve-custom-css |

### Proxmox Theme

Backup from 2026-10-20. Files:

- `80pvecustomcss-hook` — package hook
- `custom.css` — main styles
- `index.html.tpl` — template override
- `pve-custom-css-restore` — restore script
- `RESTORE.md` — documentation
