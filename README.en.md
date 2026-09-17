# 💣 Hormuz Blockade

**Language / 语言 / 言語：[English](README.en.md) | [繁體中文](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md)**

> How many waves of the US Navy can you hold back? Lay mines, fire anti-ship missiles, and defend the Strait of Hormuz — instant to pick up and play.

**🎮 [Play now](https://jiapunk.github.io/hormuz-blockade/)**

A single-file HTML game. Zero dependencies, zero backend, playable offline. Works on mobile and desktop.

---

## How to Play

You are an IRGC Navy commander. The US Fifth Fleet is trying to force its way through the Strait of Hormuz. You have two weapons:

| Weapon | Controls | Limit |
|--------|----------|-------|
| 💣 Naval mine | Click the sea to lay a mine; ships detonate it on contact | Cooldown-based |
| 🚀 Anti-ship missile | Click a target for a direct strike with splash damage | Ammo-based; refunds on kills |

### Enemy Ships

| Ship | HP | Score |
|------|----|-------|
| Scout boat | 1 | 10 |
| Destroyer | 2 | 30 |
| Cruiser | 4 | 80 |
| Aircraft carrier | 12 | 500 |
| 🛢️ **Civilian oil tanker** | — | **-100** (heavy penalty, combo reset) |

The tanker is the core tension of the game: letting it pass costs you nothing, but blowing it up costs points and breaks your combo. Sink three or more to unlock the "Tanker Butcher" ending.

### Systems

- **Combo multiplier** — chain kills for up to a 20× score bonus
- **Tactical upgrades** — every time your oil fills the bar, pick one of three (threshold rises each time): mine range, cooldown reduction, twin missiles, score multiplier, health, and more; stack infinitely
- **Three lives** — each enemy ship that slips through costs one; run out and it's over

---

## Three Modes

### 🇮🇷 Iran Defense (Main)
A standard blockade that gets harder the longer you hold.

### 📅 Daily Challenge
A special rule set rotates automatically every day — all players worldwide face the same conditions:

| Challenge | Rule |
|-----------|------|
| 🛢️ Tanker Hell | 3× tankers |
| ⚡ Carrier Blitz | Carriers appear early, double kill score |
| 💨 Top Speed | Enemy speed ×1.5 |
| 💣 Mine War | Missiles disabled, mine cooldown halved |
| 🚀 Missile Rain | Infinite missiles, mines disabled |
| ⚔️ Full Fleet | Cruisers and carriers only |
| 💀 One-Life Blockade | 1 life only, score ×2 |

### 🇺🇸 US Breakthrough (Reverse)
Play the other side — pilot a carrier dodging mines and missiles to force through the strait. Its own upgrade path (composite armor, stealth coating, agility) and leaderboard.

---

## Tech

- A single `index.html`, ~70KB
- Hand-written Canvas 2D rendering, no framework, no build step
- Sound synthesized with the Web Audio API — no audio files loaded
- Fixed timestep — identical speed on 60Hz / 120Hz / 144Hz displays
- Safe `localStorage` wrapper — won't crash in Safari private mode or WebViews
- Hard-capped particle count — no frame drops on low-end phones
- Auto-pause when the tab goes to the background
- iPhone notch and home-bar safe-area support

### Run Locally

```bash
git clone https://github.com/jiapunk/hormuz-blockade.git
cd hormuz-blockade
open index.html     # or just double-click
```

No `npm install`, no build. Edit `index.html`, refresh, done.

---

## License

MIT — fork it, remix it, use it commercially.

---

<sub>This game is a work of fiction and parody. Ship names and storyline are satirical and do not represent any political stance.</sub>
