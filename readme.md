# Discord API Documentation

A quick reference for the official Discord API and its main systems.

## 1. Introduction

The Discord API allows applications and bots to interact with Discord programmatically. It provides HTTP endpoints for working with Discord resources and a Gateway for receiving real-time events.

Official introduction:

https://discord.com/developers/docs/intro

## 2. API Reference

The API Reference contains the complete list of Discord endpoints, parameters, request methods, response formats, permissions, and resource definitions.

https://discord.com/developers/docs/reference

## 3. Resources

Discord exposes different resources through the API.

Common resources include:

- Users
- Guilds (servers)
- Channels
- Messages
- Applications
- Webhooks

Resource documentation:

https://discord.com/developers/docs/resources

## 4. HTTP API

The HTTP API is used when your application needs to request or change Discord data.

Typical operations include:

- Getting information
- Creating resources
- Updating resources
- Deleting resources
- Sending messages
- Managing channels and guild resources

Always check the official endpoint documentation for required permissions, parameters, and authentication.

## 5. Gateway

The Discord Gateway provides a persistent connection for receiving real-time events.

Examples of events include:

- Messages
- Guild events
- Member events
- Interaction-related events
- Connection and session events

Gateway documentation:

https://discord.com/developers/docs/topics/gateway

## 6. Interactions

Interactions are used for modern Discord features such as:

- Slash commands
- Buttons
- Select menus
- Modals
- Context-menu commands

Documentation:

https://discord.com/developers/docs/interactions/receiving-and-responding

## 7. Webhooks

Webhooks provide a way to send messages to Discord without maintaining a normal bot connection.

They can be useful for:

- Notifications
- Logs
- Automated messages
- External applications

Documentation:

https://discord.com/developers/docs/resources/webhook

## 8. Applications

Discord applications are the foundation for bots, commands, OAuth2 integrations, and other Discord integrations.

Documentation:

https://discord.com/developers/docs/resources/application

## 9. Users

The User resource contains information and operations related to Discord users.

Documentation:

https://discord.com/developers/docs/resources/user

## 10. Guilds

Guilds are Discord servers. The API provides endpoints for working with guild/server data and related resources.

Documentation:

https://discord.com/developers/docs/resources/guild

## 11. Channels

Channels include text, voice, category, forum, and other Discord channel types.

Documentation:

https://discord.com/developers/docs/resources/channel

## 12. Messages

The Message resource is used for reading, creating, editing, and deleting messages where the application has the required permissions.

Documentation:

https://discord.com/developers/docs/resources/message

## 13. Authentication

Discord supports authentication through bot authentication and OAuth2. The correct authentication method depends on what your application is trying to do.

Never publish bot tokens, client secrets, or other private credentials.

## 14. Permissions and Rate Limits

Discord requests are subject to permissions and rate limits. An application must have the required permissions for the operation it is attempting, and requests should respect Discord's rate-limit responses.

## 15. Official Documentation

For the most accurate and current information, use Discord's official developer documentation:

https://discord.com/developers/docs/intro

https://discord.com/developers/docs/reference

https://discord.com/developers/docs/resources

https://discord.com/developers/docs/topics/gateway

https://discord.com/developers/docs/interactions/receiving-and-responding
