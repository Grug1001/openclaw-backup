# OpenClaw Backups

Automated backups of OpenClaw configuration and workspace.

## Schedule

- **Daily:** 03:00 AM Brisbane time (retains last 7 days)
- **Weekly:** Sunday backups (retains last 4 weeks)
- **Monthly:** 1st of month (retains last 3 months)

## What Gets Backed Up

- Entire `~/.openclaw/` directory
  - Configuration files
  - Workspace (`workspace/`)
  - Credentials (`credentials/`)
  - Skills, hooks, etc.
- Excludes: `node_modules`, `*.log`, `npm/`

## Backup Locations

- Local: `~/backups/openclaw/`
- Remote: GitHub (this repository)

## Recovery

To restore from a backup:
```bash
# List available backups
ls ~/backups/openclaw/

# Restore latest daily backup
tar xf ~/backups/openclaw/openclaw-YYYY-MM-DD.tar.gz -C ~/
```

---

*Automated by OpenClaw (Craw) — Last updated: 2026-05-20*
