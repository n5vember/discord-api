# ✦ Discord API — Developer Reference

> **A clean, modern, developer-friendly reference for building Discord applications, bots, integrations, and automation.**

<p align="center">

**HTTP API** · **Gateway** · **Interactions** · **Webhooks** · **OAuth2** · **Resources**

</p>

---

## ◈ Overview

The **Discord API** allows applications to communicate with Discord programmatically.

With it, you can build:

- 🤖 Discord bots
- ⚡ Slash commands
- 🎛️ Buttons, menus, and modals
- 💬 Message systems
- 🌐 Web integrations
- 🔔 Webhook notifications
- 🔐 OAuth2 applications
- 🛠️ Server and channel management tools
- 📡 Real-time event systems

Discord's platform is mainly built around the **HTTP API**, **Gateway**, **Interactions**, and **OAuth2** systems.

---

## ✦ Documentation Map

| System | Purpose |
| --- | --- |
| 🌐 **HTTP API** | Send requests and manage Discord resources |
| 📡 **Gateway** | Receive real-time Discord events |
| ⚡ **Interactions** | Commands, buttons, menus, and modals |
| 🔔 **Webhooks** | Send automated messages to Discord |
| 🔐 **OAuth2** | Authenticate users and authorize applications |
| 📦 **Resources** | Users, guilds, channels, messages, applications, and more |

### Official Documentation

**Main Documentation**  
https://discord.com/developers/docs/intro

**API Reference**  
https://discord.com/developers/docs/reference

**Resources**  
https://discord.com/developers/docs/resources

---

# 01 — 🌐 HTTP API

The Discord HTTP API lets your application make requests to Discord.

It can be used for operations such as:

```text
GET     → retrieve information
POST    → create or send something
PATCH   → update something
PUT     → add or replace something
DELETE  → remove something
```

Common use cases include:

- Getting server information
- Sending messages
- Managing channels
- Managing guild resources
- Working with users
- Creating and managing webhooks
- Managing application resources

📖 **Reference:**  
https://discord.com/developers/docs/reference

---

# 02 — 📡 Gateway

The **Discord Gateway** provides a persistent connection for receiving real-time events.

Instead of repeatedly asking Discord whether something changed, your application can stay connected and receive events as they happen.

Examples include:

```text
MESSAGE_CREATE
GUILD_CREATE
GUILD_MEMBER_ADD
INTERACTION_CREATE
READY
RESUMED
```

A Gateway connection is especially useful for bots that need to react quickly to Discord activity.

📖 **Gateway Documentation:**  
https://discord.com/developers/docs/topics/gateway

---

# 03 — ⚡ Interactions

Interactions power many modern Discord features.

They include:

- `/slash` commands
- Buttons
- Select menus
- Modals
- User context commands
- Message context commands
- Autocomplete

A typical interaction flow looks like:

```text
User
  ↓
Discord
  ↓
Your Application
  ↓
Interaction Handler
  ↓
Response
  ↓
Discord
```

📖 **Interaction Documentation:**  
https://discord.com/developers/docs/interactions/receiving-and-responding

---

# 04 — 🔔 Webhooks

Webhooks allow applications and external services to send messages to Discord without operating like a normal bot connection.

They are useful for:

- Logs
- Website notifications
- Deployment alerts
- Monitoring systems
- Automated announcements
- External application events

📖 **Webhook Documentation:**  
https://discord.com/developers/docs/resources/webhook

> ⚠️ **Security:** Never publicly share a webhook URL if it provides access to a private channel or system.

---

# 05 — 🔐 Authentication

Discord applications can authenticate through different systems depending on what they need to access.

Common authentication concepts include:

### Bot Authentication

Used by Discord bots to interact with Discord using their bot identity.

### OAuth2

Used when an application needs users to authorize access.

OAuth2 can be used for things such as:

- User authentication
- Authorizing applications
- Requesting specific scopes
- Obtaining access tokens

📖 **Discord Developer Documentation:**  
https://discord.com/developers/docs/intro

> 🔒 **Never publish bot tokens, client secrets, or access tokens.**

---

# 06 — 📦 Discord Resources

Discord exposes many resources through its API.

### 👤 Users

Information and operations related to Discord users.

https://discord.com/developers/docs/resources/user

### 🏠 Guilds

A **guild** is Discord's API term for a server.

