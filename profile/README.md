# 🧹 PurgeBot

> **Powerful, precise message management for Discord servers.**

[![Invite Bot](https://img.shields.io/badge/Invite-PurgeBot-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/oauth2/authorize?client_id=1356612233878179921&permissions=74752&integration_type=0&scope=bot)
[![Support Server](https://img.shields.io/badge/Support-Server-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://support.purgebot.net)

## What it does

PurgeBot lets server administrators delete messages with surgical precision — by user, role, bot, webhook, ex-member, or deleted account, across a whole server, category, or channel. Operations run in the background with real-time progress, and whoever started one can call it off at any time — via `/cancel`, the cancel button, or by posting `@PurgeBot cancel`.

### Commands

| Command            | Description                                       |
| ------------------ | ------------------------------------------------- |
| `/purge user`      | Delete messages from a specific user              |
| `/purge role`      | Delete messages from members with a specific role |
| `/purge everyone`  | Clear all messages in a channel or category       |
| `/purge bot`       | Delete messages sent by bots                      |
| `/purge inactive`  | Remove messages from users who have left          |
| `/purge webhook`   | Delete messages sent by webhooks                  |
| `/purge deleted`   | Remove messages from deleted accounts             |
| `/cancel`          | Cancel a purge you started                        |
| `/help`            | Overview of commands and parameters               |
| `/stats` ✨        | View purge statistics for this server             |
| `/customize` ✨    | Custom nickname, avatar, and branding per server  |
| `@PurgeBot cancel` | Same as `/cancel`, without the command menu       |

### Filtering

Purge commands support optional filtering:

- **Modes** — `contains`, `exact`, `starts_with`, `ends_with`, `regex`
- **Attachments** — filters match message text, attachment filenames and attachment types, so `\.mp4$` or `image/` reach uploads
- **Keep instead of delete** — invert any filter to delete everything *except* what it matches
- **Case sensitivity** — optional
- **Date range** — 1–30 days
- **Scope** — server-wide (except `everyone`), category (with interactive channel-skip UI), or single channel
- **Threads** — optionally include active and archived threads (in server and category scopes, forum threads are always included)
- **Bots** — optionally include bot messages (`role`, `everyone`, `inactive`)

### Exemptions

Anything spared is never deleted, whatever the filter matches:

- **A user** — spare one member’s messages entirely (`role`, `everyone`, `bot`, `inactive`)
- **Specific messages** — by link or ID, separated by commas or spaces
- **Channels** — pick channels to skip when purging a category

### Premium ✨

Server Subscription unlocks `/customize` and `/stats` — set a custom nickname, avatar, remove the "Powered by PurgeBot" footer, and view detailed purge statistics, all per server.

---

<div align="center">

**[Invite PurgeBot](https://discord.com/oauth2/authorize?client_id=1356612233878179921&permissions=74752&integration_type=0&scope=bot)** · **[Support Server](https://support.purgebot.net)**

</div>
