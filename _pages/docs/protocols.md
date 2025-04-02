---
layout: single
title: "Supported Protocols"
permalink: /docs/protocols/
author_profile: true
---

# 🌐 Supported Protocols

OmniSocial ProtocolKit is protocol-agnostic by design — built to bridge the **Fediverse, Nostr, ATProto, IndieWeb, and beyond** through modular, plug-and-play integrations.

Each protocol is treated as a self-contained module with its own identity logic, post formatting, and federation behavior.

---

## 🔗 Core Supported Protocols

### 🐘 ActivityPub
- Used by Mastodon, PeerTube, Lemmy, and more
- Enables federation of posts, replies, boosts, likes, and media
- Actor model based on `username@domain` and Webfinger

### 🔵 AT Protocol (Bluesky)
- Decentralized identity and repository model
- Firehose feed support for content discovery
- Supports DID + PDS (Personal Data Server) federation
- Content syncing, repo following, and indexing

### ⚡ Nostr
- Public key-based publishing
- Uses NIP standards for posts, reactions, DMs, and events
- Lightning-fast and censorship-resistant
- Each profile includes a Nostr pubkey generated on creation

### 🌍 Webfinger
- Identity resolution system (used in ActivityPub and IndieWeb)
- Resolves `username@domain` to resource URLs and JSON metadata
- Required for ActivityPub federation and decentralized lookup

### 🧬 DIDs (Decentralized Identifiers)
- Enables portable, verifiable identity across protocols
- DID Documents map to public keys, service endpoints, etc.
- Used in ATProto and optionally in Nostr/Matrix

### 🧪 IndieWeb (Upcoming)
- Webmention, Micropub, IndieAuth support planned
- POSSE (Publish Own Site, Syndicate Elsewhere) workflows
- Enables website-as-identity model

### 📨 Matrix (Optional)
- E2EE real-time messaging
- Group chats, roles, moderation, and bridges to other platforms
- Fully self-hostable with Synapse or Dendrite

---

## 📦 Protocol Modules

Each protocol lives in its own module under `/protocols/`. These modules include:

- Content normalization and formatting (`normalizePost()`)
- Posting and broadcasting logic (`sendPost()`)
- Identity resolution (`resolveIdentity()`)
- Adapter functions for feed syncing and webhook listening

---

## 🔧 Add Your Own

Want to support a new protocol (e.g., Farcaster, Secure Scuttlebutt, RSS)? You can create a new module and drop it into the system.

> OmniSocial is **modular, extensible, and future-proof** — designed to grow with the protocols that power tomorrow’s internet.

---

## 🧪 Protocol Interop Flow

1. User creates a post
2. OmniSocial formats and routes the post to selected protocols
3. Each module handles delivery and formatting for its protocol
4. Inbound posts are normalized into a unified feed for the user

---

> OmniSocial isn’t just multi-protocol — it’s inter-protocol. Build once, post everywhere.
