
---

# 🗡️ Elemental Daggers Mod

A **Hytale** mod that introduces **elemental daggers**, each infused with a unique elemental power that enhances fast-paced, close-range combat through status effects, visuals, and elemental damage.

> ⚠️ **Project status:** Public release available on GitHub
> Current version includes **Poison**, **Flame**, and **Ice** daggers.

---

## ✨ Features

* 🗡️ New **elemental daggers**
* ☠️ Poison, 🔥 Fire, and ❄️ Ice elemental effects applied on hit
* Damage-over-time, burn, and slow/freeze mechanics
* Built on Hytale’s official dagger weapon templates
* Compatible with quality, level, and durability systems
* Designed to scale easily with future elemental additions

---

## 🔥 Included Elements (v1.3.0)

The mod currently includes **three elemental daggers**:

* ☠️ **Poison** – Applies poison damage over time
* 🔥 **Flame** – Inflicts burn effects and fire damage
* ❄️ **Ice** – Deals ice damage and slows enemies with freezing effects

> Additional elements may be added in future versions.

---

## 🧩 How It Works

Each dagger uses Hytale’s `InteractionVars` system to apply elemental effects consistently across all attack types.

Elemental effects are applied on:

* Normal swings (left & right)
* Stab attacks
* Charged attacks (Pounce)
* Signature ability **Razorstrike**

This ensures that **every combat action reflects the selected element**.

---

# ☠️ Poison Dagger – Technical Details

**Quality:** Epic
**Item Level:** 35
**Max Durability:** 150
**Durability loss per hit:** 0.1

---

## ⚔️ Base Physical Damage

| Attack Type      | Physical Damage |
| ---------------- | --------------- |
| Normal Swing     | 2               |
| Stab             | 6 – 8           |
| Pounce (Charged) | 29.5 – 37       |
| Razorstrike      | 17.5 – 26       |

---

## 📊 Poison Damage Summary

| Attack Type       | Poison / Tick | Duration | Total Poison Damage | Behavior |
| ----------------- | ------------- | -------- | ------------------- | -------- |
| Normal / Stab     | 10            | 8s       | 20                  | Extend   |
| Charged (Success) | 30            | 6s       | 60                  | Refresh  |
| Charged Fail      | 20            | 6s       | 40                  | Refresh  |
| Razorstrike       | 20            | 8s       | 40                  | Extend   |

---

## ☠️ Applied Effects

* `Poison_Daggers_Hit` – Normal swings and stabs
* `Poison_Daggers_Charged` – Successful charged attack
* `Poison_Daggers_Charged_Fail` – Failed charged stab
* `Poison_Daggers_Special` – Razorstrike ability

---

## 🎨 Visual Effects

* Idle poison particle effects
* Green energy weapon trail (*BlendAdd*)
* Subtle green light emission

---

# 🔥 Flame Dagger – Technical Details

**Quality:** Epic
**Item Level:** 35
**Max Durability:** 150
**Durability loss per hit:** 0.1

---

## ⚔️ Base Damage

| Attack Type      | Damage Type | Damage    |
| ---------------- | ----------- | --------- |
| Normal Swing     | Fire        | 2         |
| Stab             | Physical    | 6 – 8     |
| Pounce (Charged) | Physical    | 29.5 – 37 |
| Razorstrike      | Physical    | 17.5 – 26 |

---

## 🔥 Burn Damage Summary

| Attack Type   | Fire / Tick | Tick Rate | Duration | Total Fire Damage | Behavior |
| ------------- | ----------- | --------- | -------- | ----------------- | -------- |
| Normal / Stab | 5           | 1s        | 2s       | 10                | Extend   |
| Charged Sweep | 17.5        | 1s        | 1s       | 17.5              | Extend   |
| Charged Stab  | 20          | 0.5s      | 1s       | 40                | Extend   |
| Razorstrike   | 25          | 0.5s      | 1s       | 50                | Extend   |

> Burn effects stack by **extending duration**, rewarding aggressive and continuous attacks.

---

## 🔥 Applied Burn Effects

