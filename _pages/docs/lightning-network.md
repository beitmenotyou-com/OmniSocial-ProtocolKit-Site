---
layout: single
title: "Lightning Network Integration"
permalink: /docs/lightning-network/
author_profile: true
---

# ⚡ Lightning Network Integration

OmniSocial ProtocolKit integrates the **Bitcoin Lightning Network** to power frictionless microtransactions, spam resistance, and creator monetization — all in a decentralized, self-custodial way.

We use Lightning not just for payments, but to **enable social features** like pay-to-post, pay-to-view, and pay-to-DM.

---

## 🎯 Key Use Cases

| Feature                  | Lightning Use                              |
|--------------------------|--------------------------------------------|
| Pay-to-Comment           | Commenting costs sats (e.g., 10 sats)      |
| Pay-to-DM                | Users can set DM access price              |
| Pay-to-View              | Creators can lock content behind invoices  |
| Spam Protection          | Free post caps + paid unlocks              |
| Creator Monetization     | Full earnings via LNURL/Lightning Address  |

---

## ⚙️ How It Works

### Invoice Flow
1. User clicks to unlock premium content
2. OmniSocial generates a Lightning invoice
3. User pays via their Lightning wallet (e.g., Alby, Phoenix, Breez)
4. On payment success, the content is revealed

### DM / Comment Payments
- Uses **LNURL-pay** or **keysend** to trigger access
- Creators define pricing per message or reply
- Lightning-authenticated user sessions (LSAT optional)

---

## 💸 Supported Wallets & Methods

- **Alby** (browser extension)
- **Phoenix**, **Breez**, **Zeus**
- **LNBits**, **BTCPay Server**, or **Core Lightning** (for self-hosted backends)
- **LNURL**, **Bolt11**, and **Keysend** compatible

---

## 🔐 Self-Custody by Design

We never hold user funds. Lightning is integrated via:
- **LNURL-withdraw** for earnings
- **Webhooks** for invoice monitoring
- Optional **LSAT tokens** for spam prevention

Creators can link their **Lightning Address** to their profile (`@you@domain.com`) for direct tips and payouts.

---

## 🔧 Configuring Lightning

Edit your `.env`:

```env
LIGHTNING_BACKEND=lnbits
LN_API_KEY=your_lnbits_key
LN_WALLET_ID=wallet_id
FREE_POST_LIMIT=5
PAY_TO_COMMENT=10
```

Want to use BTCPay or another backend? Just swap out the adapter module under `/integrations/lightning/`.

---

## 💡 Coming Soon

- ⚙️ Lightning-native federation for unlocking across protocols
- 🧾 LSAT-based API rate limiting
- 🧱 Time-locked access and creator subscriptions

---

> Lightning brings financial freedom to the fediverse — enabling creators to earn and communities to scale, without ads, paywalls, or corporate control.
