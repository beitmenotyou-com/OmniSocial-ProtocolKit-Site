---
layout: single
title: "Getting Started"
permalink: /docs/getting-started/
author_profile: true
---

# 🚀 Getting Started with OmniSocial ProtocolKit

Welcome to **OmniSocial ProtocolKit** — your launchpad for building privacy-first, decentralized, and interoperable social platforms.

Whether you're a developer, community builder, or activist, this guide will help you spin up your own federated hub in no time.

---

## 🔧 1. Clone the Repository

Start by cloning the core codebase:

```bash
git clone https://github.com/beitmenotyou-com/OmniSocial-ProtocolKit.git
cd OmniSocial-ProtocolKit
```

---

## ⚙️ 2. Set Up Your Environment

Copy the `.env.example` file and configure your instance:

```bash
cp .env.example .env
```

Edit it with your custom domain, protocol modules to enable, Lightning settings, and federation preferences.

---

## 🧱 3. Install Dependencies

The project supports `bun`, `npm`, or `yarn`.

```bash
bun install
```

Or if using npm:

```bash
npm install
```

---

## 🧪 4. Run the Dev Server

To boot up the local instance:

```bash
bun dev
# or npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) to view your local deployment.

---

## 🧬 5. Explore the Features

Once running, try out:

- Creating a profile (auto-generates Nostr keys + DID)
- Federated posting across ActivityPub, ATProto, and Nostr
- Enabling Lightning for microtransactions
- Sending encrypted messages (E2EE)
- Testing `username@domain` identity resolution

---

## 📚 6. Read the Docs

Use the left sidebar to dive into:

- Protocol Architecture
- Feature Overview
- End-to-End Encryption
- API Reference
- Contribution Guide

---

## 🌐 Live Deployment (Optional)

You can deploy instantly to:

- **Vercel** (CI/CD ready)
- **Netlify** (drag-and-drop)
- **Docker** (for VPS/self-hosting)
- **GitHub Pages** (for docs site only)

We provide deployment templates in the `/deploy/` directory.

---

> This project is yours — fork it, remix it, and help us decentralize the internet for everyone.
