# 💬 Project 1 – On-Screen HUD Tips

This project demonstrates how to create **automatic on-screen HUD tips** in **Unreal Engine 5.5.4** using Blueprints.
It’s a lightweight, polished system that displays short text prompts when players enter trigger zones — perfect for tutorials, hints, or in-world storytelling.

---

## 🖼️ Preview

![HUD Tips Preview](Media/HUDTips.gif)

---

## 🧱 Features

- **WBP_HUDTip** widget with transparent multi-line text box
- **Fade animation** for smooth appearance and disappearance
- **FadeCE custom event** to control UI transitions
- **BP_TriggerZone** actor with overlap detection and player reference
- **Automatic widget creation and removal** during gameplay
- Modular setup — easy to expand for **quest markers**, **tutorials**, or **interactive world prompts**

# 🤖 Project 2 – Following AI Companion

This project demonstrates how to create a **custom AI companion** in **Unreal Engine 5.5.4** using Blueprints.
It blends **AI behavior** and **character design** to build a companion that not only follows the player but also moves and looks uniquely yours — adding personality, rhythm, and presence to the game world.

---

## 🖼️ Preview

![AI Companion Preview](Media/AiCompanion.gif)

---

## 🧱 Features

- **BP_Companion** character duplicated from the player for independent AI control
- **ABP_Companion** animation blueprint with modified skeletal proportions
- **Transform (Modify) Bone** setup to give the companion a unique appearance
- **Pawn Sensing** and **AI Move To** nodes for automatic player tracking
- **Navigation Mesh Bounds Volume** for smooth AI movement within the level
- Modular structure — extendable for **pets**, **followers**, or **story-driven NPCs**

---
