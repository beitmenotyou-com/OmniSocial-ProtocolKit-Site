---
layout: single
title: "Architecture"
permalink: /docs/architecture/
author_profile: true
---

# 🧱 Protocol Architecture

OmniSocial ProtocolKit is built around a **modular, federated architecture** that allows seamless integration and interoperability between major decentralized protocols.

Each protocol is treated as a plug-in module, enabling developers to mix and match based on their needs and community goals.

---

## 🔗 Core Protocol Modules

### **ActivityPub**
- Powers federation with Mastodon, PeerTube, Lemmy, and more
- Uses `username@domain` identity format
- Federates posts, replies, likes, boosts, and media

### **AT Protocol**
- Connects with Bluesky’s Firehose feed
- Enables post discovery and identity via DID + repo structure
- Cross-posting and syncing supported via API adapters

### **Nostr**
- Lightweight, keypair-based protocol
- Users generate a Nostr public/private keypair on signup
- Supports real-time feeds, direct messages (DMs), and events

### **Webfinger + DIDs**
- Resolves `username@domain` handles to decentralized identities
- Webfinger used for ActivityPub and email-style lookups
- DIDs used for portable, verifiable identity across protocols

### **IndieWeb (Webmention, Micropub, etc.)**
- Enables personal publishing and decentralized interactions
- Future modules will support IndieAuth, POSSE, and WebSub

---

## 📡 Content Federation Flow

1. **User creates content** from their OmniSocial dashboard
2. The content is signed, formatted, and broadcast to:
   - Nostr relays (via NIP formats)
   - ActivityPub inboxes (via HTTP)
   - ATProto Firehose feeds
3. Federated platforms ingest, store, and optionally display the content

---

## 🔐 Identity Format

Each profile is assigned a **`username@domain` identifier** that maps to:
- ActivityPub actor URL
- Nostr public key
- ATProto DID (Decentralized Identifier)
- Webfinger JSON resource
- IndieWeb microformats (if enabled)

---

## 🧩 Extensibility

Want to add a new protocol? Use our plug-and-play architecture:
- Create a new module in `/protocols/`
- Implement `normalizePost()`, `sendPost()`, and `resolveIdentity()`
- Plug it into the backend federation engine

---

> This architecture ensures the kit is **future-proof, interoperable, and developer-friendly** — ready to federate with any decentralized network that respects freedom, sovereignty, and open standards.
