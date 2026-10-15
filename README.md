# Army Base Survival
A third-person survival shooter built in **Unreal Engine** using **Blueprints only**. Fight through an army base camp, collect coins, dodge turret fire, and avoid damage zones to survive.

Developed as a game development assignment for **CEGA**.

##  Overview

You play as a soldier stranded inside an enemy army base camp surrounded by wooden barracks, watch towers, fuel tanks, and oil pumps. Enemy **turrets** track your every move and open fire. At the same time, **damage hazards** on the ground punish careless movement. Your goal is to collect as many coins as possible while keeping your health above zero.

---

##  Gameplay Features

| Feature | Description |
|---|---|
| **Random Coin Spawning** | Coins spawn at random locations in the level and keep spawning or respawning during gameplay. |
| **Coin Counter (Score)** | A HUD counter in the top-left corner updates every time you collect a coin. |
| **Health Bar** | A health bar (100/100) at the top of the screen drains as you take damage. |
| **Enemy Turret** | A turret that always rotates to face the player and fires projectiles at them. |
| **Projectile Damage** | Bullets that hit the player reduce health. |
| **Damage Zones** | Stepping on a damager (hazard) also reduces health. |
| **Army Base Environment** | A themed military camp with buildings, towers, sandbag bunkers, and desert terrain. |

---

## ✅ Assignment Requirements Checklist

This project fulfils all required features of the **Enemy Shooting Assignment**:

- [x] **Random Object Spawning:** collectible coins spawn at random locations using Blueprints, and keep spawning or respawn after collection.
- [x] **Collectibles and Score System:** the player collects coins, each one increases the score, and the score is displayed on screen.
- [x] **Enemy That Faces the Player:** the turret continuously rotates to face the player.
- [x] **Projectile Shooting:** the enemy turret shoots projectiles toward the player using Blueprints.
- [x] **Player Survival:** the player must dodge bullets and hazards, and health is reduced when hit or when stepping on a damager.

---

## 🕹️ How to Play

1. Start the game and explore the army base camp.
2. **Collect coins** to increase your score. Watch the **Coin** counter on the top-left.
3. **Avoid the turret's bullets.** Each hit drains your health.
4. **Stay away from damage zones.** Stepping on a damager also hurts you.
5. Keep your health above **0** and collect coins to win. *(Update with your exact win/lose condition, e.g. "Collect 20 coins to win".)*

## Blueprint Architecture

The entire game logic is built with Unreal Engine Blueprints.

- **Player Character BP:** handles movement, health, taking damage, and coin collection.
- **Coin BP:** a collectible actor with overlap detection that adds to the score and is destroyed on pickup.
- **Turret / Enemy BP:** every tick, finds the player and rotates to face them (`Find Look at Rotation` → `Set Actor Rotation`), then spawns projectiles on a timer.
- **Damager BP:** a hazard actor that reduces player health when stepped on (overlap event).
- **HUD / Widget BP:** displays the health bar (`100/100`) and the coin counter, bound to player variables.

---

## 🛠️ Tech Stack

- **Engine:** Unreal Engine 5.3.2
- **Scripting:** Blueprints (visual scripting)
- **UI:** UMG (Unreal Motion Graphics)
- **Platform:** Windows

---

## License

This project was created for educational purposes.
