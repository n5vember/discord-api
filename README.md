<div align="center">

<img src="https://media.discordapp.net/attachments/1498241659878768670/1536824710937968771/content.png?ex=6a7ccf0b&is=6a7b7d8b&hm=905a6647aab3e568d077055585f6e057f6ccff952e101a4eb8a6906327e7f3d3&=&format=webp&quality=lossless&width=384&height=217" alt="Discord API Banner" width="384">

# Discord API Collection

**A clean, organized reference for Discord APIs, endpoints, documentation, and useful resources.**

</div>

---

## ✦ About

This repository is a clean reference hub for working with the **Discord API**.

It organizes official API resources, explains the main systems, and provides a quick starting point for developers building Discord bots, applications, integrations, and automation.

> **Simple • Clean • Organized • Developer Friendly**

---

## 📚 What's Inside

| File | Description |
|---|---|
| `api.md` | Direct Discord API links |
| `shortexplaining.md` | Short explanation of how the API works |
| `readme.md` | Full API overview and developer guide |

---

## 🔗 Main API Systems

### 🌐 REST API
Used to request, create, update, and delete Discord resources.

Examples:
- Messages
- Channels
- Guilds
- Users
- Roles
- Webhooks

### 📡 Gateway
Provides a persistent connection for receiving real-time Discord events.

Examples:
- Messages
- Member events
- Presence updates
- Guild events
- Interactions

### ⚡ Interactions
Used for modern Discord features:

- Slash commands
- Buttons
- Select menus
- Modals
- Context menus
- Autocomplete

### 🔔 Webhooks
Useful for sending automated messages, embeds, notifications, logs, and external service events to Discord.

### 🔐 OAuth2
Allows users to authorize applications and provides authentication flows for Discord integrations.

---

## 🧩 How It Works

```text
                 YOUR APPLICATION
                        │
                        ▼
                 ┌──────────────┐
                 │ Discord API  │
                 └──────┬───────┘
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
          REST API             Gateway
              │                   │
              ▼                   ▼
        API Requests        Real-time Events
              │                   │
              └─────────┬─────────┘
                        ▼
                 Your Application
```

Your application can use the REST API for actions and the Gateway for real-time events.

---

## 🔐 Authentication

Discord applications commonly use bot authentication or OAuth2.

Example bot authorization header:

```http
Authorization: Bot YOUR_BOT_TOKEN
```

Example request:

```http
GET https://discord.com/api/v10/users/@me
Authorization: Bot YOUR_BOT_TOKEN
```

> ⚠️ **Never publish bot tokens, client secrets, access tokens, or private webhook URLs.**

---

## 🛡️ Permissions

Discord uses permissions to control what applications can access and modify.

Common permissions include:

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

Only request the permissions your application actually needs.

---

## ⏱️ Rate Limits

Discord protects its API with rate limits.

Your application should:

- Handle `429` responses.
- Respect Discord's rate-limit information.
- Avoid unnecessary requests.
- Cache data where appropriate.
- Use Gateway events when real-time updates are needed.

---

## 🚀 Common Projects

This API reference can be useful for building:

- 🤖 Discord bots
- 🌐 Discord dashboards
- ⚡ Slash-command systems
- 🔔 Webhook systems
- 🔐 OAuth2 applications
- 🛠️ Server management tools
- 📊 Logging systems
- 🔗 External integrations
- 🧪 API testing tools

---

## 🗂️ Repository Structure

```text
.
├── api.md
├── shortexplaining.md
└── readme.md
```

**`api.md`**  
Direct Discord API documentation links.

**`shortexplaining.md`**  
A short explanation of the Discord API and its basic workflow.

**`readme.md`**  
The complete overview, architecture, security notes, and developer reference.

---

## 📖 Official Documentation

The complete official documentation is available through the Discord Developer Portal.

See **`api.md`** for the direct links to Discord's official resources.

---

## ⚠️ Security

Never commit secrets to GitHub.

Use environment variables instead:

```env
DISCORD_TOKEN=your_private_token
CLIENT_SECRET=your_private_secret
```

Add sensitive files to `.gitignore`:

```gitignore
.env
.env.*
secrets.json
config.local.json
```

---

<div align="center">

**Discord API Reference**

*Built for developers. Designed to stay simple.*

</div>
