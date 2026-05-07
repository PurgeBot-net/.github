# 🧹 PurgeBot

> **Powerful, precise message management for Discord servers.**

[![Invite Bot](https://img.shields.io/badge/Invite-PurgeBot-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/oauth2/authorize?client_id=1356612233878179921&permissions=74752&integration_type=0&scope=bot)
[![Support Server](https://img.shields.io/badge/Support-Server-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://support.purgebot.net)

## What it does

PurgeBot lets server administrators delete messages with surgical precision — by user, role, webhook, inactivity, or across an entire server, category, or channel. Operations run in the background with real-time progress and a one-click cancel button.

### Commands

| Command           | Description                                          |
| ----------------- | ---------------------------------------------------- |
| `/purge user`     | Delete messages from a specific user                 |
| `/purge role`     | Delete messages from members with a specific role    |
| `/purge everyone` | Clear all messages in a channel, category, or server |
| `/purge inactive` | Remove messages from users who have left             |
| `/purge webhook`  | Delete messages sent by webhooks                     |
| `/purge deleted`  | Remove messages from deleted accounts                |
| `/help`           | Overview of commands and parameters                  |
| `/stats` ✨       | View purge statistics for this server                |
| `/customize` ✨   | Custom nickname, avatar, and branding per server     |

### Filtering

Every purge command supports optional content filtering:

- **Modes** — `contains`, `exact`, `starts_with`, `ends_with`, `regex`
- **Case sensitivity** — optional
- **Date range** — 1–30 days
- **Scope** — server-wide, category (with interactive channel-skip UI), or single channel
- **Threads** — optionally include active and archived threads
- **Bots** — optionally include bot messages

### Premium ✨

Server Subscription unlocks `/customize` and `/stats` — set a custom nickname, avatar, remove the "Powered by PurgeBot" footer, and view detailed purge statistics, all per server.

## Repositories

| Repository                                                   | Description                                                                       |
| ------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| [interactions](https://github.com/PurgeBot-net/interactions) | HTTP service — receives and routes slash commands, modals, and components         |
| [gateway](https://github.com/PurgeBot-net/gateway)           | Gateway service — maintains the Discord WebSocket connection and publishes events |
| [purger](https://github.com/PurgeBot-net/purger)             | Worker service — consumes purge jobs from Redis and performs message deletion     |
| [common](https://github.com/PurgeBot-net/common)             | Shared Go library — job types, Redis helpers, guild locking                       |
| [database](https://github.com/PurgeBot-net/database)         | Database package — PostgreSQL schema and query functions                          |
| [locale](https://github.com/PurgeBot-net/locale)             | i18n package — all user-facing strings and translations                           |
| [workflows](https://github.com/PurgeBot-net/workflows)       | Reusable CI/CD workflows for all services                                         |
| [docker](https://github.com/PurgeBot-net/docker)             | Docker Compose deployment stack                                                   |
| [template](https://github.com/PurgeBot-net/template)         | GitHub template for new service repositories                                      |

## Stack

Go · PostgreSQL · Redis · Kafka · Docker · GitHub Actions · Sentry

---

<div align="center">

**[Invite PurgeBot](https://discord.com/oauth2/authorize?client_id=1356612233878179921&permissions=74752&integration_type=0&scope=bot)** · **[Support Server](https://support.purgebot.net)**

</div>
