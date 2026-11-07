# Privileged intents application

PurgeBot's answers for Discord's **Request Intents Review** form, as of November 2026.

## Application Details

**What does your application do?**

```text
PurgeBot is a Discord bot for deleting messages in bulk. Moderators with the Manage Messages permission run /purge on a channel, a category or the whole server, and choose whose messages go: one user, members with a role, everyone, bots, webhooks, people who left the server, or deleted accounts.

A purge can be limited to the last 1-30 days and can skip a user, specific messages or channels. With a text filter, it deletes only the messages that match, or only the ones that don't. Purges run in the background with a live progress message and can be cancelled at any time.

Premium servers also get /stats for purge statistics and /customize to change the bot's nickname and avatar.

Support server: https://support.purgebot.net
```

**Do you have a public Privacy Policy telling your users about their data usage?** Yes

**Where is your Privacy Policy available?**

```text
On our website: https://biast12.com/purgebot/privacypolicy
```

**Please share a link to your Privacy Policy.**

```text
https://biast12.com/purgebot/privacypolicy
```

## Privileged Gateway Intents

| Intent                 | Select            |
| ---------------------- | ----------------- |
| Server Members Intent  | Leave it unticked |
| Presence Intent        | Leave it unticked |
| Message Content Intent | Tick it           |

## Message Content Intent

| Question                                                                      | Select |
| ----------------------------------------------------------------------------- | ------ |
| Can users opt-out of having their message content data tracked?               | No     |
| Are you storing message content data off-platform (outside of Discord)?       | No     |
| Will the message content data be used to train machine learning or AI Models? | No     |

**Why do you need the Message Content intent?**

```text
The /purge command has an optional filter, so moderators can delete only the messages that contain some text or match a regex. It also checks attachment names and types, so you can remove every .mp4 upload in a channel.

One example is cleaning up after a raid or after accounts get compromised. The same scam link ends up in several channels, mixed in with normal conversation, and moderators want the link gone without wiping everything else those users wrote.

To do this, PurgeBot reads the existing messages in the channels being purged and checks each one against the filter. Without the Message Content intent the text and attachments come back empty, so the filter has nothing to match.

When a moderator runs a purge with a filter, message content is checked in memory and thrown away right after. We never store or log it, never share it, and don't use it for analytics or AI.
```

### Please provide links to screenshots and/or videos that demonstrate your use case

```text
https://youtu.be/igVbPTYn5E4

Three filtered purges in a test server: one removes messages with a scam link, one removes .mp4 uploads, and one keeps only images.
```
