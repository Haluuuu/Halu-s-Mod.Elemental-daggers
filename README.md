🗡️ Elemental Daggers Mod

A Hytale mod that introduces elemental daggers, starting with a Poison Dagger that applies elemental effects directly on normal attacks.

⚠️ Project status: First public release available on GitHub (v1.0.0)

✨ Features

🗡️ New Poison elemental dagger

☠️ Damage-over-time poison effect applied on every hit

Built on Hytale’s official dagger weapon templates

Compatible with quality, level, and durability systems

Structured to easily add more elemental daggers in future updates

🔥 Included Elements (v1.0)

Currently, the mod includes one elemental dagger:

☠️ Poison – Applies damage over time to enemies on hit

Additional elements are planned for future versions.

🧩 How It Works

The Poison Dagger uses Hytale’s InteractionVars system to apply poison effects across multiple attack types.

The poison effect is applied on:

Normal swings (left & right)

Stab attacks

Charged attacks (Pounce)

Signature ability Razorstrike

This ensures that every attack type consistently reflects the poison element.

🧪 Poison Dagger – Technical Details

Quality: Epic
Item Level: 35
Max Durability: 150
Durability loss per hit: 0.1

⚔️ Base Damage
Attack Type	Physical Damage
Normal Swing	2
Stab	6 – 8
Pounce (Charged)	29.5 – 37
Razorstrike	17.5 – 26
☠️ Applied Effects

Poison_Daggers_Hit → Normal swings and stabs

Poison_Daggers_Charged → Successful charged attack

Poison_Daggers_Charged_Fail → Failed charged attack

Poison_Daggers_Special → Razorstrike ability

🎨 Visual Effects

Poison particle effect while idle

Green weapon trail using BlendAdd render mode

Subtle green light emission

🛠️ Crafting Recipe

Required Bench: Weapon Bench (Tier 2)

Materials:

Thorium Bar ×3

Venom Sac ×15

Bone Fragment ×15

Poisoned Trunk ×2
