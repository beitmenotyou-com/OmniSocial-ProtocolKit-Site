---
layout: single
title: "Spam Protection Mechanisms"
permalink: /docs/spam-protection/
author_profile: true
---

# 🛡️ Spam Protection Mechanisms

In a decentralized network, spam is a threat to usability, trust, and privacy. OmniSocial ProtocolKit introduces a **self-sovereign, microtransaction-based anti-spam layer** — without relying on captchas, centralized blocklists, or surveillance.

Our approach empowers communities and creators to resist abuse while preserving freedom of expression.

---

## ⚡ Microtransaction Barriers

OmniSocial uses the **Lightning Network** to make spam economically infeasible:

| Action Type       | Default Limit / Cost        |
|-------------------|-----------------------------|
| Posts             | Free up to 5/hour, then paid |
| Comments          | 10 sats each                |
| DMs               | Creator-defined pricing     |
| Content Unlocking | Paid via Lightning invoice  |

These values are configurable in `.env`:

```env
FREE_POST_LIMIT=5
PAY_TO_COMMENT=10
PAY_TO_DM=optional
```

---

## 🧱 Rate Limiting

To prevent bot flooding:

- Per-IP post limits (configurable)
- Rate limits on content creation per user
- Optional Lightning unlocks to bypass limits

---

## 🔐 Identity Cost & Proof-of-Work (Pluggable)

Optional enhancements:

- Pay-to-register flows using Lightning
- Nostr key signing or proof-of-work (e.g. POW CAPTCHA for signup)
- Webfinger + DID validation to reduce sockpuppets

---

## 🧩 Self-Custodial Moderation Tools

Communities can define:

- Post quotas and unlocks
- DM rules and tipping amounts
- Comment pricing based on content category or audience
- Role-based muting, hiding, and flagging tools

All logic lives **client-side or server-local** — never in a centralized API.

---

## 🛠️ Developer Hooks

Anti-spam logic can be extended with:

- Webhook triggers for abuse detection
- Lightning address or pubkey whitelisting
- Token-based access or staking models (future module)

---

## 🧬 Federated Trust, Not Global Bans

OmniSocial avoids centralized moderation lists. Instead:

- Instances can federate or defederate selectively
- Users can block other users or mute protocols
- Decentralized moderation coming via Matrix/ActivityPub governance

---

> Spam resistance should never cost you your privacy. OmniSocial protects you using **incentives, identity, and choice — not surveillance or control.**
