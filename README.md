<div align="center">

<img src="https://media.discordapp.net/attachments/1498241659878768670/1536824710937968771/content.png?ex=6a7ccf0b&is=6a7b7d8b&hm=905a6647aab3e568d077055585f6e057f6ccff952e101a4eb8a6906327e7f3d3&=&format=webp&quality=lossless" alt="Discord API Banner" width="800">

# Discord API Reference

### A clean, stylish and organized Discord API reference for developers.

<p>
  <strong>REST API</strong> •
  <strong>Gateway</strong> •
  <strong>Interactions</strong> •
  <strong>OAuth2</strong> •
  <strong>Webhooks</strong>
</p>

</div>

---

## ✦ Overview

This repository is a compact reference for developers working with the **Discord API**.

Everything is separated into simple files so you can quickly find official documentation, understand the basics, or use the full reference.

---

## 📁 Files

| File | Purpose |
|:---:|---|
| `api.md` | Official Discord API links |
| `shortexplaining.md` | Short explanation of how the API works |
| `readme.md` | Full overview and reference |

---

## ⚡ Discord API

The Discord API is the communication layer between your application and Discord.

```text
                    YOUR APPLICATION
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
          REST API                  Gateway
              │                         │
              ▼                         ▼
       Requests / Actions          Live Events
              │                         │
              └────────────┬────────────┘
                           ▼
                         DISCORD
```

---

## 🌐 REST API

The REST API uses HTTP requests to work with Discord resources.

Common resources include:

- Guilds
- Channels
- Messages
- Users
- Members
- Roles
- Webhooks
- Applications

Typical methods:

```http
GET
POST
PATCH
PUT
DELETE
```

---

## 📡 Gateway

The Gateway provides a persistent connection between your application and Discord.

It is mainly used for real-time events such as:

- Messages
- Guild events
- Member updates
- Presence updates
- Interactions
- Voice-related events

```text
Discord
   │
   │ real-time event
   ▼
Gateway Connection
   │
   ▼
Your Application
```

---

## ⚡ Interactions

Discord Interactions are used for modern application features.

### Slash Commands

```text
/ban
/help
/ping
```

### Components

- Buttons
- Select menus
- Modals
- Autocomplete
- Context menus

Interactions make Discord applications feel fast and interactive.

---

## 🔔 Webhooks

Webhooks are useful for sending automated messages into Discord.

Common uses:

```text
Website → Discord
GitHub  → Discord
Logs    → Discord
Alerts  → Discord
Apps    → Discord
```

They can send normal messages and rich embeds without requiring a traditional bot command.

---

## 🔐 Authentication

Discord applications can authenticate through bot authorization or OAuth2.

Example bot authorization format:

```http
Authorization: Bot YOUR_BOT_TOKEN
```

**Never put a real token inside source code or publish it on GitHub.**

---

## 🛡️ Permissions

Discord permissions control what an application can do inside a server.

Examples:

```text
VIEW_CHANNEL
SEND_MESSAGES
MANAGE_MESSAGES
MANAGE_CHANNELS
MANAGE_ROLES
KICK_MEMBERS
BAN_MEMBERS
ADMINISTRATOR
```

Only request permissions your application actually needs.

---

## ⏱️ Rate Limits

Discord uses rate limits to protect the API.

A good application should:

- Respect `429` responses
- Follow Discord's rate-limit headers
- Avoid unnecessary requests
- Cache data when appropriate
- Prefer Gateway events for real-time updates

---

## 🔒 Security

**Never commit secrets to GitHub.**

Recommended:

```env
DISCORD_TOKEN=your_token
CLIENT_SECRET=your_secret
```

And add sensitive files to `.gitignore`:

```gitignore
.env
.env.*
secrets.json
config.local.json
```

If a secret is exposed, revoke or rotate it immediately.

---

## 🧩 What Can You Build?

With Discord's API, developers can create:

```text
🤖 Bots
🌐 Dashboards
⚡ Slash Commands
🔔 Webhook Systems
🔐 OAuth2 Applications
📊 Logging Systems
🛠️ Server Management
🔗 External Integrations
```

---

## 📚 Documentation

For the official resources, open **`api.md`**.

For a quick explanation, open **`shortexplaining.md`**.

---

<div align="center">

### Discord API Reference

**Clean documentation. Simple structure. Developer focused.**

</div>
