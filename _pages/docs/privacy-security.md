---
layout: single
title: "Privacy and Security Features"
permalink: /docs/privacy-security/
author_profile: true
---

# 🛡️ Privacy & Security Features

**OmniSocial ProtocolKit** is built from the ground up with privacy, encryption, and user sovereignty as core principles — not afterthoughts.

We believe that **freedom requires privacy**, and every user deserves tools that don’t track, exploit, or compromise them.

---

## 🔐 End-to-End Encryption

- **OpenPGP.js**: Encrypts private posts, pay-to-unlock content, and creator messages
- **Matrix Olm/Megolm**: Optional module for full encrypted DMs and group chats
- **Nostr DMs**: Uses shared key encryption (NIP-04) for private messaging
- **Local keypair generation**: No keys stored on the server

See [End-to-End Encryption Implementation](./docs/end-to-end-encryption/) for full details.

---

## 🕵️ Metadata Minimization

We avoid collecting or storing any unnecessary metadata. This includes:

- ✅ No IP logging (unless self-hosted with Nginx config enabled)
- ✅ No email tracking
- ✅ Optional anonymous mode for viewing content
- ✅ Decentralized identity via DIDs and Nostr keys — not OAuth

---

## 🧬 Decentralized Identity

- `username@domain` identity across ActivityPub, ATProto, Matrix, Nostr
- DID Documents published on your domain or via decentralized registries
- Keypair-based access — no reliance on centralized auth systems

---

## ⚡ Lightning-Powered Spam Protection

- Limits free posting to configurable caps (e.g., 5/hour)
- Uses **pay-to-comment**, **pay-to-DM**, and **pay-to-view** as anti-spam mechanisms
- Fully self-custodial — Lightning wallets never exposed or held server-side

---

## 🔄 Transparent & Auditable

- Open-source backend and frontend
- OpenPGP-signed releases planned
- GitHub Actions CI/CD for traceable build pipelines
- All protocol interactions can be logged locally for auditability

---

## 🚨 Moderation with Consent

- Decentralized moderation tools built on roles and room permissions
- No centralized blacklist or surveillance system
- Optional user-run community moderation modules (compatible with ActivityPub & Matrix)

---

## ✅ Your Data, Your Rules

- All content, posts, and keys are exportable
- You can self-host or federate with trusted peers
- No ads, no trackers, no analytics by default
- Self-destructing posts and ephemeral content are planned

---

> OmniSocial is more than software — it’s a declaration of **digital independence**. Privacy is not a feature. It’s your right.