https://discord.com/developers/docs/resources/guild

### 💬 Channels

Text, voice, category, forum, and other Discord channel types.

https://discord.com/developers/docs/resources/channel

### 📨 Messages

Used for working with Discord messages where the application has the required permissions.

https://discord.com/developers/docs/resources/message

### 🧩 Applications

Applications are the foundation for bots, commands, integrations, and OAuth2 features.

https://discord.com/developers/docs/resources/application

---

# 07 — 🧠 How Everything Connects

A Discord application can use multiple systems together.

For example:

```text
                    ┌─────────────────┐
                    │     Discord     │
                    └────────┬────────┘
                             │
             ┌───────────────┼───────────────┐
             │               │               │
             ▼               ▼               ▼
        ┌─────────┐     ┌──────────┐    ┌───────────┐
        │ HTTP API│     │ Gateway  │    │ Webhooks  │
        └────┬────┘     └────┬─────┘    └─────┬─────┘
             │               │                │
             └───────────────┼────────────────┘
                             ▼
                    ┌─────────────────┐
                    │ Your Application│
                    └─────────────────┘
                             │
                             ▼
                    Commands / Logic
```

A bot might use:

**Gateway** → receive an event  
**Application logic** → process it  
**HTTP API** → perform an action  
**Interaction response** → reply to the user

---

# 08 — 🛡️ Permissions & Security

Discord permissions control what an application can do.

Always make sure your application has only the permissions it actually needs.

### Never expose:

```text
Bot Tokens
Client Secrets
OAuth2 Access Tokens
Private API Keys
Private Webhook URLs
```

Do not commit secrets to Git repositories or place them directly inside public frontend code.

A safer approach is to use environment variables:

```env
DISCORD_TOKEN=your_private_token
CLIENT_SECRET=your_private_secret
```

---

# 09 — ⏱️ Rate Limits

Discord APIs use rate limits to protect the platform.

Your application should:

- Respect HTTP `429` responses
- Follow Discord's rate-limit information
- Avoid unnecessary requests
- Cache data when appropriate
- Use Gateway events when real-time updates are available

📖 **API Reference:**  
https://discord.com/developers/docs/reference

---

# 10 — 🚀 Typical Bot Architecture

A simple Discord bot can be structured like this:

```text
Your Bot
│
├── Authentication
│
├── Gateway
│   └── Event handling
│
├── Commands
│   ├── Slash commands
│   ├── Buttons
│   ├── Menus
│   └── Modals
│
├── API Layer
│   ├── Users
│   ├── Guilds
│   ├── Channels
│   └── Messages
│
└── Services
    ├── Logging
    ├── Database
    └── Configuration
```

This keeps your Discord logic organized and makes larger applications easier to maintain.

---

# 11 — 📚 Official Links

| Documentation | Link |
| --- | --- |
| Discord Developers | https://discord.com/developers/docs/intro |
| API Reference | https://discord.com/developers/docs/reference |
| Resources | https://discord.com/developers/docs/resources |
| Gateway | https://discord.com/developers/docs/topics/gateway |
| Interactions | https://discord.com/developers/docs/interactions/receiving-and-responding |
| Webhooks | https://discord.com/developers/docs/resources/webhook |
| Applications | https://discord.com/developers/docs/resources/application |
| Users | https://discord.com/developers/docs/resources/user |
| Guilds | https://discord.com/developers/docs/resources/guild |
| Channels | https://discord.com/developers/docs/resources/channel |
| Messages | https://discord.com/developers/docs/resources/message |

---

# ✦ Quick Start

If you're new to Discord development:

```text
1. Create a Discord application
          ↓
2. Configure your application/bot
          ↓
3. Choose your authentication method
          ↓
4. Connect through the Gateway if real-time events are needed
          ↓
5. Use HTTP endpoints for API operations
          ↓
6. Add interactions such as slash commands/buttons
          ↓
7. Handle permissions and rate limits
          ↓
8. Keep all credentials private
```

---

## ⚠️ Important

This README is a **reference and overview**, not a replacement for Discord's official documentation.

Discord's API can change over time. Always verify endpoint behavior, permissions, authentication requirements, and limits against the current official documentation.

**Official documentation:**  
https://discord.com/developers/docs/intro

---

<p align="center">

**Built for Discord developers.**  
*Clean documentation • Clear architecture • Official references*

</p>