* `Flame_Staff_Burn_Hit` – Normal swings and stab attacks
* `Flame_Staff_Burn_Charged_Slash` – Charged sweep attack
* `Flame_Staff_Burn_Charged` – Charged stab attack
* `Flame_Staff_Burn_Special` – Razorstrike ability

---

## 🎨 Visual & Feedback Effects

* Fire screen overlay on affected targets
* Red-orange entity tint while burning
* Continuous fire particle emission
* Flame weapon trail (*BlendAdd*)
* Fire burst particles on impact
* Burn status icon displayed on affected enemies

---

# ❄️ Ice Dagger – Technical Details

**Quality:** Epic
**Item Level:** 35
**Max Durability:** 150
**Durability loss per hit:** 0.1

---

## ⚔️ Base Physical Damage

| Attack Type      | Physical Damage |
| ---------------- | --------------- |
| Normal Swing     | 2               |
| Stab             | 6 – 8           |
| Pounce (Charged) | 29.5 – 37       |
| Razorstrike      | 17.5 – 26       |

---

## ❄️ Ice Damage Summary

| Attack Type     | Ice Damage | Cooldown | Duration | Behavior |
| --------------- | ---------- | -------- | -------- | -------- |
| Normal / Stab   | 25         | 6s       | 5s       | Extend   |
| Charged Attacks | 35         | 6s       | 5s       | Extend   |
| Razorstrike     | 15 – 25    | 6s       | 5s       | Extend   |

> Ice effects **slow enemies**, apply freezing visuals, and deal **absolute ice damage**.

---

## ❄️ Applied Ice Effects

* `Ice_Daggers_Hit` – Normal swings and stabs
* `Ice_Daggers_Charged` – Charged attacks
* `Ice_Daggers_Special` – Razorstrike ability

---

## 🧊 Crowd Control & Debuff Effects

* Movement slowdown (`HorizontalSpeedMultiplier`)
* Freeze visual VFX (`ModelVFXId: Freeze`)
* Hurt animation feedback
* Ice impact explosions
* Snow & frost particles
* Absolute ice damage type
* Duration stacking via **Extend**

---

## 🎨 Visual & Feedback Effects

* Frost weapon trail (**Medium_Frost**)
* Ice burst hit particles
* Snow impact & explosion effects
* Subtle blue glow light on dagger
* Frozen enemy VFX overlay

---

## 🛠️ Crafting Recipes

### ☠️ Poison Dagger — Weapon Bench Tier 2

* Thorium Bar ×3
* Venom Sac ×15
* Bone Fragment ×15
* Poisoned Trunk ×2
* Emerald Gem ×1

---

### 🔥 Flame Dagger — Weapon Bench Tier 2

* Adamantite Bar ×3
* Ruby Gem ×5
* Fire Essence ×15
* Fire Trunk ×2

---

### ❄️ Ice Dagger — Weapon Bench Tier 2

* Cobalt Bar ×3
* Ice Essence ×15
* Ice Trunk ×2
* Diamond Gem ×1

---

## 🚀 Installation

1. Clone or download the repository from GitHub
2. Copy the mod folder into Hytale’s mods directory
3. Launch the game
4. Enable the mod in the mod menu

---

## 🛠️ Requirements

* **Hytale** (with mod support enabled)

---

## 📌 Roadmap

* [x] Poison elemental dagger
* [x] Flame elemental dagger
* [x] Ice elemental dagger
* [ ] Elemental balance pass
* [ ] More elemental expansions

---

## 🤝 Contributing

Community feedback is welcome and appreciated!

* Element suggestions
* Balance feedback
* Visual and particle improvements
* Code optimizations

Feel free to open an **Issue** or submit a **Pull Request**.

---

## 📜 License

Released under an open license for learning, modification, and community use.

---

## 👤 Author

**Halugamer**
Creator of *Halu’s Mod – Elemental Daggers*

📧 Contact: [Harold.Herrera2375@gmail.com](mailto:Harold.Herrera2375@gmail.com)

---

⭐ If you like this mod, don’t forget to leave a star on GitHub!

---
