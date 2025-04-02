---
layout: single
title: "Matrix Integration for Messaging"
permalink: /docs/matrix-integration/
author_profile: true
---

# 📨 Matrix Integration for Messaging

OmniSocial ProtocolKit integrates [Matrix](https://matrix.org) — a decentralized, end-to-end encrypted protocol for secure messaging — to power **federated direct messages and group chats** across your social network.

Matrix is modular, open-source, and ideal for communities that value privacy, autonomy, and real-time communication.

---

## 🔐 Why Matrix?

- 💬 **Federated messaging** with full E2EE support
- 🛠️ Fully self-hostable homeserver (e.g., Synapse or Dendrite)
- 🧩 Compatible with Web clients like [Element Web](https://element.io)
- 🌍 Interoperable with other federated apps (via bridges)

---

## 🧱 Features in OmniSocial

| Feature                         | Implementation                             |
|---------------------------------|---------------------------------------------|
| 1:1 Direct Messaging            | Matrix E2EE (Olm protocol)                 |
| Group Chats                     | Rooms with role-based access               |
| Identity Integration            | Matrix ID = `@username:yourdomain.com`     |
| Embedded Chat                   | Optional Element Web iframe or modal       |
| Encrypted Attachments           | Native support via Matrix clients          |

---

## 🧬 Identity Format

We match your OmniSocial identity with Matrix using the format:

```
@username:yourdomain.com
```

This keeps all your decentralized identities aligned — across Matrix, ActivityPub, Nostr, and AT Protocol.

---

## 🚀 Self-Hosting Matrix

To deploy your own Matrix homeserver:

### Option 1: Synapse (official server)

```bash
docker run -it --rm \
  -v ~/.synapse:/data \
  -e SYNAPSE_SERVER_NAME=yourdomain.com \
  matrixdotorg/synapse:latest
```

### Option 2: Dendrite (lightweight Go implementation)

```bash
git clone https://github.com/matrix-org/dendrite
cd dendrite
go run ./cmd/dendrite
```

Then configure `.well-known/matrix/server` on your domain to point to your homeserver.

---

## 🧩 Integration Options

You can embed **Element Web** directly in your frontend:

```html
<iframe
  src="https://chat.yourdomain.com"
  width="100%" height="600px"
  style="border: none;">
</iframe>
```

Or use the Matrix JS SDK for tighter in-app chat features.

---

## 🧪 Advanced Features (Optional)

- Room-based moderation (for community governance)
- Bridging with IRC, Slack, Telegram, etc.
- Decentralized VoIP and video calls (via Jitsi + Matrix)
- Integration with Lightning to unlock chat access

---

## 💡 Use Cases

- Encrypted DMs for creators and followers
- Community-wide discussion rooms
- Private working groups with federated identities
- On-chain or protocol-based room access in the future

---

> Matrix gives OmniSocial the power of secure, decentralized messaging — without relying on Big Tech or closed ecosystems. It’s freedom chat, for the fediverse.
